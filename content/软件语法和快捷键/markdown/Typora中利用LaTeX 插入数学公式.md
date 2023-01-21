利用[Typora](https://www.typora.io/)进行资料总结时，遇见公式，一般的方法是剪切粘贴，但过于麻烦，因此学习利用LaTeX进行公式编辑，Typora对[Latex](https://www.latex-project.org/)进行了很好的支持，对Latex插入公式进行简单总结学习

本文内容参考https://blog.csdn.net/baidu\_38060633/article/details/79183905 在Typora上进行了实验。

LaTeX 编辑数学公式基本语法元素
------------------

数学公式有两种形式： inline 和 display

*   **inline（行间公式）**：在正文插入数学公式，用`$...$` 将公式括起来
    
*   **display(快间公式)** ：独立排列的公式，用 `$$...$$`将公式括起来，默认显示在行中间
    
*   **各类希腊字母表：** 
    
    eg: `$\alpha$`: α \\alpha α
    
    ![](https://img-blog.csdnimg.cn/20181104140244618.JPG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2hhcHB5ZGF5X2Q=,size_16,color_FFFFFF,t_70)

### 上下标、根号、省略号

*   **下标：** \_ eg: x i x\_i xi​
    
*   **上标：** ^ eg: $ x^2$
    
    注意：上下标如果多于一个字母或者符号，需要用一对{}括起来 eg： x i 1 x\_{i1} xi1​ 、 x α t x^{\\alpha t} xαt
    
*   **根号：** \\sqrt eg: 5 n \\sqrt\[n\]{5} n5 ​
    
* **省略号：** \\dots \\cdots 分别表示 … \\dots … $ \\cdots$

### 运算符

**基本预算符：**  ± \\pm ± ÷ \\div ÷

*   **求和：**  \\sum\_1^n : ∑ 1 n \\sum\_1^n ∑1n​
    
*   **积分：** \\int\_1^n: ∫ 1 n \\int\_1^n ∫1n​
    
*   \*\*极限：\*\*lim\_{x \\to \\infty} :
    
    $ lim\_{x \\to \\infty}$
    
*   **分数：** \\frac{}{} 如： 3 8 \\frac{3}{8} 83​
    
*   **矩阵与行列式**
    
    矩阵：`$$\begin{matrix}...\end{matrix}$$` ,使用&分隔同行元素，\\ 换行。eg:

```latex
$$
	\begin{matrix}
	1 & x & x^2\\
	1 & y & y^2\\
	1 & z & z^2\\
	\end{matrix}
$$

```

1 x x 2 1 y y 2 1 z z 2

1amp;xamp;x21amp;yamp;y21amp;zamp;z2

111​xyz​x2y2z2​  
​ 行列式：

```latex
$$
X=\left|
	\begin{matrix}
		x_{11} & x_{12} & \cdots & x_{1d}\\
		x_{21} & x_{22} & \cdots & x_{2d}\\
		\vdots & \vdots & \ddots & \vdots \\
		x_{11} & x_{12} & \cdots & x_{1d}\\
	\end{matrix}
\right|
$$

```

X = ∣ x 11 x 12 ⋯ x 1 d x 21 x 22 ⋯ x 2 d ⋮ ⋮ ⋱ ⋮ x 11 x 12 ⋯ x 1 d ∣ X=\\left|

x11amp;x12amp;⋯amp;x1dx21amp;x22amp;⋯amp;x2d⋮amp;⋮amp;⋱amp;⋮x11amp;x12amp;⋯amp;x1d

\\right| X\=∣∣∣∣∣∣∣∣∣​x11​x21​⋮x11​​x12​x22​⋮x12​​⋯⋯⋱⋯​x1d​x2d​⋮x1d​​∣∣∣∣∣∣∣∣∣​

*   **分隔符**

各种括号用 () \[\] { } \\langle\\rangle 等命令表示,注意花括号通常用来输入命令和环境的参数,所以在数学公式中它们前面要加 \\。可以在上述分隔符前面加 \\big \\Big \\bigg \\Bigg 等命令来调整大小。

*   **箭头**

```latex
$\leftarrow$

```

← \\leftarrow ←

![](https://img-blog.csdnimg.cn/20181104140310286.JPG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2hhcHB5ZGF5X2Q=,size_16,color_FFFFFF,t_70)

*   **方程式**
    
    ```latex
    E=mc^2
    
    ```
    
    E = m c 2 E=mc^2 E\=mc2
    
*   **分段函数**
    
    ```latex
    $$
    f(n)=
    	\begin{cases}
    		n/2, & \text{if $n$ is even}\\
    		3n+1,& \text{if $n$ is odd}
    	\end{cases}
    $$
    
    ```
    
    f ( n ) = { n / 2 , if  n  is even 3 n + 1 , if  n  is odd f(n)=
    
    {n/2,amp;if n is even3n+1,amp;if n is odd
    
    f(n)\={n/2,3n+1,​if n is evenif n is odd​
    
*   **方程组**
    
    ```latex
    $$
    \left\{
    	\begin{array}{c}
    		a_1x+b_1y+c_1z=d_1\\
    		a_2x+b_2y+c_2z=d_2\\
    		a_3x+b_3y+c_3z=d_3
    	\end{array}
    \right.
    $$
    
    ```
    
    { a 1 x + b 1 y + c 1 z = d 1 a 2 x + b 2 y + c 2 z = d 2 a 3 x + b 3 y + c 3 z = d 3 \\left\\{
    
    a1x+b1y+c1z\=d1a2x+b2y+c2z\=d2a3x+b3y+c3z\=d3
    
    \\right. ⎩⎨⎧​a1​x+b1​y+c1​z\=d1​a2​x+b2​y+c2​z\=d2​a3​x+b3​y+c3​z\=d3​​

### 常用公式

*   **线性模型**

```latex
$$
	h(\theta) = \sum_{j=0} ^n \theta_j x_j
$$

```

h ( θ ) = ∑ j = 0 n θ j x j h(\\theta) = \\sum\_{j=0} ^n \\theta\_j x\_j h(θ)\=j\=0∑n​θj​xj​

*   **均方误差**
    
    ```latex
    $$
    	J(\theta) = \frac{1}{2m}\sum_{i=0}^m(y^i - h_\theta(x^i))^2
    $$
    
    ```
    
    J ( θ ) = 1 2 m ∑ i = 0 m ( y i − h θ ( x i ) ) 2 J(\\theta) = \\frac{1}{2m}\\sum\_{i=0}^m(y^i - h\_\\theta(x^i))^2 J(θ)\=2m1​i\=0∑m​(yi−hθ​(xi))2
    
*   **求积公式**
    
    ```latex
    \$$
    	H_c=\sum_{l_1+\dots +l_p}\prod^p_{i=1} \binom{n_i}{l_i}
    \$$
    
    ```

H c = ∑ l 1 + ⋯ + l p ∏ i = 1 p ( n i l i ) H\_c=\\sum\_{l\_1+\\dots +l\_p}\\prod^p\_{i=1} \\binom{n\_i}{l\_i} Hc​\=l1​+⋯+lp​∑​i\=1∏p​(li​ni​​)

*   **批量梯度下降**
    
    ```latex
    $$
    	\frac{\partial J(\theta)}{\partial\theta_j} = -\frac1m\sum_{i=0}^m(y^i - 	h_\theta(x^i))x^i_j
    $$
    
    ```
    
    ∂ J ( θ ) ∂ θ j = − 1 m ∑ i = 0 m ( y i − h θ ( x i ) ) x j i \\frac{\\partial J(\\theta)}{\\partial\\theta\_j} = -\\frac1m\\sum\_{i=0}^m(y^i - h\_\\theta(x^i))x^i\_j ∂θj​∂J(θ)​\=−m1​i\=0∑m​(yi−hθ​(xi))xji​
    
*   **推导过程**
    
    ```latex
    $$
    \begin{align}
    	\frac{\partial J(\theta)}{\partial\theta_j}
    	& = -\frac1m\sum_{i=0}^m(y^i - h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(y^i-h_\theta(x^i))\\
    	& = -\frac1m\sum_{i=0}^m(y^i-h_\theta(x^i)) \frac{\partial}{\partial\theta_j}(\sum_{j=0}^n\theta_j x^i_j-y^i)\\
    	&=-\frac1m\sum_{i=0}^m(y^i -h_\theta(x^i)) x^i_j
    \end{align}
    $$
    
    ```
    
    KaTeX parse error: Expected 'EOF', got '&' at position 48: …tial\\theta\_j} &̲ = -\\frac1m\\sum…

添加内容：  
1.字符下标

max ⁡ a &lt; x &lt; b { f ( x ) } \\max \\limits\_{a&lt;x&lt;b}\\{f(x)\\} a<x<bmax​{f(x)}

```latex
$$
\max \limits_{a<x<b}\{f(x)\}	
$$

```

### 参考

1.  [https://blog.csdn.net/baidu\_38060633/article/details/79183905](https://blog.csdn.net/baidu_38060633/article/details/79183905)
2.  [https://www.latex-project.org/help/](https://www.latex-project.org/help/)

注：如有问题，请指正，谢谢 
 [https://blog.csdn.net/happyday_d/article/details/83715440](https://blog.csdn.net/happyday_d/article/details/83715440)