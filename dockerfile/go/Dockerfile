FROM ttbb/base:latest

ARG version=1.19
ARG TARGETARCH

RUN wget https://golang.org/dl/go$version.linux-$TARGETARCH.tar.gz && \
    tar -C /usr/local -xzf go$version.linux-$TARGETARCH.tar.gz && \
    ln -s /usr/local/go/bin/go /usr/bin/go && \
    ln -s /usr/local/go/bin/gofmt /usr/bin/gofmt && \
    rm -rf go$version.linux-$TARGETARCH.tar.gz
