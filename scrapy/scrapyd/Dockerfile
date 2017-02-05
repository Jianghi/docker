FROM zgl/scrapy_base:latest
MAINTAINER zhangguanglei <xian0617@gmail.com>

ENV BUILD_PACKAGES build-base libxslt-dev libxml2-dev libffi-dev python-dev openssl-dev 
RUN apk del ${BUILD_PACKAGES}
ADD ./scrapyd.conf /etc/scrapyd/
EXPOSE 6800
CMD ["scrapyd"]
