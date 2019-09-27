FROM debian:10

# Original Installation Manager File:
# ftp://tug.org/historic/systems/texlive/2019/install-tl-unx.tar.gz

# Install TeX live
COPY texlive.profile /
RUN apt-get update \
  && apt-get install --no-install-recommends -y \
    wget perl fontconfig libwww-perl \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/* \
  && wget https://github.com/nimamahmoudi/docker-latex-parser/raw/master/texlive/2019/install-tl-unx.tar.gz \
  && tar xzvf install-tl-unx.tar.gz \
  && ./install-tl-*/install-tl -profile texlive.profile \
  && rm -rf install-tl-*

ENV PATH="/usr/local/texlive/2019/bin/x86_64-linux:${PATH}"
