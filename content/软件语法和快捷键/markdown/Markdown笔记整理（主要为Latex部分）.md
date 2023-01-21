**写在前面：使用了Typora之后，它的排版看起来很舒服，特别是英文的字体，而且支持latex格式的公式，真的很推荐理科生使用。但是我也没有看到很详细的技术文档，在知乎，CSDN和简书上也看到了很多的介绍，但是也不是很详细，有的还是不是特别好找。再此我也写下一些我自己的使用下来的notes。如有错误，欢迎指出，同时也欢迎大家补充。** 

**1\. 行间公式对齐**

latex里面有'&' 对齐，但是我没怎么用过latex，使用时还要导入很多包，这也是markdown的好处一直，简洁方便。

'&'对齐有两行语法，不需要导入包。'&'放在需要对齐位置之前就好了

```cpp
\begin{equation}
\begin{aligned}
&f(x,y)\\
&f(x,y,z)\\
&f(x,y,z,t)\\
&f(x,y,x,t,\lambda)
\end{aligned}
\end{equation}

```

![](https://pic2.zhimg.com/v2-e5aac6c2b33755a4c994af348b4e82d5_b.jpg)

行间公式对齐

**2\. 单括号**

\\text{if it is odd}也是公式中的文字格式。

```text
f(n)=
	\begin{cases}
		n/2, & \text{if $n$ is even}\\
		3n+1,& \text{if $n$ is odd}
	\end{cases}
```

![](https://pic3.zhimg.com/v2-0c0697b173c22c684c0b068615b11782_b.jpg)

单括号

**3\. 公式中的黑体**

公式黑体和latex中有一点点不一样, \\mathbf{P}为黑体P。但是这样的黑体不是数学斜体，这个还没有找到比较好的解决方法。

![](https://pic3.zhimg.com/v2-22b253c4105a3c454d0c6fa23cfa8c72_b.jpg)