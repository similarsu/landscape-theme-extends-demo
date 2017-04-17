---
title: hexo安装(ubuntu)
date: 2017-03-29 14:05:01
categories:
- 博客
- hexo
tags:
- hexo
- install
- ubuntu
- 安装
---
#### 1、安装{% post_link linux中安装nodejs nodejs %}
#### 2、替换为淘宝npm镜像
{% codeblock lang:bash %}
npm install -g cnpm --registry=https://registry.npm.taobao.org
{% endcodeblock %}
#### 3、安装hexo
{% codeblock lang:bash %}
cnpm install -g hexo-cli
{% endcodeblock %}
