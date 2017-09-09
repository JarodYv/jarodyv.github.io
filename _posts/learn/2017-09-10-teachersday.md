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

贺卡最终是这样子的，后面有说明是怎么一步一步做出来的。

<iframe allowtransparency="true" width="485" height="402" src="//scratch.mit.edu/projects/embed/173550969/?autostart=false" frameborder="0" allowfullscreen></iframe>

### 设计

我梦想中的贺卡的样子应该有音乐，有动画，还有我的祝福语，充满浓浓爱意。我和爸爸找了很多贺卡的图片做参考，最后选择了爱心从礼盒飞出这个动画效果（见下图）。

![参考效果图](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1504942633513&di=615c8c069b84b08ab3ac29377ea58e35&imgtype=0&src=http%3A%2F%2Fimg02.tooopen.com%2Fimages%2F20140121%2Fsy_54605983789.jpg)

贺卡中的元素如下：

* 背景
* 礼盒
* 心心

设计完成，接下来就是去准备素材啦～～

### 准备

### 实现动画

#### 礼盒膨胀动画

#### 礼盒打开动画

#### 文字飞入

#### 粒子效果

#### 加入声音

你可以点击[这里](https://scratch.mit.edu/projects/173550969/)查看整个工程的源代码。

<pre class='blocks'>
when green flag clicked
forever
   turn cw (15) degrees
   say [Hello!] for (2) secs
   if <mouse down?> then
      change [mouse clicks v] by (1)
   end
</pre>

