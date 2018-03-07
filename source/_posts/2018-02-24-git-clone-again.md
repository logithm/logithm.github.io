---
title: git clone again
date: 2018-02-24 14:48:04
tags: [git, hexo]
categories: 工具
keywords:
description: 终于在B电脑上有机会尝试git clone了, 过程看起来很low. 
---

```
1. install node
2. install git
3. ssh-keygen
4. git config --global user.name "xyzio"
5. git config --global user.email "xyzio@gmail.com"
6. git config --global http.postBuffer 1048576000
7. npm install hexo-cli -g
```


第一步: 在A电脑上部署了一切

第二步: 在B电脑上建立了[同步环境](http://chitanda.me/2015/06/18/hexo-sync-in-multiple-pc/)  

1. 在hexoblog目录下git init
1. 新建hexoblog\xyzio.github.io目录, 以下操作在该目录下进行.
1. git init
1. git remote add origin https://github.com/xyzio/xyzio.github.io.git
1. git fetch --all
1. git reset --hard origin/hexo
1. 拷贝node_modules, public, themes/next到相应的目录
1. 运行myhexo.sh大招

以下才是日常
下班前在B电脑运行myhexo.sh大招, 回到家在A电脑运行git pull. 依此循环.


[hexo 多终端同步博客](http://www.joahcy.com/BuildBlog/mutil_term_sync/): 这篇博文应该也是对的.
____________________

A电脑上把一切都弄好, 包括node等环境, hexo安装配置, github的本地及远程仓库.

B电脑上先建立node等环境, hexo安装好. 然后再建立本地github的仓库, 与远程搭上关系, 再clone下来. 

B电脑上如果有改动, 则myhexo.sh, 将github与B同步, 保证github上的是最新的. 

回到A电脑, 先git pull.
