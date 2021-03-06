---
title: MarkDown学习笔记
date: 2019-12-23 23:00:00
author: 小茗
img: https://www.xmubshw.com/down/xdh/MarkDownimg.jpg
top: true
cover: true
coverImg: https://www.xmubshw.com/down/xdh/MarkDownimg.jpg
mathjax: false
summary: MarkDown学习笔记
categories: Markdown
tags:
  - Typora
  - Markdown
---
# MarkDown

```
轻量级标记语言.
理解:比如Html需写120个字符,但用MarkDown只需要写30字符.
用途:主要用于写项目文档.
```
***

## 标题:

|一级标题|二级标题|
|:-:|:-:|
|======|------|

***

### 多种写法:

|一级标题|二级标题|三级标题|四级标题|五级标题|六级标题|
|:-:|:-:|:-:|:-:|:-:|:-:|
|#|##|###|####|#####|######|

***

## 字体:

### 三种字体写法:

|斜体|粗体|粗斜体|
|:-:|:-:|:-:|
|* 斜体 *|** 粗体 **|***  粗斜体  ***|
|_ 斜体 _|__ 粗体 __|___ 粗斜体 ___|

***

## 分割线:

```
可用三个以上的星号(*)或者减号(-)或者下划线(_)来建立分割线;
```

|第一种|第二种|第三种|
|:-:|:-:|:-:|
|***|---|___|

***

## 删除线:

```
文字两端加两个波浪线;
~~MarkDown~~
```

### 例:

~~MarkDown~~
***

## 下划线:

```
不可直接表示,需借用Html标签<u></u>表示.
<u>MarkDown</u>
```

### 例:

<u>MarkDown</u>
***

## 角标:

```
小茗Ub生活网[^小茗Ub生活网]
```

### 例:

小茗Ub生活网[^小茗Ub生活网]
***

## 列表:

|有序列表|无序列表|
|:-:|:-:|
|1.第一项|* 第一项|
|2.第二项|* 第二项|
|3.第三项|* 第三项|

### 例:

#### 有序列表:

1.第一项

#### 无序列表:

* 第一项

***

## 列表嵌套:

|有序列表|
|:-:|
|1.第一项(此项后加四个空格,即为列表嵌套) * 嵌套第一项|
|2.第二项(此项后加四个空格,即为列表嵌套) - 嵌套第二项|
|3.第三项(此项后加四个空格,即为列表嵌套) - 嵌套第三项|

### 例:

1.第一项
* 嵌套第一项

***

## 区块:

```
> 最外层
> > 第一层
> > > 第二层
> > > > 第三层
```

### 例:

> 最外层
> > 第一层
> > > 第二层
> > > > 第三层
***

## 代码:

```
需用''括起来.
```
***

## 代码区块:

```
需用上下三个```符号把代码包起来
```

### 例:

```
<u></u>
```
***

## 链接:

|链接①|链接②|
|:-:|:-:|
|[名称](链接)|<链接>|

链接③:
```
[名称][随便给一个值]
[值]:链接
```
***

## 图片:

```
![给一个值](图片地址)
```

### 例:

![xm](https://www.xmubshw.com/down/logo.png)

***

## 表格:

```
|左|中|右|
|:-|:-:|-:|
|左|中|右|
```

### 例(因为浏览器兼容问题,可能表格样式会显示不全,但书写格式是标准的):

|左|中|右|
|:-|:-:|-:|
|左|中|右|

***

## 上标和下标:

```
可用Html标签
<sup>文字</sup>为上标
<sub>文字</sub>为下标
```

### 例:

|上标|下标|
|:-:|:-:|
|益达<sup>Tm</sup>|Ho<sub>2</sub>|

***

## 正常显示普通符号:

```
使用反斜杠(\)转义特殊字符
\* 正常显示星号(*) \*
```

### 例:

\* 正常显示星号 \*

***

## 自动生成目录:

```
使用[toc],放在MarkDown文档最上方,会自动生成目录
```

***

## 常用符号:
|常用符号①|常用符号②|常用符号③|
|:-:|:-:|:-:|
|\(反斜杠)|`(反引号)|*(星号)|
|_(下划线)|{}(花括号)|[] (方括号)|
|()(小括号)|#(#号)|+(加号)|
|-(减号)|.(英文句号)|!(感叹号)|