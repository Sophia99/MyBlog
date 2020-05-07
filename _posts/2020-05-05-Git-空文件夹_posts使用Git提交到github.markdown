---
layout: post
title:  "git管理空文件，上传远程时会忽略掉空文件"
date:   2020-05-05 15:54:58 +0800
categories: git
---

## git管理空文件，上传远程时会忽略掉空文件
**背景**：2020年，我决定自己写博客；在自己使用别人的*github* 博客模板时，因为全删了*posts* 文件夹里的文章，更新本地分支到远程*github*时，*posts*文件夹没有了。


**解决方法**：在*google* 上，搜索得知，没有*posts* 文件夹的原因就是*Git* 会忽略掉空的文件夹。具体的操作如下：

    cd _posts   #回到空文件夹
    touch .gitkeep	#.gitkeep相当于一个占位符来追踪空的文件夹
	git add .
	git commit -m "add a new file"
	git push github


至此，*posts* 文件夹就出现了，解决了*git* 忽略空文件夹的上传问题。

