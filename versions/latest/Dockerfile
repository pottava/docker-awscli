# AWS-CLI
# docker run --rm pottava/awscli aws --version

FROM pottava/python:2.7

RUN apk --no-cache add --virtual build-dependencies py-pip \
      && pip install awscli \
      && apk del build-dependencies
