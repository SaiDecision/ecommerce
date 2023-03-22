FROM alpine:3.15 as alpine
LABEL maintainer="sspdevops89@gmail.com"

# Perform apk update
RUN apk --no-cache update && apk upgrade && \
    rm -rf /tmp/* /var/cache/apk/*

FROM scratch
COPY --from=alpine / /
CMD ["/bin/sh"]
