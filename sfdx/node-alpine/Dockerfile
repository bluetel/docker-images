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
RUN npm i @salesforce/cli --global --no-save
RUN sfdx --version

# Installing vlocity build tool
RUN npm i --global vlocity --no-save

# Installing puppeteer
RUN npm i --global puppeteer --no-save
