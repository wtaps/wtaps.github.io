---
layout: post
title: "python虚拟环境virtualenv"
description: ""
category: "python"
tags: [python]
---

python虚拟环境工具virtualenv

## 介绍
virtualenv 用来创建隔离的Python环境。比如你想装Django1.4和1.6两个版本，但想2个版本互不影响，就用到这个工具了。

## 安装
直接使用pip安装
{% highlight bash %}
$ sudo pip install virtualenv
{% endhighlight %}

## 选项
{% highlight bash %}
$ virtualenv --help
选项:
--version 显示当前版本号。
-h, --help 显示帮助信息。
-v, --verbose 显示详细信息。
-q, --quiet 不显示详细信息。
-p PYTHON_EXE, --python=PYTHON_EXE 指定所用的python解析器的版本，比如 --python=python2.5 就使用2.5版本的解析器创建新的隔离环境。 默认使用的是当前系统安装(/usr/bin/python)的python解析器
--clear 清空非root用户的安装，并重头开始创建隔离环境。
--no-site-packages 令隔离环境不能访问系统全局的site-packages目录。
--system-site-packages 令隔离环境可以访问系统全局的site-packages目录。
--unzip-setuptools 安装时解压Setuptools或Distribute
--relocatable 重定位某个已存在的隔离环境。使用该选项将修正脚本并令所有.pth文件使用相当路径。
--distribute 使用Distribute代替Setuptools，也可设置环境变量VIRTUALENV_DISTRIBUTE达到同样效要。
--extra-search-dir=SEARCH_DIRS 用于查找setuptools/distribute/pip发布包的目录。可以添加任意数量的–extra-search-dir路径。
--never-download 禁止从网上下载任何数据。此时，如果在本地搜索发布包失败，virtualenv就会报错。
--prompt==PROMPT 定义隔离环境的命令行前缀。
{% endhighlight %}

## 建立虚拟环境
{% highlight bash %}
$ virtualenv .env # 建立名为.env的虚拟环境
$ source .env/bin/activate # 启动该虚拟环境
(.env)
$ deactivate      # 推出虚拟环境

$ virtualenv .env3 --python=python3.2 # 建立python版本为3.2的虚拟环境

{% endhighlight %}

先研究这么多，等用的深了再补充。
