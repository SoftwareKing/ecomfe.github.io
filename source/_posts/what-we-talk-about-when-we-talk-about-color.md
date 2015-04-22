title: 当我们谈论颜色时，我们在谈论什么
date: 2015-4-22
author: Firede
author_link: http://weibo.com/firede
tags:
- color
- 前端设计感
- 用户体验
---

前端工程师想到颜色时，首先想起的便是基于 RGB 模型的 16 进制颜色代码，这也是我们工作中最常用到的 **数值表示** 方式。

但是，我们谈起颜色时，可能会遇到这样的场景：

> 设计：「这里用牡丹色，再稍微调亮一些。」  
> 前端：「……」（你™在说什么！）

这时你应该去向设计小伙伴要最熟悉的 16 进制颜色代码了，但“语言不通”的挫折感还是有一点的。  
小伙伴觉得你没有 **设计感**，你觉得小伙伴不够严谨。

想要愉快的交流下去，就得补点儿颜色方面的知识了，先复习一下基础。

## 基本原理

我们在中学的 **物理** 课上学过，颜色本质上是特定范围的 [电磁波](http://zh.wikipedia.org/wiki/电磁波)（如下图[^1]）。

[^1]: 可见光谱在电磁波中的范围，原作者：[Philip Ronan](http://en.wikipedia.org/wiki/File:EM_spectrum.svg)

![我们看到的色彩，是电磁波谱的一小部分](/blog/what-we-talk-about-when-we-talk-about-color/spectrum.png)

但从 **生理** 来看，人们能看到颜色，是因为人类每只眼球视网膜大约有 600-700 万的 [视锥细胞](http://en.wikipedia.org/wiki/Cone_cell)，他们是处理可见光谱颜色的 **感光器**[^2]。
人类的视锥细胞有三种，分别是 **短波（S 或蓝色）视锥细胞**、**中波（M 或绿色）视锥细胞**、**长波（L 或红色）视锥细胞**；这些视锥细胞响应的组合，让我们能够分辨出大约一千万种颜色。

[^2]: 视细胞中还有一种 [视杆细胞](http://en.wikipedia.org/wiki/Rod_cell)，他们在黑暗条件下比较敏感，但几乎不参与对颜色的处理。

所以，我们常说的 **原色** 其实是个生物学的概念，是由人类的生理特征决定的。

---

以 **反射光源** 或 **颜料着色** 时使用的色彩，属于 **消减型** 的原色系统。

我们身边的物体大多数都无法自行发光，必须借助光源的 **反射** 才能被看见。
当光源照射物体时，对物体而言，可分为被吸收的波长与反射的波长，反射后的波长即是我们所看到的颜色。

CMYK（印刷四分色模式）是彩色印刷时采用的一种套色模式，它利用色料的 **减色混合法** 原理，加上黑色油墨[^3]，共计四种颜色叠加，形成所谓 **全彩印刷**。
四种标准颜色是 **青色（Cyan）**、**品红色（Magenta）**、**黄色（Yellow）** 和 **黑色（blacK）**。

[^3]: 理论上只用上述三种颜色能够混合成黑色，但实际印刷时三种颜色的相加只能形成一种深灰色或深褐色。

![消减型原色系统](/blog/what-we-talk-about-when-we-talk-about-color/subtractive-primaries.png)

对前端来说，我们的主要产出是用各种屏幕来展示的，上面那些和我们关系不大，了解即可。

---

以 **光源投射** 时使用的色彩，属于 **叠加型** 的原色系统。

此系统中包含了 **红**、**绿**、**蓝** 三种原色，使用这三种原色可以产生其他颜色，例如红色与绿色混合可以产生黄色或橙色，绿色与蓝色混合可以产生青色，蓝色与红色混合可以产生紫色或品红色。
当这三种原色以等比例叠加在一起时，会变成灰色；若将此三原色的强度均调至最大并且等量重叠时，则会呈现白色。这套原色系统常被称为「RGB 色彩空间」。[^4]

[^4]: 原色（维基百科）：<http://zh.wikipedia.org/wiki/原色>

![叠加型原色系统](/blog/what-we-talk-about-when-we-talk-about-color/additive-primaries.png)

电视、显示器、手机屏幕都是基于 **RGB 色彩模型** 来运转的，所以我们用 **RGB** 来表述颜色是最贴近硬件的方式。

很显然，作为前端的你已经非常熟悉 RGB 了；你经常通过调整 `#RRGGBB` 中代表 红、绿、蓝 的值，调整设计细节；
你看到一个颜色的 HEX 代码就能够想象出它偏向哪种色彩，颜色是深是浅。但是，如果设计小伙伴对你说：

> 这里 hover 时，把背景的 **亮度** 提高百分之十五就好啦。

这时你 **像显示器一样思考** 的 **RGB 调整术** 可能就算不过来了。我们需要了解一些符合 **人类思考方式** 的色彩空间。

## HSB

## HSL

## HUSL

## 书目

以下是写这篇博客时主要参考的书目，以及我根据主观印象给的评分，供参考。

* [黑客与设计：剖析设计之美的秘密](http://dwz.cn/hacker-design)，评分：★★★★★，作者：[美] David Kadavy，ISBN：9787115345370
* [色彩设计的原理](http://dwz.cn/color-design)，评分：★★★★★，作者：[日] 伊达千代，ISBN：9787508629902
* [色彩构成](http://dwz.cn/interaction-of-color)，评分：★★★★☆，作者：[美] Josef Albers，ISBN：9787562463450
* [配色设计原理](http://dwz.cn/color-schemes)，评分：★★★☆☆，作者：[日] 奥博斯科编辑部，ISBN：9787500690351