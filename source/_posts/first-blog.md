---
title: first blog
date: 2020-02-09 23:51:38
tags: hexo
---

## 如何初始化github博客

1 . 安装npm
``` shell
xcode-select --install
npm install hexo-cli -g
```

2 . 初始化博客

``` shell
hexo init
npm install
hexo g
hexo s
```

3 . 安装对应插件

```shell 
npm i hexo-deployer-git # 安装git同步插件  使用https同步 
git config --global credential.helper store # 修改git配置 存储密码 
```
修改配置文件
```yaml
deploy:
  type: git
  repo: <repository url> # https://bitbucket.org/JohnSmith/johnsmith.bitbucket.io
  branch: [branch]
  message: [message]
```

4 . 编写博客

```shell
hexo new post 'tile'
hexo generate
hexo server
hexo clean&&hexo deploy
```
