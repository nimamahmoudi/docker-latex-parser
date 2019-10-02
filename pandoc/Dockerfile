FROM debian:10
LABEL maintainer="nima_mahmoudi@live.com"

# Update with latest version every once in a while: https://github.com/jgm/pandoc/releases/
RUN apt-get update \
    && apt-get install --no-install-recommends -y \
        wget \
    && wget https://github.com/jgm/pandoc/releases/download/2.7.3/pandoc-2.7.3-1-amd64.deb -O pandoc-amd64.deb \
    && dpkg -i pandoc-amd64.deb \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

