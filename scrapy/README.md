# base
build base env from alpin
- build
    - docker build -t zgl/scrapy_base:latest ./base

# dev
- build
    - docker build -t zgl/scrapy_dev:latest ./dev
- start
    - docker run -it --name dev zgl/scrapy_dev:latest
    - docker start dev
- stop
    - docker stop dev
# scrapyd
- [官网](http://scrapyd.readthedocs.io/en/latest/)

- build
    - docker build -t zgl/scrapyd:latest ./scrapyd
- start
    - docker run -d --name scrapyd -p6800:6800 zgl/scrapyd
    - docker start scrapyd
    - docker attach scrapyd
- stop
    - docker stop scrapyd && docker rm scrapyd

# scrapy-splash
- [git address](https://github.com/scrapinghub/splash) 
- [docker address](https://hub.docker.com/r/scrapinghub/splash/)

- docker command

    需注意port映射到内网上
    - docker pull scrapinghub/splash
    - docker run -d -p 8050:8050 --name splash scrapinghub/splash
    - docker start splash
    - docker stop splash