不想看文章的可以看视频：

今天继续分享一下使用 Typora 在画图方面的小技巧。是的，你没看错，Typora 也能”画“图。

说是画图，但并不像其他专业的绘图软件那样，通过拖拖拽拽一些元素，画出流程图、时序图等。Typora 的制图功能是由 Mermaid 强力驱动，如果你使用过 PlantUML，那么 Mermaid 也非常容易上手。

### **Mermaid**

**Mermaid\[1\]** 是一种简单的类似 Markdown 的脚本语言，通过 JavaScript 编程语言，将文本转换为图片。因此，真正实现画图功能的并不是 Typora 本身，它只是内置了对 Mermaid 的支持。

![](https://pic2.zhimg.com/v2-4e44a08fa37bdb6b03df9fcec8480ed9_b.jpg)

Mermaid 支持绘制非常多种类的图，常见的有时序图、流程图、类图、甘特图等等。下面分享一下如何绘制这些图，语法非常容易掌握。

先在 Typora 中，输入 **\`\`\`mermaid** 然后敲击回车，即可初始化一张空白图。

### **流程图**

语法解释：`graph` 关键字就是声明一张流程图，`TD` 表示的是方向，这里的含义是 Top-Down 由上至下。

```text
graph TD;
    A-->B;
    A-->C;
    B-->D;
```

![](https://pic4.zhimg.com/v2-d4e7402e1dce5cefb924776e01b0bffb_b.jpg)

### **时序图**

语法解释：`->>` 代表实线箭头，`-->>` 则代表虚线。

```text
sequenceDiagram
    Alice->>John: Hello John, how are you?
    John-->>Alice: Great!
```

![](https://pic3.zhimg.com/v2-decde80f8f46a4a5399f20c55bb4b00a_b.jpg)

### **状态图**

语法解释：`[*]` 表示开始或者结束，如果在箭头右边则表示结束。

```text
stateDiagram
    [*] --> s1
    s1 --> [*]
```

![](https://pic1.zhimg.com/v2-b33193d8007a927648f169cf075864a8_b.jpg)

### **类图**

语法解释：`<|--` 表示继承，`+` 表示 `public`，`-` 表示 `private`，学过 Java 的应该都知道。

```text
classDiagram
      Animal <|-- Duck
      Animal <|-- Fish
      Animal <|-- Zebra
      Animal : +int age
      Animal : +String gender
      Animal: +isMammal()
      Animal: +mate()
      class Duck{
          +String beakColor
          +swim()
          +quack()
      }
      class Fish{
          -int sizeInFeet
          -canEat()
      }
      class Zebra{
          +bool is_wild
          +run()
      }
```

![](https://pic1.zhimg.com/v2-b6da49f44aee84e63186d91de51596d4_b.jpg)

### **甘特图**

甘特图一般用来表示项目的计划排期，目前在工作中经常会用到。

语法也非常简单，从上到下依次是图片标题、日期格式、项目、项目细分的任务。

```text
gantt
    title 工作计划
    dateFormat  YYYY-MM-DD
    section Section
    A task           :a1, 2020-01-01, 30d
    Another task     :after a1  , 20d
    section Another
    Task in sec      :2020-01-12  , 12d
    another task      : 24d
```

![](https://pic3.zhimg.com/v2-4e8a1f1d33213f64fd0eb3779b1e6ad2_b.jpg)

### **饼图**

饼图使用 `pie` 表示，标题下面分别是区域名称及其百分比。

```text
pie
    title Key elements in Product X
    "Calcium" : 42.96
    "Potassium" : 50.05
    "Magnesium" : 10.01
    "Iron" :  5
```

![](https://pic3.zhimg.com/v2-804c453be09ada35d3257f1601c19d5a_b.jpg)

### **导出**

绘制好的图片可以选择菜单/文件/导出，导出为图片或者网页格式。在网页中图片是以 SVG 格式渲染的，你可以复制 SVG 内容，导入到 SVG 的图片编辑器中进一步操作。

![](https://pic2.zhimg.com/v2-907aef8d603e125c85d2a14ed96a9e79_b.jpg)

Mermaid 官方有一个在线的工具，可以导出 SVG 和 PNG。

[Mermaid live editor​mermaid-js.github.io](https://link.zhihu.com/?target=https%3A//mermaid-js.github.io/mermaid-live-editor)

**小结**

可以看到，Mermaid 使用非常简洁优雅的语法，让使用者可以快速地画出常用的图形，并且图片的非常美观，配色和谐，富有现代感。这个 Typora 画图的功能，你学会了吗？

我还写过关于 Typora 的一些使用小技巧，欢迎阅读

[https://zhuanlan.zhihu.com/p/163608242​zhuanlan.zhihu.com![](https://pic2.zhimg.com/v2-dd83e053fd151d52053e2a73dcad956d_ipico.jpg)
](https://zhuanlan.zhihu.com/p/163608242)

有人在评论区提到了「语雀」，我也写了一篇文章。和 Typora 相比，语雀具有更强大的在线编辑器，同样也支持 Mermaid 语法进行制图，对各种文档附件支持程度极高。

[https://zhuanlan.zhihu.com/p/220504919​zhuanlan.zhihu.com![](https://pic1.zhimg.com/v2-8d56c8e032e9d9e660e4f3c3ac7a8094_ipico.jpg)
](https://zhuanlan.zhihu.com/p/220504919)

### **参考资料**

\[1\]

Mermaid: [https://mermaid-js.github.io/mermaid/#/](https://link.zhihu.com/?target=https%3A//mermaid-js.github.io/mermaid/%23/) 
 [https://zhuanlan.zhihu.com/p/172635547](https://zhuanlan.zhihu.com/p/172635547)