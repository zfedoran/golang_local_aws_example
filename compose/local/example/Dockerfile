FROM golang:alpine

RUN apk --no-cache update && \
    apk --no-cache add python3 py3-pip py-setuptools ca-certificates bash curl && \
    pip --no-cache-dir install awscli && \
    rm -rf /var/cache/apk/*


COPY ./compose/local/example/entrypoint /entrypoint
RUN sed -i 's/\r$//g' /entrypoint
RUN chmod +x /entrypoint

COPY ./compose/local/example/start /start
RUN sed -i 's/\r$//g' /start
RUN chmod +x /start

WORKDIR /app
ENTRYPOINT ["/entrypoint"]