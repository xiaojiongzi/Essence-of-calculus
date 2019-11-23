## Visualizing the chain rule and product rule

#### 一：加法法则： 

​		 公式：
$$
\frac{d}{dx}(g(x)+f(x)) = \frac{dg}{dx}+\frac{df}{dx}
$$

#### 二：乘法法则：

​		公式：
$$
\frac{d}{dx}(g(x)*f(x)) = f(x)\frac{dg}{dx}+g(x)\frac{df}{dx}
$$
​		推导：

 ![1.png](https://github.com/xiaojiongzi/Essence-of-calculus/blob/master/images/1.png?raw=true) 

​		红色的这部分化简出来肯定有个 (dx)^2，可以忽略；也可以理解为两个很小值d(g)与d(h)相乘相对d(x)会小很多，可以忽略。

#### 三：链式法则

​    公式  
$$
\frac{d}{dx}(g(h(x)) = \frac{dg}{dh}\frac{dh}{dx}=\frac{dg}{dx}
$$
​		可以这么说，g(h)的变化率乘以h(x)的变化率。

## What's so special about Euler's number e

求指数函数的导数的时候如 f(x) = 2^x, 得到如下式子：
$$
\frac{dy}{dx}=2^x(\frac{2^{dx}-1}{dx})
$$
后面这个括号里面直接化不出来，但随着dx取值减少；这个括号里的值会出现一个常数
$$
\frac{d(2^t)}{dx}=2^x(0.6931...)
$$
同理 
$$
\frac{d(3^t)}{dx}=3^x(1.0986...)
$$

$$
\frac{d(8^t)}{dx}=8^x(2.07941...)
$$
所有的幂函数的变化率都是他自己乘以一个常数。然后我们刚好发现 8 的系数是 2 的系数的 3 倍；0.6931 * 3 = 2.07941。这说明这个常数应该是与幂函数的常数的大小有一个log关系的；log(8) = 3log(2)。这时，我们就要想找到一个数能不能使变化率的常数等于1，也就是找到这个对数的底数。然后这个数就是e，这里就不推倒了。所以幂函数的导数就是。
$$
\frac{da^x}{dx}=a^x\ln{a}
$$
为什么说e自然呢，因为变化率等于函数本身。

e的解释，建议再参考参考这个，理解下e为什么这么自然 http://www.ruanyifeng.com/blog/2011/07/mathematical_constant_e.html 

## Implicit differentiation, what's going on here?

隐函数 f(x,y)=0 的求导怎么做呢，先看下面的例子，我们要求的是dx/dt：



![2](https://github.com/xiaojiongzi/Essence-of-calculus/blob/master/images/2.png?raw=true)

假设图示的梯子匀速下路速度为v(m/s), x,y分别表示两条直角边的长度，它们都是关于t的函数。因为斜边恒等于5，也就是x^2+y^2恒等于25；所以图示的第二个式子成立（x^2+y^2）关于时间的变化率恒等于零。然后化成第3个式子，x(t)表示水平的这条边当前的长度，y(t)表示竖直的这条边当前的长度，dy/dx为速度v；代入式子可求得dx/dt。

抛开t直接看 x^2+y^2=25;令S=x^2+y^2。dS可以看成是S的一点微小的变化；只有当dS为零的时候，S才会等于25；就相当于经过很小的变化之后，这个点还是在函数图像上。

其他的也同理 g(x) = h(x); 求导，直接就化成 dg = dh; 意思就是两边的变化相等，变化之后，函数g(x) = h(x)才会依旧成立。

得到这个结论后，Inx的导数可以这么求：
$$
\ln{x} = y \\ e^y=x \\ de^y = dx \\ e^ydy = dx \\ \frac{dy}{dx}=\frac{1}{e^y} \\ \frac{dy}{dx}= \frac{1}{x}
$$
那么通式就是
$$
\frac{d\log_ax}{dx}=\frac{1}{x\ln{a}}
$$

## Limits, L'Hopital's rule, and epsilon delta definitions

导数的正式定义： 
$$
\frac{df}{dx} = \lim_{\Delta{x}\to0}\frac{f(x+\Delta{x})-f(x)}{\Delta{x}}
$$
x与\Delta{x}的区别就是dx等于\Delta{x}无限趋向于0的结果；而\Delta{x}中x的变化可以是任意的。df也是同理。 可以看成左边就是右边的简写形式。

dx的理解问题：有人理解把它就看成一个数学符号，还有人把它当成一个无穷小的变化量；这都不太对，dx为无穷小的变化量，这个说法有点自相矛盾，pass；应当将dx解读为一个具体的有限小的变化量，在思考时，随时关注dx逼近0时的情况。

极限的定义：

![3](https://github.com/xiaojiongzi/Essence-of-calculus/blob/master/images/3.png?raw=true)

这里在x=0时不存在极限，如图所示，因为无论两条竖线怎么逼近，两条横线的距离都不能再小了。这个叫极限的（ε-δ）定义。这里不多扩展，可自行百度。我是简单的理解为连续就有极限。

洛必达法则：

​	当f(x)与g(x)在某一点a处，f(a) = g(a)=0时，不能直接计算出f(a)/g(a)的值；需要求x逼近与a时的极限值。求f(a)/g(a) 就相当于  df/dg 。因为f(a)=0, df近似为f函数在a点的函数值f(a),同理g也是一样。分子分母同时除以dx就得到了
$$
\lim_{x\to{a}}(\frac{f(x)}{g(x)})=\frac{f'(x)}{g'(x)}\quad \quad(f(a)=0, g(a)=0)
$$
这只是一部分0/0型的，还有oo/oo型的就自行百度吧。

洛必达法则是伯努利发现的；洛必达花钱买的名字。