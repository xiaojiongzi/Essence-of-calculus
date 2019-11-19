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

![image-20191119213835656](C:\Users\USER\AppData\Roaming\Typora\typora-user-images\image-20191119213835656.png)

​		红色的这部分化简出来肯定有个 (dx)^2，可以忽略；也可以理解为两个很小值d(g)与d(h)相乘相对d(x)会小很多，可以忽略。

#### 三：链式法则

​    公式  
$$
\frac{d}{dx}(g(h(x)) = \frac{dg}{dh}\frac{dh}{dx}=\frac{dg}{dx}
$$
​		可以这么说，g(h)的变化率乘以h(x)的变化率。