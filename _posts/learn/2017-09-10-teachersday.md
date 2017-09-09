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

<iframe allowtransparency="true" width="485" height="402" src="//scratch.mit.edu/projects/embed/173822977/?autostart=false" frameborder="0" allowfullscreen></iframe>

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

#### 礼盒膨胀动画

礼盒打开前，我希望做一个动画吸引人点击。因为只有点击礼盒，后面的动画才会触发。

礼盒动画我希望做出一种礼盒中有很多的东西准备爆出来的感觉。Scratch中的**鱼眼**特效可以给图片加上一种放大镜放大的效果，基本可以实现我想要的爆出来的感觉。只要循环不断膨胀--还原--膨胀--还原 ………… 直到礼盒被点击。

<pre class='blocks'>
重复执行直到 <(running) = [0]> // 用变量running控制是否还播放动画
  将 [鱼眼 v] 特效设定为 [50]
  等待 [1] 秒
  将 [鱼眼 v] 特效设定为 [0]
  等待 [1] 秒
结束 
</pre>

> 所谓动画，是利用视觉暂留现象，在一定时间内不断变化对象的状态而产生的视觉效果。上面的动画利用循环不断改变角色图片的状态，从而实现动画效果。这种动画实现方式一般比较适合以一定规律循环重复的动画。

#### 礼盒打开动画

点击礼盒后，礼盒会打开。礼盒打开过程需要以动画形式来呈现。

> 礼盒的打开动画比较复杂，不像礼盒膨胀动画一样有规律可循。这个时候就需要使用**帧动画**来实现。

由于我们找到的礼盒素材是gif图，gif图本身就是一种帧动画。爸爸很容易得就将里面一帧一帧的图片抽取出来，然后导入到礼盒的造型中。

![](
http://xiooix.oss-cn-hangzhou.aliyuncs.com/img/teachersday_pic3.jpg)

然后利用循环每次切换一个造型，形成一帧一帧的帧动画。

<pre class='blocks'>
重复执行 [4] 次 // 重复执行4次，因为礼盒有4个动画帧
	下一个造型
	等待 [0.1] 秒 //  每帧之间等待0.1s；根据视觉暂留现象，等待0.04s效果更佳
结束
</pre>

> 帧动一般用于实现复杂的动画效果，比如人物行走、炸弹爆炸等，有UI奖每一帧画出来，然后像放电影一样逐帧播放出来。

#### 文字飞入

对于一些简单的**位移动画**， Scratch提供了模块可以简单很简单地实现。

<pre class='blocks'>
在 [?] 秒内滑行到 x:[?] y:[?]
</pre>

贺卡中文字的飞入就可以用 <code class='b'>在 [?] 秒内滑行到 x:[?] y:[?]</code> 来实现。先让文字的位置设在屏幕外，然后在1秒钟的时间内飞到屏幕指定位置。

#### 粒子效果

上面的动画实现方式是Scratch中最常用的3种动画实现方式：`循环特效`、`帧动画`、`位移动画`。这些动画方式在实现单个角色动画时很有效，但是对于实现心心飞出这种大量角色动画时，就会有点小问题--每个心的动画都是一样的，整体效果非常生硬。爸爸说：要想让心心飞的自然，需要使用**粒子系统**

> 粒子系统是计算机图形学中模拟一些特定的模糊现象的技术，比如火、雪、爆炸、烟花等由大量随机粒子构成的自然现象。

粒子系统太高深，我听不懂，所以心心飞出的效果是爸爸实现的。直接贴代码出来，大家自己去研究。总之，我的理解是**加入大量随机变量**。

<pre class='blocks'>
when I start as a clone
set [count v] to [0]
switch costume to (join [heart] (pick random [1] to [5]))
set [ghost v] effect to [0]
change size by [-20]
go to x:[0] y[-150]
wait (pick random [0] to [10]) secs
repeat until< (y position)>[180]>
	change [count v] by [1]
	change size by [2]
	change [ghost v] effect by [2]
	if <(count)>[50]> then
		set [count v] to [50]
	end
	glide [1] secs to x:((x position)+(pick random ([-30]+((count)*[-1])) to ([30]+((count)*[1])))) y:(((y position)+[20])+(pick random [5] to [15]))
end
broadcast [onemore v]
delete this clone
</pre>

### 加入声音

贺卡怎么能没有声音呢？

首先要加入背景音乐。我几乎把Scratch音频库中的音乐都听了一遍，最终选出 **odesong-b**作为背景音乐，因为这个音乐不但好听，更重要的是循环播放可以衔接上。

<pre class='blocks'>
重复执行
	播放声音 [odesong-b v] 直到播放完毕 // 注意一定要加until done，否则播不出来。为什么？自己去想。
结束
</pre>

我的祝福语要我亲自录，Scratch自带录音功能。

![](
http://xiooix.oss-cn-hangzhou.aliyuncs.com/img/teachersday_pic4.jpg)

点击我的头像就播我的祝福语

<pre class='blocks'>
当角色被点击时
播放声音 [wish v]
</pre>

### 总结

贺卡终于做完了，希望老师们都能喜欢。

这个项目主要用到了很多动画实现方法，让我很好地学习了用Scratch如何做动画。

完整的项目代码在[这里](https://scratch.mit.edu/projects/173550969/)，欢迎remix。


