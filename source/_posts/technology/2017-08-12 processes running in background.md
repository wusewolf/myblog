---
layout: post
title:  让进程在后台可靠运行的几种方法       
date:   2017-08-12 14:55:11
category: "技术"
tags: "Linux tips" 
---

** 让进程在后台可靠运行的几种方法---总结 **

## nohup/setsid/&   
1. nohup ping www.ibm.com &
2. setsid ping www.ibm.com
3. (ping www.ibm.com &) 

## disown对已经运行的进程来控制
- 用disown -h jobspec来使某个作业忽略HUP信号。  
- 用disown -ah 来使所有的作业都忽略HUP信号。   
- 用disown -rh 来使正在运行的作业忽略HUP信号。

## 参考链接[Linux 技巧：让进程在后台可靠运行的几种方法](https://www.ibm.com/developerworks/cn/linux/l-cn-nohup/)