---
title: 关于 /etc/hosts 文件
date: 2018-09-20 13:10:41
tags:
- Mac

---

## 主机名 ip 配置文件

hosts---The static table lookup for host name(主机名查询静态表)

linux 的 /etc/hosts 是配置 ip 地址和其对应主机名的文件，不同的linux版本，这个配置文件也可能不同。比如 Debian 的对应文件时 /etc/hostname。

## 配置文件的用途

这个文件可以配置主机 IP 及其对应的主机名，可以减少 DNS 查询，节省时间，

linux 主机名的相关配置文件就是 /etc/hosts 这个文件告诉主机那些域名对应那些ip

比如文件中有这样的定义

```shell
192.168.1.100    linumu100    test100
```

假设 `192.168.1.100` 是一台网站服务器，在网页中输入 `http://linumu100` 或 `http://test1000` 就会打开 `192.168.1.100` 的网页。


## 配置文件格式说明

一般/etc/hosts的内容一般有如下类似内容：
```shell
##
# Host Database
#
# localhost is used to configure the loopback interface
# when the system is booting.  Do not change this entry.
##
127.0.0.1	localhost
255.255.255.255	broadcasthost
::1             localhost
```

一般情况下hosts文件的每行尾一个主机，每行由三部分组成，每个部分由空格隔开。

第一部分：网络IP地址；
第二部分：主机名或域名；
第三部分：主机名别名；

当然每行也可以是两部分，即主机IP地址和主机名。

主机名（hostname) 和 域名（domain)的区别：
主机名通常在局域网内使用，通过hosts文件，主机名就被解析到对应IP;
域名通常在INTERNET上使用，但如果本机不想使用internet上的域名解析，这时就可以更改hosts文件，加入自己的域名解析。

## hosts文件可以帮助解决哪些问题

- 加快域名解析
- 开发测试 mock 线上域名环境，可以充当部份 fiddler 的功能


