
## 前言

CSS中，有很多**非布局样式**，这些样式（属性）和与布局无关，包括：

- 字体、字重、颜色、大小、行高
- 背景、边框
- 滚动、换行
- 装饰性属性（粗体、斜体、下划线）等。

这篇文章，我们来对上面的部分样式做一个回顾。

## 字体

### 字体分类

常见的字体可以分为两类：**衬线体、无衬线体**。

![](http://img.smyhvae.com/20191004_1101.png)

**1、serif（衬线体）**：在字的笔画开始、结束的地方有额外的装饰，而且笔画的粗细会有所不同。比如：宋体、楷体。

**2、sans-serif（无衬线体）**：笔划粗细基本一致，只剩下主干，造型简明有力，起源也很晚。适用于标题、广告等，识别性高。

常见的无衬线体有：

- 黑体
- 微软雅黑（Microsoft Yahei）：Windows平台默认的中文字体
- Arial：Windows平台默认的英文字体
- 苹方（PingFang SC）：Mac & iOS 平台的中文字体
- San Francisco：Mac & iOS 平台的英文字体
- [思源黑体](https://baike.baidu.com/item/%E6%80%9D%E6%BA%90%E9%BB%91%E4%BD%93/14919098)。是 Adobe 和 Google 在2014年7月联合推出的一款开源字体。

补充：

（1）海报设计、PPT不要用宋体。

（2）乔布斯

参考链接：[如何优雅的选择字体(font-family)](https://segmentfault.com/a/1190000006110417)

### 字体族

css 中的字体族可以理解成是某一类字体。常见的字体族可以分为五类：

- serif:衬线体。
- sans-serif：无衬线体。
- monospace：等宽字体。每一个字母所占的宽度是相同的。写代码的字体尽量用等宽字体。
- cursive：手写字体。比如徐静蕾手写体。
- fantasy：梦幻字体。比如一些艺术字。

这五类字体族不代表某一个具体的字体，而是当你在 css 中指定字体族的时候，就有可能在字体族中找出一种字体来显示。

![](http://img.smyhvae.com/20191004_1130.png)

参考链接：[serif，sans-serif，monospace，cursive和fantasy](http://www.ayqy.net/blog/serif%EF%BC%8Csans-serif%EF%BC%8Cmonospace%EF%BC%8Ccursive%E5%92%8Cfantasy/)

### 多字体 fallback

多字体 fallback机制：当指定的字体找不到（或者某些文字不支持这个字体）时，那就接着往后找。比如：

```css
.div1{
    font-family: "PingFang SC", "Microsoft Yahei", monospace;
}

```
上方代码的意思是：让 div1 在 Mac & iOS 平台用 苹方字体，在 Win 平台用微软雅黑字体，如果这两个字体都没有，就随便找一个等宽的字体进行渲染。

注意：

（1）写css 代码时，字体族不需要带引号。

（2）有些 Mac 用户会安装 Office 等软件，安装这些软件后，系统会顺带安装微软雅黑字体。此时，写 css 代码时，如果写成 `"Microsoft Yahei", "PingFang SC"`这种顺序，可能导致有些 Mac 用户用微软雅黑来显示字体。

### 常见的字体&文本属性

```css
	font-style: italic;	/* italic表示斜体，normal表示不倾斜*/
	font-weight: bold;  /* 字体加粗，100至900 */
    text-decoration: underline; /* 下划线 */
    cursor: pointer;  /*鼠标悬停时，光标显示为手形*/

```

`font-weight`属性：在设置字体是否加粗时，属性值既可以填写`normal`、`bold`这样的加粗字体，也可以直接填写 100至900 这样的数字。`normal`的值相当于400，`bold`的值相当于700。

### 其他

- 网络字体

- [iconfont](https://www.iconfont.cn/)

## 边框

如何用边框画一个三角形？详见《02-CSS基础/06-CSS盒模型详解》中的最后一段。

## 文字换行

- ovferflow-wrap：通用的属性。用来说明当一个不能被分开的字符串（单词）太长而不能填充其包裹盒时，为防止其溢出，浏览器是否允许这样的单词**中断换行**。

- word-break：指定了怎样在单词内断行。这里涉及到CJK（中文/日文/韩文）的文字换行。

- white-space：空白处是否换行。

上面这三个 css 属性进行组合，可以设置各种不同的属性。

当然，如果想让一段很长的文本不换行，可以直接设置`white-space: nowrap` 这一个属性即可。

## CSS Hack

- CSS Hack 的方式：不合法但可以生效的写法。

- 可以用来解决一些浏览器的兼容性问题。

- 缺点：难理解、难维护、易失效（比如浏览器升级后，hack可能会失效）。

- 替代方案：特性检测。

- 替代方案：针对性加 class


## CSS 效果

我们可以利用 CSS 实现各种效果，常见的效果属性有：

- box-shadow：盒子的阴影

- text-shadow：文本的阴影

- border-radius

- background

- clip-path


