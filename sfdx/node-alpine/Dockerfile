FROM node:10-alpine


RUN apk add ca-certificates

# Installing JQ
RUN apk update \
 && apk add jq \
 && rm -rf /var/cache/apk/*
RUN jq --version

# Installing SFDX
RUN npm install sfdx-cli --global --no-save
RUN sfdx --version