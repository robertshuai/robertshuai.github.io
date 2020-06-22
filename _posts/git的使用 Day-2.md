---
layout: post
title: '算法笔记（第一周）'
subtitle: '算法'
date: 2020-6-21
categories: 技术
cover: 'http://on2171g4d.bkt.clouddn.com/jekyll-theme-h2o-postcover.jpg'
tags: jekyll 前端开发 设计
---



如何安全高效地管理代码？
1、把现有的项目或新项目用Git管理
$ mkdir test

$ cd test

$ git init

$ touch readme.txt

$ git add readme.txt

$ git commit -m "add readme.txt"

# 简单解释一下git commit命令，-m后面输入的是本次提交的说明，可以输入任意内容，当然最好是有意义的，这样你就能从历史记录里方便地找到改动记录。

$ git status

$ git remote add origin 远程仓库URL

# 执行推送或者拉取的时候，如果省略了远程仓库的名称，则默认使用名为”origin“的远程仓库。因此一般都会把远程仓库命名为origin。

$ git push origin master

# PS：当被要求输入用户名和密码，请使用你在GitHub的用户名和密码。

# 由于远程仓库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送到远程新的master分支，还会把本地的master分支

# 和远程的master分支关联起来，那么下一次推送时就可以省略分支名称了。但是，首次必须指定远程仓库名称和分支名称。



2、从远程仓库克隆到本地（推荐）
$ git clone 远程仓库URL

# PS：当被要求输入用户名和密码，请使用你在GitHub的用户名和密码。

$ cd 远程仓库目录名

$ touch README.md

$ git add README.md

$ git commit -m "add Readme.md"

$ git push

如何快速高效地获取他人优秀代码？

GitHub：https://github.com/



3、Git 技巧篇
给文件重命名的简便方法

$ git clone 远程仓库地址 

$ cd 远程仓库目录

$ touch README.txt

$ git add README.txt

$ git commit -m "add readme.txt"

$ git push

$ git log

# 彻底回退到某个版本

$ git reset --hard 版本号（必须慎用！！！）

$ git log

# 简便做法

$ git mv README.txt README.md

$ git status

$ git commit -m "rename readme"

$ git log

正确删除文件的方法

# 简便做法

$ git rm readme.md
