---
title: Hexo導入から公開記事作成まで
tags: hexo
date: 2020-11-13 13:53:07
---



### docker-compose.yml 作成

```
version: '3'
services:
  blog:
    build: ./generator/
    container_name: hexo
    volumes: 
      - ./generator/app:/usr/src/app
    ports:
      - 4000:4000
    tty: true
```

<!-- more -->

### docker-compose build

```
docker-compose build --no-cache
```

### blog コンテナへアクセス

```
docker-compose exec blog /bin/sh
```

### sample プロジェクト作成＆移動

```
hexo init sample && cd sample
```

### 下書き記事を作成

```
hexo new draft introduction
```

### 下書き記事表示オプションでサーバ起動

```
hexo server --draft
```

### 下書き記事を公開フォルダへ移動

```
hexo publish introduction
```
