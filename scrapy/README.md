# base
 build base env from alpin

# scrapy
- docker build -t zgl/scrapy_dev:latest ./scrapy

# scrapyd
- http://scrapyd.readthedocs.io/en/latest/

- docker build -t zgl/scrapyd:latest ./scrapyd
- docker run -d --name scrapyd -p6800:6800 zgl/scrapyd
- docker stop scrapyd
- docker rm scrapyd

# scrapy-splash
- [git address](https://github.com/scrapinghub/splash) 
- [docker address](https://hub.docker.com/r/scrapinghub/splash/)

- docker command
    
    需注意port映射到内网上

    - docker pull scrapinghub/splash
    - docker run -p 8050:8050 scrapinghub/splash
