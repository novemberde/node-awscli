FROM docker:stable

# Install Docker
RUN apk add --virtual build-dependencies build-base gcc wget git
RUN apk -v --update add \
        python \
        py-pip \
        groff \
        less \
        mailcap \
        && \
    pip install --upgrade awscli==1.14.5 s3cmd==2.0.1 python-magic && \
    apk -v --purge del py-pip && \
    rm /var/cache/apk/*

RUN apk update && apk add bash
RUN apk update && apk add --update nodejs nodejs-npm
RUN npm i -g npm
RUN npm i -g node-gyp

ENTRYPOINT []
CMD ["sh"]