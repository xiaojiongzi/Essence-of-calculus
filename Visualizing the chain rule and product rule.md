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