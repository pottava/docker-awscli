# AWS-CLI v1.14
# docker run --rm pottava/awscli --version
# docker run --rm -v $HOME/.aws:/root/.aws pottava/awscli iam list-users

FROM alpine:3.7

ENV PAGER=less \
    LESS="-eirMX"

RUN apk --no-cache add python less
RUN apk --no-cache add --virtual build-dependencies py2-pip \
      && apk --no-cache add groff jq \
      && pip install 'awscli == 1.14.70' \
      && apk del --purge -r build-dependencies

ENTRYPOINT ["aws"]
CMD ["--version"]
