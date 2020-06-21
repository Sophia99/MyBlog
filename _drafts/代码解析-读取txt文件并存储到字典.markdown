---
layout: post
title:  "读取txt文件并存储文件内容到字典"
date:   2020-05-08 15:54:58 +0800
categories: [Python,Code-Analysising]
---
**背景**：学习python爬虫中，遇到需要将web端获取到的headers转化为python的字典类型数据。

**前提**：在网站中，复制网站的headers参数到headers.txt文件中
【上图】

**目的**：我需要将headers.txt文件中的内容转化为字典格式。【上图】

**代码**：
	f = open(r'E:/PycharmProjects/SipderLearningProject/headers.txt','r')
	headers = {}
	for line in f.read().split('\n'):
	    name,value = line.strip().split(':',1)
	    headers[name] = value
	print(headers)

**代码解析**：

1.第一行f = open(),这是用只读的模式打开特定路径下的txt文件。open() 函数的第一个参数[r'E:/PycharmProjects/SipderLearningProject/headers.txt']的'r'表示只读打开；第二个参数'r'也表示只读。关于open() 函数的更多用法参考【上连接】。

2.第二行是定义headers这个变量

3.第三行到第五行是一个for循环和for循环体。