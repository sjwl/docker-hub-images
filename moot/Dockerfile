FROM ubuntu:14.04

ENV TERRAFORM_VERSION=0.7.1
ENV TERRAFORM_SHA256SUM=133766ed558af04255490f135fed17f497b9ba1e277ff985224e1287726ab2dc

RUN apt update && apt install -y \
        git bash wget unzip

ADD https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_linux_amd64.zip ./
ADD https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_SHA256SUMS ./

RUN sed -i "/terraform_${TERRAFORM_VERSION}_linux_amd64.zip/!d" terraform_${TERRAFORM_VERSION}_SHA256SUMS
RUN sha256sum -c terraform_${TERRAFORM_VERSION}_SHA256SUMS
RUN unzip terraform_${TERRAFORM_VERSION}_linux_amd64.zip -d /bin
RUN rm -f terraform_${TERRAFORM_VERSION}_linux_amd64.zip

