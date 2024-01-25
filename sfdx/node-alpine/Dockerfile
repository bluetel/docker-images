FROM node:16-alpine

RUN apk upgrade --no-cache \
    && apk add --no-cache --upgrade \
    bash \
    ca-certificates \
    curl \
    git \
    jq \
    openssh

# Installing SFDX
RUN npm i @salesforce/cli@2.24.4 --global --no-save
RUN sfdx --version
