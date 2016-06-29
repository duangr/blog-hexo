---
title: sshpass的安装使用
date: 2016-06-28 14:24:00
tags:
- ssh
---
# 前言
用的是mac电脑，喜欢用iTerm访问远程终端。由于不同的终端用户名和密码不同，想在执行`ssh`命令远程登录时直接将用户名、密码、IP地址在一个命令中输入完成，避免交互式输入带来的不便。
网上搜索类似解决方案，找到`sshpass`。下面介绍下`sshpass`的安装使用。

# 功能场景
通过`sshpass`+`ssh`，在一次命令中将用户名、密码、IP地址全部输入，完成登录远程主机的操作。

# 安装使用
## 下载
http://sourceforge.net/projects/sshpass/files/

比如我下载版本： sshpass-1.05.tar.gz
## 安装
解压
```
tar -xvf sshpass-1.05.tar.gz
```
编译安装
```
./configure
make
make install
```
验证
```
sshpass -h
```
# 应用案例
```
sshpass -p "${passwd}" ssh ${user}@${host}
```

# 参考资料
