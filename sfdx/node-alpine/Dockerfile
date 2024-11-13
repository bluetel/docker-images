FROM node:18-alpine

RUN apk upgrade --no-cache \
    && apk add --no-cache --upgrade \
    bash \
    ca-certificates \
    curl \
    git \
    jq \
    openssh \
    openjdk21 \
    chromium \
    nss \
    freetype \
    harfbuzz \
    ca-certificates \
    ttf-freefont \
    nodejs \
    yarn

# Installing SFDX
RUN npm i @salesforce/cli --global --no-save
RUN sfdx --version

# Installing vlocity build tool
RUN npm i --global vlocity --no-save

# Tell Puppeteer to skip installing Chrome. We'll be using the installed package.
ENV PUPPETEER_EXECUTABLE_PATH=/usr/bin/chromium-browser

# Puppeteer v23.8.0 works with Chromium 130.
RUN yarn add puppeteer@23.8.0
