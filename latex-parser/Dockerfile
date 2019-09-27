FROM nimamahmoudi/texlive-2019
LABEL maintainer="nima_mahmoudi@live.com"

# Install Pandoc
RUN apt-get update \
    && apt-get install --no-install-recommends -y \
        pandoc pandoc-citeproc\
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
