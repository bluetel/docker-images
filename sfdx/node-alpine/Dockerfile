FROM node:18-alpine

RUN apk upgrade --no-cache \
    && apk add --no-cache --upgrade \
    bash \
    ca-certificates \
    curl \
    git \
    jq \
    openssh \
    openjdk21

# Installing SFDX
RUN npm i @salesforce/cli@2.68.6 --global --no-save
RUN sf --version

# Installing vlocity build tool
RUN npm i --global vlocity --no-save
