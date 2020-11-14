From node:14-alpine

WORKDIR /usr/src/app

RUN apk add git
RUN npm install -g hexo-cli
RUN npm install -g hexo-deployer-git
RUN npm install -s hexo-asset-link
RUN npm install hexo-renderer-marked --save

EXPOSE 4000
