FROM adoptopenjdk/openjdk12:alpine-slim
LABEL maintainer="uhooi <the_uhooi@yahoo.co.jp>"

ARG VERSION="1.10.4"

RUN set -x && \
    export REDPEN_URL="https://github.com/redpen-cc/redpen" && \
    export DOWNLOAD_URL="${REDPEN_URL}/releases/download/redpen-${VERSION}/redpen-distribution-${VERSION}-assembled.tar.gz" && \
    wget -q ${DOWNLOAD_URL} -O /tmp/redpen.tar.gz && \
    tar -xzvf /tmp/redpen.tar.gz && \
    cp -av redpen-distribution-${VERSION}/* /usr/local/ && \
    rm -rf redpen-distribution-${VERSION} /tmp/redpen.tar.gz && \
    unset REDPEN_URL DOWNLOAD_URL

COPY logback.xml /usr/local/conf/logback.xml

WORKDIR /work
ENTRYPOINT ["/usr/local/bin/redpen"]

