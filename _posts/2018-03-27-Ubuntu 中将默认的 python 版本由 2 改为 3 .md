---
title: Ubuntu 中将默认的 python 版本由 2 改为 3 
category: skills
---
参考链接: [https://www.jianshu.com/p/9d3033d1b26f](https://www.jianshu.com/p/9d3033d1b26f)
<!-- more -->

现在的Ubuntu 中在终端中输入``python``，进入的是python 2的交互环境，输入``python3``进入的是python 3 交互环境。这里是我找到的解决办法：

环境：VirtualBox， Ubuntu 17.10.1

我用到的命令：

    rm /usr/bin/python
    ln -s /usr/bin/python3.6 /usr/bin/python


注：原博``usr``拼错

### 重要提示：删除python 2 可能会导致Ubuntu默认的输入法无法使用。

