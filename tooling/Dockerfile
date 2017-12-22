FROM hashicorp/terraform:0.11.1 AS terraform
FROM airhelp/kops:latest
COPY --from=terraform $(which terraform) /usr/bin/terraform 
MAINTAINER "sjwl https://github.com/sjwl"

ENTRYPOINT []
