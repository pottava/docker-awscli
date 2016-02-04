# AWS-CLI
# docker run --rm pottava/awscli aws --version
# docker run --rm -v $HOME/.aws:/root/.aws pottava/awscli aws ec2 describe-instances

FROM pottava/python:2.7

RUN apk --no-cache add --virtual build-dependencies py-pip \
      && apk --no-cache add groff jq \
      && pip install awscli \
      && apk del build-dependencies
