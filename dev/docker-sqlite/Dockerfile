# -- DEV DOCKERFILE --
# -- DO NOT USE IN PRODUCTION! --

FROM node:10-alpine
LABEL maintainer "requarks.io"

RUN apk update && \
    apk add bash curl git python make g++ nano openssh gnupg sqlite --no-cache && \
    mkdir -p /wiki

WORKDIR /wiki
COPY package.json .
RUN yarn --silent

ENV dockerdev 1
ENV DEVDB sqlite

EXPOSE 3000

CMD ["tail", "-f", "/dev/null"]
