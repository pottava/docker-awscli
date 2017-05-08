# AWS-CLI v1.11
# docker run --rm pottava/awscli --version
# docker run --rm -v $HOME/.aws:/root/.aws pottava/awscli iam list-users

FROM pottava/python:2.7

RUN apk --no-cache add --virtual build-dependencies py2-pip \
      && apk --no-cache add groff jq \
      && pip install 'awscli == 1.11.83' \
      && apk del --purge -r build-dependencies

ENTRYPOINT ["aws"]
CMD ["--version"]
