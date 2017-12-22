FROM hashicorp/terraform:0.11.1 AS terraform
RUN cp $GOPATH/bin/terraform /terraform
FROM airhelp/kops:latest
COPY --from=terraform /terraform /usr/bin/terraform 
MAINTAINER "sjwl https://github.com/sjwl"

ENTRYPOINT []
