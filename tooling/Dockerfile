FROM hashicorp/terraform:0.11.1 AS terraform
WORKDIR $GOPATH/src/github.com/mcuadros/terraform-provider-helm
RUN git clone https://github.com/mcuadros/terraform-provider-helm.git ./ && \
make build
RUN cp $GOPATH/bin/terraform* /terraform*
FROM airhelp/kops:latest
COPY --from=terraform /terraform* /usr/bin/terraform*
MAINTAINER "sjwl https://github.com/sjwl"

RUN apk --no-cache add jq && rm -f /var/cache/apk/*

ENTRYPOINT []
