---
title: Ubuntu 安装最新版 Sublime Text 
category: 笔记
---
及没有找到有效的OpenPGP解决办法
参考链接：[https://www.sublimetext.com/docs/3/linux_repositories.html](https://www.sublimetext.com/docs/3/linux_repositories.html)
<!-- more -->

使用如下方法可以顺利安装，但是打开会提示更新，因此这种方法获得的不是最新版：

	sudo add-apt-repository ppa:webupd8team/sublime-text-3
	sudo apt-get update
	sudo apt-get install sublime-text-installer
	sudo apt-get install sublime-text

###安装最新版SublimeText方法（目前版本3143）：


	wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
	（不成功的话https改为http，-qO - ，这里O是大写）

	sudo apt-get install apt-transport-https

	二选一，稳定版、开发版
    echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
    echo "deb https://download.sublimetext.com/ apt/dev/" | sudo tee /etc/apt/sources.list.d/sublime-text.list

	sudo apt-get update
	sudo apt-get install sublime-text

<br><br><br>

###gpg: 找不到有效的 OpenPGP 数据
第一步时总是出现错误，提示：

	gpg: 找不到有效的 OpenPGP 数据。

Google了好多办法似乎都没有什么用，忘了看了哪里的方法，试了：
	
	wget https://download.sublimetext.com/sublimehq-pub.gpg
提示:
	
	无法建立SSL连接

于是尝试改为http：
	
	wget http://download.sublimetext.com/sublimehq-pub.gpg
成功！
