---
title: hexo搭建博客保姆级别教程
date: 2021-03-29 17:57:34
tags:
cover: https://img.imgdb.cn/item/6061a5818322e6675cdea5b0.jpg
---

> 在写之前踩了很多坑，先感谢butterfly-2群的各位大佬的指点让我从小白到入门，此篇文章记录一下搭建的过程以及遇到的坑，希望能帮助到跟我刚入坑的小白

## 安装git



### 1、git下载&安装

官网下载即可，直接下一步，然后完成（[下载官网直通车](https://git-scm.com/download/win)）

> 电脑是32位的下载32-bit，反之64-bit

![](https://img.imgdb.cn/item/6065d4968322e6675c00edc7.png)





### 2、验证git是否安装成功

鼠标右键显示如图则安装成功

> 注：后续安装hexo操作都是在Git Bash Here里面进行

![](https://img.imgdb.cn/item/6065d73c8322e6675c03ea94.png)

进入Git Bash Here，输入git --version可以查看git版本

```bash
git --version
```



## 安装Node.JS



### 1、Node.js下载&安装

官网下载即可，直接下一步，然后完成（[下载官网直通车](https://nodejs.org/en/download/)）

> 电脑是32位的下载32-bit，反之64-bit（下载.msi）

![](https://img.imgdb.cn/item/6065d27f8322e6675cfe9731.png)



### 2、验证Node.js是否安装成功

打开Git Bash Here，输入node -v，显示版本号表示安装成功

```bash
node -v && npm -v
```

> 建议安装好了node.js后切换npm为淘宝源

临时使用

```bash
npm --registry https://registry.npm.taobao.org
```

全局使用

```bash
npm config set registry https://registry.npm.taobao.org
```

