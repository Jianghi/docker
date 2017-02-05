# base
build base env from alpin

# scrapy
- build
    - docker build -t zgl/scrapy_dev:latest ./dev
- start
    - docker run -it --name dev zgl/scrapy_dev:latest

# scrapyd
- [官网](http://scrapyd.readthedocs.io/en/latest/)

- build
    - docker build -t zgl/scrapyd:latest ./scrapyd
- start
    - docker run -d --name scrapyd -p6800:6800 zgl/scrapyd
- stop
    - docker stop scrapyd && docker rm scrapyd

# scrapy-splash
- [git address](https://github.com/scrapinghub/splash) 
- [docker address](https://hub.docker.com/r/scrapinghub/splash/)

- docker command

    需注意port映射到内网上
    - docker pull scrapinghub/splash
    - docker run -p 8050:8050 scrapinghub/splash
