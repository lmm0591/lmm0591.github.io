---
title: brew 简介
date: 2018-09-20 23:34:28
tags:
- Mac
---

## 一、简介

brew 是一个软件包管理工具,类似于 centos 下的 yum 或者 ubuntu 下的 apt-get,非常方便,免去了自己手动编译安装的不便

- brew 安装目录 /usr/local/Cellar
- brew 配置目录 /usr/local/etc
- brew 命令目录 /usr/local/bin (注:homebrew在安装完成后自动在/usr/local/bin加个软连接，所以平常都是用这个路径)

## 二、安装

```shell
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" 
```

## 三、常用命令

```shell
brew  install mysql  //安装mysql

brew search mysql  //搜索mysql

brew info mysql    //   查找mysql相关信息

brew update     //更新自己的Homebrew

brew outdated   //会显示哪些软件可以升级

brew upgrade     //升级所有软件（后面不加名字）

brew upgrade  mysql  //    升级mysql软件

brew list      //显示已经安装的软件

brew uninstall xx //卸载某些软件

brew cleanup    //定期清理一些安装包缓存

```

## 四、brew cask 的常用命令

安装完 brew 时，brew-cask 已经安装好了，无需自行安装。

```shell
brew cask search # 列出所有可以被安装的软件
brew cask search name # 查找所有和 name相关的应用
brew cask install name # 下载安装软件
brew cask uninstall name # 卸载软件
brew cask info app # 列出应用的信息
brew cask list # 列出本机按照过的软件列表
brew cask cleanup # 清除下载的缓存以及各种链接信息
```

## 五、更新 brew cask 及通过 brew-cask 安装的程序

```shell
brew update && brew upgrade brew-cask #更新cask自身
brew cask uninstall name && brew cask install name ＃更新程序
```

## 六、常用软件

```shell
brew cask install launchrocket #非常友好的 brew 服务 图形界面
```