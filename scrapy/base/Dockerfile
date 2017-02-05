FROM alpine:latest
MAINTAINER zhangguanglei <xian0617@gmail.com>

ENV RUNTIME_PACKAGES ca-certificates python py-pip git curl libxslt libxml2 openssl
ENV BUILD_PACKAGES build-base libxslt-dev libxml2-dev libffi-dev python-dev openssl-dev 

RUN apk add --no-cache ${RUNTIME_PACKAGES} ${BUILD_PACKAGES} && \
    pip install --upgrade pip && \
    pip --no-cache-dir install \
      git+https://github.com/scrapy/scrapy.git \
      git+https://github.com/scrapy/scrapyd.git \
      git+https://github.com/scrapy/scrapyd-client.git \
      git+https://github.com/scrapinghub/scrapy-splash.git \
      && rm -rf /root/.cache && \
  curl -sSL https://github.com/scrapy/scrapy/raw/master/extras/scrapy_bash_completion >> /root/.bashrc
  
