FROM alpine:latest
MAINTAINER zhangguanglei <xian0617@gmail.com>

ENV RUNTIME_PACKAGES ca-certificates python py-pip git curl libxslt libxml2 openssl py-mysqldb py-redis py-hiredis
ENV BUILD_PACKAGES build-base libxslt-dev libxml2-dev libffi-dev python-dev openssl-dev 
RUN apk update && apk add ${RUNTIME_PACKAGES} ${BUILD_PACKAGES} 
RUN mkdir -p ~/.pip/
ADD ./pip.conf ~/.pip/
#RUN pip install --upgrade pip && \
#    pip --no-cache-dir install \
#      git+https://github.com/scrapy/scrapy.git \
#      git+https://github.com/scrapy/scrapyd.git \
#      git+https://github.com/scrapy/scrapyd-client.git \
#      git+https://github.com/scrapinghub/scrapy-splash.git \
RUN pip install --upgrade pip &&\
    pip --no-cache-dir install \
      scrapy \
      scrapyd \
      scrapyd-client \
      scrapy-splash \
      && rm -rf /root/.cache && \
  curl -sSL https://github.com/scrapy/scrapy/raw/master/extras/scrapy_bash_completion >> /root/.bashrc
  
