---
title: GitHubPagesへデプロイする
tags: hexo
date: 2020-11-14 04:04:59
---


### Git設定
```
git config --global user.name "アカウント名"
git config --global user.email "メールアドレス"
```

<!-- more -->

### _config.yml設定(編集箇所のみ抜粋)
```
url: https://{githubのusername}.github.io/{リポジトリ名}/
root: /{リポジトリ名}
type: git
  repo: {クローンURL}
  branch: {設定するブランチ名}
```

### デプロイ実施
```
hexo deploy
```

### トラブルシューティング

下記のようなエラーメッセージが表示される場合は
```
/usr/src/app/sample # hexo deploy
INFO  Validating config
ERROR Deployer not found: git
```
下記のコマンドを実施してみてください
```
npm install hexo-deployer-git --save
```
