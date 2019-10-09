FROM node:10-alpine


RUN apk add ca-certificates

RUN npm install sfdx-cli --global --no-save
RUN sfdx --version