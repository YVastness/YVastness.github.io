> Vimium是效率与装逼兼具，极客上网的不二选择, 当你能熟练的使用时，你就会对他爱不释手，我也是用熟练之后才发现是vimium如此的好用和舒服.
> 接下来我就介绍一下Vimium的基本用法以及自己自定义的一下心得，方便小白快速入门

## 首先

![img](https://upload-images.jianshu.io/upload_images/3026741-b90a7a5de603772f.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

## Vimium是什么

Vimium是Vim和 Chromium的结合，Vim是linux中让你脱离鼠标编辑文本的利器，同样Vimium是让你脱离鼠标就能上网的终极利器，你不用移动鼠标就能跳转页面，切换标签，打开历史记录，打开书签等等，这比传统的鼠键结合的方式要快得多，就拿百度一个问题来说，我们首先要输入一个问题这个时候我们用到了键盘，然后聪明一点的会直接按下回车，笨一点的右手拿起鼠标点击搜索，搜索结果出来了，我们要用鼠标来回移动点击想要的连接，发现问题问的不对，我们又点击输入框，又切换回键盘输入问题。。。。这样鼠标键盘的来回切换花费了我们大量的时间，对于想要高效工作学习的人是难以忍受的。
而用上Vimium之后你只需要输入问题，回车，按F，输入链接对应的编号,修改问题?一样输入输入框对应的编号，立马回到输入框.整个过程完全不用鼠标的切换,就是这么优雅而酷炫

![img](https://upload-images.jianshu.io/upload_images/3026741-f1bf005b132102f2.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

## 听起来Vimium很难?

似乎Vimium是很强大的工具，很多人就开始望而却步了，感觉似乎不是一个很容易上手的东西，那我们换种方式来说，Vimium其实可以理解成一种快捷键配置，用过鼠标手势的应该都知道，鼠标手势其实就是把你鼠标的某一种轨迹对应一种浏览器的操作，从而执行，VImium也是一样的，但是Vimium的功能强大所以快捷键更多。但是不用担心，人们只关心自己常用的，所以从常用的入手， 一点点操作就完全没有问题。Vimium还有一个问题，就是它初始化的快捷键设置太过反人类，我会带着你边介绍边一点一点的修改初始快捷，让你熟悉他，他也熟悉你，这就完美了。

## Vimium设置界面

在你点击添加到Chrome之后你的浏览器右上角就会出现一个蓝色的V,这就是我们今天的主角了，鼠标一上去，右键选项，就进入设置界面了,在这里我们只关注第二个框框，即自定义用户快捷键的输入框，点击Show avaliable commands可以看到现在的快捷键列表，然后我们开始调教我们的Vimium吧

![img](https://upload-images.jianshu.io/upload_images/3026741-ef0580257bbb908d.png?imageMogr2/auto-orient/strip|imageView2/2/w/350/format/webp)

Vimium

![img](https://upload-images.jianshu.io/upload_images/3026741-b5c9ea8537d8001e.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

## 快捷键对照表

![img](https://upload-images.jianshu.io/upload_images/3026741-1eab85b4bf911885.png?imageMogr2/auto-orient/strip|imageView2/2/w/1054/format/webp)

这个可以先不管，只用知道第一个是快捷键，第二个是快捷键介绍，括号中是自定义代码就行了,跟着我往下走

## 最基础的操作-上下左右 -w/s/a/d

我们在上网的时候最常见的操作就是滚动滚轮，上下移动界面以及滚动条左右移动界面,在初始化的操作中被设定为jkhl，对于我来说这是很不科学的操作，因为玩游戏玩的多的都知道上下左右是wsad，所以！改!

```
map w scrollUp
map s scrollDown
map a scrollLeft
map d scrollRight
```

在编辑框输入这四行代码,表示让w对应向上滚动，s对应向下滚动,a向左滚，d向右滚...从快捷键对照表括号中知道对应的快捷键代码就能修改相应的快捷键。很容易理解对吗?下面的代码都表示在上述的自定义编辑框中添加的内容，修改完成记得点击最下面的**save changes**

### 半页滚动-h/l

以上的滚动都只是细微的滚动，我们要快速浏览的时候一般都是滚动半页,对应修改scrollPageDown和scrollpageUp,我个人的喜好是h上滚半页,l下滚半页



```cpp
map l scrollPageDown
map h scrollPageUp
```

### 回到顶部/底部-qq/ee

为了方便直接回到最上面和最下面我们还要对这两个快捷键进行设置，我们的左手边现在还有q和e比较空闲，所以我们可以把q设为回到顶部e回到底部，但是后来发现这样我很容易按错.一旦不小心按到q就会回到顶部,这样会降低效率所以我把回到顶部设为qq，也就是要按两次q才能回到顶部，相当于给我们一个确认的机会，同理，回到底部设为ee



```cpp
map qq scrollToTop
map ee scrollToBottom
```

## 后退/前进-j/k

我们经常会用到后退和前进每次都要在左上角点击实在太麻烦，所以我把两个操作放到了右手边j和k,按j后退，按k前进,这样两个键就可以进退自如了,



```cpp
map j goBack
map k goForward
```

这样子定义的基本上都修改完了，还有一些操作我觉得位置还算合理，没有修改的必要

## 终极跳转链接大法-f

vim大杀器，让你不用鼠标就能跳转各种页面，只需要按下f所有的链接都会被标记出来，连接旁边会有黄色的卡片，卡片上写着英文，输入这个英文就能跳转了，需要注意的是**如果输入的是小写的英文则会在当前标签打开，原来的标签会消失，想要打开新的标签页要输入大写的英文，即按住shift再输入**.

*你也可以直接按大写F，这时候都是打开新标签页的操作*

![img](https://upload-images.jianshu.io/upload_images/3026741-d919438aaf737593.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

## 跳转标签页-J/K

之前我们用小写j和k进行前进和后退，为了尽量不移动手指(就是这么懒), 我们直接用大写J和K来跳转标签页，J向前跳，K向后跳，再也不用一直ctrl+tab了

## 关闭页面/恢复页面 - x/X

关闭当前页面不用再移动鼠标到上面了，只需要按下x，这个页面就over了，就和玩街机一样爽快，什么？不小心关了？大写X，一键回档。

## 终极搜索栏 - o

o是打开新世界的大门，在这里你可以**搜索历史记录，搜索书签，还可以直接打开一个新的网址(或者直接百度谷歌搜索,依赖你的设置的搜索引擎)**,简直不要太方便,虽然chrome的地址栏也可以搜索，但是第一需要手动去点，第二显示出来没有Vimium好看

> 小写o是在当前标签页打开，大写O是在新标签页打开

![img](https://upload-images.jianshu.io/upload_images/3026741-990da9527414476d.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

## 搜索书签 - b

如果你只是想搜索书签，那么一个b就可以了

> 大小写区别同上

![img](https://upload-images.jianshu.io/upload_images/3026741-c91badd41ffb4ec8.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

## 刷新页面 - r

按r刷新界面
是不是比f5要近一点呢，没错，一点懒都要偷

## 页面搜索 - /

相当于ctrl+f的搜索，常用程度一般: )

## 总结

走完上面的流程你会发现基本大部分的浏览器操作都已经有了自己的新快捷键，而且以我的方式自定义你可以操作起来和打拳皇，lf2一样的简单，两手只用放在该放的位置不动就能进行几乎所有的操作，当然还有一些操作是没法替代的，比如玩游戏等等。但是在日常的搜索，阅读，你会发现熟练之后效率奇快而且逼格极高，别人还没看到鼠标动就切换到了下一个页面，当然vimium的极限不止于此，还有很多黑科技，大家自己去探索吧