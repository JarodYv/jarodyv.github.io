---
layout: blog
learn: true
title:  "用Scratch制作教师节贺卡，祝老师教师节快乐！"
background: #ffc0cb
background-image: http://xiooix.oss-cn-hangzhou.aliyuncs.com/img/teachersday.png
date:   2017-09-10 23:13:54
category: 我学
tags:
- scratch
- 编程
- 教师节 
---

9月10号是一年一度的教师节，我要为老师送上一份特别的礼物。送什么好呢？

我想送花给老师，于是妈妈教我做手工花。

![](http://xiooix.oss-cn-hangzhou.aliyuncs.com/img/learn_20170910_pic1.jpg)

我还想送贺卡给老师，于是我让爸爸教我用scratch做会动的贺卡。

贺卡最终是这样子的

<iframe allowtransparency="true" width="485" height="402" src="//scratch.mit.edu/projects/embed/173550969/?autostart=false" frameborder="0" allowfullscreen></iframe>

你可以点击[这里](https://scratch.mit.edu/projects/173550969/)查看整个工程的源代码。

```blocks
when green flag clicked
forever
   turn cw (15) degrees
   say [Hello!] for (2) secs
   if <mouse down?> then
      change [mouse clicks v] by (1)
   end
</scratchblocks>
```

