---
title: Vim基本命令学习笔记
date: 2019-12-24 11:00:00
author: 小茗
img: https://bbsfiles.vivo.com.cn/vivobbs/attachment/forum/201803/18/121017tlaa2ia8asaa28pc.jpg!t700x2000.jpg
top: true
cover: true
coverImg: https://bbsfiles.vivo.com.cn/vivobbs/attachment/forum/201803/18/121017tlaa2ia8asaa28pc.jpg!t700x2000.jpg
mathjax: false
summary: Vim基本命令学习笔记
categories: Vim
tags:
  - Git
---
# Git

## 概念:

```
分布式版本控制系统
```

## 安装:

### 在 Linux 上安装:

如果你想在 Linux 上用二进制安装程序来安装 Git，可以使用发行版包含的基础软件包管理工具来安装。
```
$ sudo yum install git
```
如果你在基于 Debian 的发行版上，请尝试用 apt-get：
```
$ sudo apt-get install git
```

***

## 创建:


创建空目录:
```
mkdir 目录名
```
打开目录:
```
cd 目录名
```
把目录变成Git可管理的仓库:
```
git init
```

提交用户名:
```
$ git config --global user.name "用户名"
```

提交邮箱:

```
$ git config --global user.email "邮箱"
```

建立本机SSH协议秘钥:

```
ssh-keygen -t rsa -C '邮箱'
```

建立与远程库的链接(建议用ssh协议):

```
git remote add 需要设置的库名 远程库的链接
```

***

## 常用命令:


### 将文件提交到暂存区:

```
git add 文件名
```
***

### 将暂存区文件提交到本地版本库:

```
git commit -m "说明"
```
***

### 查看工作区状态:

```
git status
```
***

### 回退:

```
git checkout --hard HEAD^
```
此处(HEAD^为上个版本,可换为版本ID号)

#### 将暂存区还未提交的改动撤销:

```
git reset HEAD 文件名
```

#### 将提交到版本库里的文件替换回暂存区(参考版本回退):

```
git checkout -- 文件名
```
***

### 查看提交历史:

```
git reflog
```
***

### 丢弃工作区:

```
git checkout -- 文件名
```
***

### 删除:

#### 步骤①:
```
rm 文件名
```

#### 步骤②:
```
git rm 文件名
```

#### 步骤③:
```
git commit -m "说明"
```
***

### 误删除一个文件,恢复操作:

```
git reset HEAD 文件名
```
或者
```
git checkout -- 文件名
```
***

### 分支操作:

#### 创建并切换分支:

```
git checkout -b 分支名
```

#### 切换分支:

```
git checkout 分支名
```

#### 查看分支:

```
git branch
```

##### 查看远程分支(此命令实际是查看所有分支):

```
git branch -a
```


#### 删除分支:

```
git branch -d 分支名
```

##### 删除远程分支:

```
git push -d 库名 分支名
```

#### 修改分支名称:

##### 修改本地分支名称:

```
git branch -m 当前分支名 需要修改的分支名
```

##### 修改远程分支名称:

```
第一步:先删除远程分支
第二步:更改本地分支名
第三步:上传本地分支到远程库
```

#### 合并某分支到当前分支:

```
git merge 分支名
```

也可用'rebase'变基操作.

#### 查看分支合并情况:

```
git log --graph
```

#### 隐藏工作区:

```
git stash
```

#### 显示工作区:

```
git stash list
```

#### 恢复工作区:

```
git stash pop
```

#### 恢复工作区后复制一个特定的提交到当前分支:

```
git cherry-pick 版本ID号
```
***

### 抓取和提交以及克隆:

#### 抓取:

```
git pull 库名 分支名
```

每次抓取完成后都要对比信息是否正确:

```
git diff
```

#### 提交:

##### 向远程推送分支内容:

```
git push 库名 分支名
```

推送本地分支到远程分支:

```
git push 库名 本地分支名:远程分支名
```

#### 克隆:

```
git clone git链接
```

#### 远程库:

##### 查看远程库:

```
git remote -v
```

##### 删除远程库:

```
git remote rm 库名
```
***

### 标签:

#### 如何打标签:

先切换到需要打标签的分支上;

```
git checkout 分支名
```

打标签:

```
git tag 标签内容
```

给历史内容打标签:

```
git log 标签内容 ID号
```

创建有说明的标签:

```
git tag -a 标签内容 -m "说明" ID号
```

#### 查看标签:

```
git tag
```

#### 查看标签说明:

```
git show 标签名
```

#### 删除标签:

```
git tag -d 标签名
```

#### 推送标签:

```
git push 库名 标签名
```

一次性推送未推送到远程的标签:

```
git push 库名 --tags
```

#### 远程删除标签

第一步:必须先删除本地标签;

```
git tag -d 标签名
```

第二步:再删除远程标签;

```
git push 库名 :refs/tags/标签名
```
***