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

![我的手工花](http://xiooix.oss-cn-hangzhou.aliyuncs.com/img/learn_20170910_pic1.jpg)

我还想送贺卡给老师，于是我让爸爸教我用scratch做会动的贺卡。

贺卡最终是这样子的，后面有说明是怎么一步一步做出来的。

<iframe allowtransparency="true" width="485" height="402" src="//scratch.mit.edu/projects/embed/173550969/?autostart=false" frameborder="0" allowfullscreen></iframe>

### 设计

我梦想中的贺卡的样子应该有音乐，有动画，还有我的祝福语，充满浓浓爱意。我和爸爸找了很多贺卡的图片做参考，最后选择了爱心从礼盒飞出这个动画效果（见下图）。

![参考效果图](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1504942633513&di=615c8c069b84b08ab3ac29377ea58e35&imgtype=0&src=http%3A%2F%2Fimg02.tooopen.com%2Fimages%2F20140121%2Fsy_54605983789.jpg)

贺卡中的元素如下：

* 背景
* 礼盒
* 字母（拼写Happy Teachers' Day)
* 心心

交互过程如下：

1. 点击绿旗后屏幕上只有背景和礼盒，礼盒有动画吸引人点击；
2. 点击礼盒后，礼盒打开
3. HAPPY TEACHERS DAY从天而降，同时礼盒里飞出心心

设计完成，接下来就是去准备素材啦～～

### 准备

Scratch里自带了好多素材，先从Scratch自带的素材库中找找看。

从**背景库**中，我选择了**hearts2**做背景
![](http://xiooix.oss-cn-hangzhou.aliyuncs.com/img/teachersday_p1.jpg)

我发现Scratch角色库中有好多的**心**，心心的素材也解决了。
![](http://xiooix.oss-cn-hangzhou.aliyuncs.com/img/teachersday_p2.jpg)

字母简单，我知道Scratch自带字母素材，导入我想要的字母（HAPPY TEACHERS DAY）。

就剩礼盒了。Scratch素材库中没有，我请求爸爸帮忙。爸爸帮我找到一个符合要求的礼盒，还是会动的gif图。太棒了！这样不仅礼盒素材有了，而且还能做打开礼盒的动画了！

### 实现动画

我设计的贺卡是要会动的，所以要实现大量动画效果。根据我的设计，贺卡中会动的元素有：

* 礼盒动画（吸引人打开）
* 礼盒大开动画
* HAPPY TEACHERS DAY飞入动画
* 心心向上飞动画

这些动画实现的方式和思路都不同，下面逐个说一下。

##### 礼盒膨胀动画

礼盒打开前，我希望做一个动画吸引人点击。因为只有点击礼盒，后面的动画才会触发。

礼盒动画我希望做出一种礼盒中有很多的东西准备爆出来的感觉。Scratch中的**鱼眼**特效可以给图片加上一种放大镜放大的效果，基本可以实现我想要的爆出来的感觉。只要循环不断膨胀--还原--膨胀--还原 ………… 直到礼盒被点击。

<pre class='blocks'>
repeat until < (running)=[0]> // 用变量running控制是否还播放动画
	set [fisheye v] effect to [50]
	wait [1] secs
	set [fisheye v] effect to [0]
	wait [1] secs
end
</pre>

##### 礼盒打开动画

##### 文字飞入

##### 粒子效果

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
end
</pre>

