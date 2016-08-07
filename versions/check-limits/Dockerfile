# AWS limits checker
# @see https://github.com/joehack3r/aws
# docker run --rm -it -v $HOME/.aws:/root/.aws pottava/awscli:check-limits

FROM pottava/awscli:latest

ENV COMMIT=41fb72b028de4ab4052648147c83380f657e705b

RUN apk --no-cache add curl bash bc \
      && curl -o /usr/local/bin/statsd-client https://raw.githubusercontent.com/etsy/statsd/master/examples/statsd-client.sh \
      && curl -o /usr/local/bin/check-aws-limits https://raw.githubusercontent.com/joehack3r/aws/${COMMIT}/scripts/check-aws-limits.sh \
      && sed -i -e 's/tr --delete/tr -d/g' /usr/local/bin/check-aws-limits \
      && chmod +x /usr/local/bin/* \
      && apk del --purge curl

ENTRYPOINT ["check-aws-limits"]
