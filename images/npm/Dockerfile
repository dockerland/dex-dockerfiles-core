FROM alpine

#
# v1 dex-api
#
ENV \
  DEX_API="v1" \
  HOME="/dex/home" \
  WORKSPACE="/dex/workspace"

RUN mkdir -p $HOME $WORKSPACE
VOLUME /dex

#
# npm image
#

RUN apk add --update \
    nodejs \
    && rm -rf /var/cache/apk/*

RUN npm install -g npm

ENTRYPOINT ["npm"]
CMD ["--help"]
