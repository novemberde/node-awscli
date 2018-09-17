
FROM docker:stable

# Install Docker
RUN apk update && apk add nodejs nodejs-npm
RUN apk update && apk add --virtual build-dependencies build-base gcc wget git
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

CMD ["sh"]