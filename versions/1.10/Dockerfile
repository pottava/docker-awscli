# AWS-CLI v1.10
# docker run --rm pottava/awscli --version
# docker run --rm -v $HOME/.aws:/root/.aws pottava/awscli iam list-users

FROM pottava/python:2.7

RUN apk --no-cache add --virtual build-dependencies py-pip \
      && apk --no-cache add groff jq \
      && pip install 'awscli == 1.10.67' \
      && apk del --purge -r build-dependencies

VOLUME /root/.aws

ENTRYPOINT ["aws"]
CMD ["--version"]
