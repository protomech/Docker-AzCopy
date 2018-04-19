FROM microsoft/dotnet:2.1-runtime-alpine
MAINTAINER Boshi Lian <farmer1992@gmail.com>

RUN apk update && apk add ca-certificates && update-ca-certificates && \
    apk add openssl bash rsync && \
    mkdir /tmp/azcopy && \
    wget -O /tmp/azcopy/azcopy.tar.gz https://aka.ms/downloadazcopyprlinux &&  \
    tar -xf /tmp/azcopy/azcopy.tar.gz -C /tmp/azcopy &&  \
    /tmp/azcopy/install.sh

RUN rm -rf /tmp/azcopy

CMD ["/usr/bin/azcopy"]
