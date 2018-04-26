---
title: linux与genymotion模拟串口通信
date: 2018-04-26 15:51:44
categories:
- 移动开发
- android
tags:
- 串口
- 模拟
- 虚拟机
- 模拟器
- genynotion
- vm
---
# 在linux中如何模拟串口与安卓虚拟机genynotion进行通讯？

### 1、打开vm virtualbox,选中相应的虚拟机
{% asset_img 1-1.png %}

### 2、右击设置，选中串口，配置如下
{% asset_img 1-2.png %}
<!-- more -->
** 注 **
```
端口模式选为主机管道
路径/地址：/tmp/文件名随意，解决访问权限
```

### 3、在linux中 执行如下命令
{% code lang:bash %}
socat unix-connect:/tmp/mock tcp-listen:12345
{% endcode %}

** 注 **
```
/tmp/mock:为步骤2中串口路径中配置的路径
12345：为端口
```

### 4、打开telnet,模拟交互
{% code lang:bash %}
telnet 127.0.0.1 12345
{% endcode %}

** 注 **
```
12345：为步骤3中配置的端口
```
