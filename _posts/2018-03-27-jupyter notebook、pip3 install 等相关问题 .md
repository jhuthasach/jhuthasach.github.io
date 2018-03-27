---
title: jupyter notebook、pip3 install 等相关问题
category: skills
---
<!-- more -->

环境：Ubuntu 17.10.1

## python 2 和 python 3 环境安装通过pip安装时命令是不一样的:
参考链接1：[https://www.jupyter.org/install](https://www.jupyter.org/install)

参考链接2：[https://www.exegetic.biz/blog/2017/06/setting-up-jupyter-ubuntu-xenial/](https://www.exegetic.biz/blog/2017/06/setting-up-jupyter-ubuntu-xenial/)

Python 3 (官方推荐):

    python3 -m pip install --upgrade pip
    python3 -m pip install jupyter

Python 2 :

    python -m pip install --upgrade pip
    python -m pip install jupyter
    
最后测试是否成功:

    jupyter notebook

## 运行 jupyter notebook 时出现 No such file or directory 错误：
参考链接：[https://stackoverflow.com/questions/42648610/error-when-executing-jupyter-notebook-no-such-file-or-directory](https://stackoverflow.com/questions/42648610/error-when-executing-jupyter-notebook-no-such-file-or-directory)

Python 3

	sudo pip3 install --upgrade --force-reinstall --no-cache-dir jupyter
    你可以直接尝试一下这条命令安装试试，我是折腾了半天最后用这条命令解决的。
    
Python 2

	sudo pip install --upgrade --force-reinstall --no-cache-dir jupyter


	
    