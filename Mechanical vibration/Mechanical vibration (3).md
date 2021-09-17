# Mechanical vibration 机械振动
---
**$$\begin{aligned}Organized\quad in\quad NKU \end{aligned}$$**
***
[toc]

* * *

## 简谐振动的合成和分解
----------

### 同方向同频率的简谐振动合成后仍为一简谐振动
-------------------------

*   证明：我们首先定义两个同频率的简谐运动的方程 $x_{1}=A_{1}cos\left( \omega t + \varphi_{10} \right)$ 与$x_{2}=A_{2}cos\left( \omega t + \varphi_{20} \right)$ 。所以合振动的方程是 $x=x_{1}+x_{2}=A_{1}cos\left( \omega t + \varphi_{10} \right) + A_{2}cos\left( \omega t + \varphi_{20} \right)$ 。利用高中所学的三角函数。 $x=A_{1}cos\left( \omega t + \varphi_{10} \right) + A_{2}cos\left( \omega t + \varphi_{20} \right)$ $=A_{1} cos\omega t \cdot cos\varphi_{10} - A_{1} sin\omega t \cdot sin\varphi_{10}  + A_{2} cos\omega t \cdot cos\varphi_{20} - A_{2} sin\omega t \cdot sin\varphi_{20}$ $=( A_{1}cos\varphi_{10} + A_{2}cos\varphi_{20}) cos\omega t - (A_{1} sin\varphi_{10} + A_{2}sin\varphi_{20}  )  sin\omega t$

此时我们令 $A=\sqrt{( A_{1}cos\varphi_{10} + A_{2}cos\varphi_{20}) ^{2} + (A_{1} sin\varphi_{10} + A_{2}sin\varphi_{20} )^{2}}$ $=\sqrt{A_{1}^{2}+ A_{2}^{2} + 2A_{1}A_{2}cos\varphi_{10}cos\varphi_{20} + 2A_{1}A_{2}sin\varphi_{10}sin\varphi_{20}  }$

$=\sqrt{A_{1}^{2}+ A_{2}^{2} + 2A_{1}A_{2}cos(\varphi_{20} - \varphi_{10} ) }$ （这里是 $\varphi_{20}$ 还是 $\varphi_{10}$ 在前都没有关系，因为 $cosx=cos(-x)$ ）

令 $tan \varphi = \frac{A_{1} sin\varphi_{10} + A_{2}sin\varphi_{20} }{A_{1}cos\varphi_{10} + A_{2}cos\varphi_{20}}$

所以继续按照高中三角函数相加，把 $A$ 提出来。

$原式=A(\frac{A_{1}cos\varphi_{10} + A_{2}cos\varphi_{20}}{A} cos\omega t -\frac{ A_{1} sin\varphi_{10} + A_{2}sin\varphi_{20}   }{A} sin\omega t )$

$=A(cos\varphi cos\omega t - sin\varphi sin\omega t )$

$=Acos(\omega t + \varphi)$

  

   结论：==由此可知同方向同频率的两个简谐运动合成出来，仍旧是一个简谐运动。==**周期依旧是原来的周期，振幅变成了** $\sqrt{A_{1}^{2}+ A_{2}^{2} + 2A_{1}A_{2}cos(\varphi_{20} - \varphi_{10} ) }$ **。初相变成了** $arctan \frac{A_{1} sin\varphi_{10} + A_{2}sin\varphi_{20} }{A_{1}cos\varphi_{10} + A_{2}cos\varphi_{20}}$ **。**

  
---
### 同方向不同频率的简谐运动合成
------------------

  证明：我们首先定义两个同方向不同频率的简谐运动的方程 $x_{1}=Acos\left( \omega_{1} t + \varphi \right)$ 与 $x_{1}=Acos\left( \omega_{2} t + \varphi \right)$ 。所以合运动就是 $x=x_{1}+x_{2}=Acos\left( \omega_{1} t + \varphi \right) + Acos\left( \omega_{2} t + \varphi \right)$

$=A(  cos \omega_{1} t \cdot cos\varphi - sin\omega_{1} t \cdot sin\varphi + cos \omega_{2} t \cdot cos\varphi - sin\omega_{2} t \cdot sin\varphi )$

$=A[ (cos \omega_{1} t +  cos \omega_{2} t  ) cos\varphi - (sin\omega_{1} t + sin\omega_{2} t) sin\varphi ]$

和差化积得

$=A[2 (cos( \frac{\omega_{1}+\omega_{2}}{2}  t)cos( \frac{\omega_{1}-\omega_{2}}{2}  t)cos\varphi - 2sin( \frac{\omega_{1}+\omega_{2}}{2}  t)cos( \frac{\omega_{1}-\omega_{2}}{2}  t) sin\varphi ]$

$=2Acos( \frac{\omega_{1}-\omega_{2}}{2}  t)[(cos( \frac{\omega_{1}+\omega_{2}}{2}  t)cos\varphi - sin( \frac{\omega_{1}+\omega_{2}}{2}  t) sin\varphi ]$

$=2Acos( \frac{\omega_{1}-\omega_{2}}{2}  t) \cdot cos( \frac{\omega_{1}+\omega_{2}}{2}  t + \varphi)$

 结论：==同方向不同频率的简谐运动合成之后仍然是振动，但是这个方程明显不满足简谐运动。==

*   它的**周期**变成了 $\frac{4\pi}{\omega_{1}+\omega_{2} }$ 。
*   **振幅**是一个周期性变化的值 $|2Acos( \frac{\omega_{1}-\omega_{2}}{2}  t) |$ （因为振幅只能为正值）

*   **振幅的周期**是 $\frac{2\pi}{\omega_{1}-\omega_{2} }$ （因为取绝对值所以减半）
*   这种振幅呈现周期性变化的叫做**拍**
*   合振幅每变化一个周期称为一拍.单位时间内拍出现的次数 （合振幅变化的频率）叫作**拍频**

*   $\omega_{拍} =| \omega_{1}-\omega_{2}| \Rightarrow \upsilon = \frac{\omega_{拍} }{2\pi}=| \frac{\omega_{1}}{2\pi} - \frac{\omega_{2}}{2\pi}|=| \upsilon_{1}-\upsilon_{2}|$ **拍的频率为两个分振动的频率之差！**

*   **初相未变**

![](\pic%20Mechanical%20vibration/7.jpg)  

---
### 两个相互垂直的同频率简谐振动的合成与李萨如图
---

*   **证明**：我们表示两个运动的初始方程$x=A_{1}cos\left( \omega t + \varphi_{10} \right)$ 与$y=A_{2}cos\left( \omega t + \varphi_{20} \right)$。

* 如果不能画图，我们也可以从另外一方面来证明。**消参**得到质点运动的方程 $\frac{x^{2}}{A_{1}^{2}}+\frac{y^{2}}{A_{2}^{2}}-2\frac{xy}{A_{1}A_{2}}cos(\varphi_{20} - \varphi_{10}) = sin(\varphi_{20} - \varphi_{10})$ 。

* 在大部分情况下这是个椭圆。当 $\varphi_{20} - \varphi_{10} = k\pi + \frac{\pi}{2}$时 ，方程就可以写成 $\frac{x^{2}}{A_{1}^{2}}+\frac{y^{2}}{A_{2}^{2}}=1$ 这是一个高中常见的椭圆（焦点在哪个轴取决于两个振幅大小）。当 $\varphi_{20} - \varphi_{10} = k\pi$ 时，原式就可以写成 $\frac{x^{2}}{A_{1}^{2}}-2\frac{xy}{A_{1}A_{2}}+\frac{y^{2}}{A_{2}^{2}}=0$ 。这是一个完全平方式。所以可以写成 $y=\frac{A_{2}}{A_{1}}x$ 。这就是一条直线了，并不是椭圆.

* 刚刚讨论了一些特殊情况，接下来看看合成之后离开平衡位置的位移是什么。很明显 $S=\sqrt{x^{2}+y^{2}} = \sqrt{A_{1}^2+A_{2}^2}cos(\omega t + \varphi)$ 

  
*   结论：在直角坐标系把图形画了出来。同周期我们就可以得到以下的图形。图中的箭头就是质点运动的方向。

![](\pic%20Mechanical%20vibration/8.jpg)  


*   李萨如图：==上面的类似于这样画出来就称之为李萨如图。== 上面都是同周期，当周期不同的时候会形成各种各样的李萨如图，如下

* 我们可以通过丽萨如图直接得到角频率比例：
  分别做一条水平和竖直的直线与丽萨如图相交，分别计算两条直线与图形形成的交点个数，注意直线应该尽量避免与莉萨如图本身的交点相交，如果直线与丽萨如图本身的交点相交，那么计数时应当＋2，此时有：
  $$\begin{aligned} \frac{水平交点数}{竖直交点数} = \frac{竖直频率}{水平频率} \end{aligned} $$
  常见的图像如下：
![](\pic%20Mechanical%20vibration/9.png)  

---
## 对于一般的简谐运动合成
-----------

对于这部分一般就两种方法：

*   通过**三角恒等式**将多个方程写成一个方程就行了。比较好看出连续变化的关系，但是不好求，写起来特麻烦。
*   通过**旋转矢量法**，将多个简谐运动画在图里，然后向量相加。比较容易直观的看出某一时刻质点的运动状态，但是不好表示连续变化的关系。

* * *

## 阻尼振动
----

*   证明与定义：前面都是讲的理想状态下，能量无损耗。但在现实是肯定不可能的。所以引入了阻力系数 $\gamma$ 。你可以大致理解成以前学的摩擦系数差不多的东西。阻力系数的定义是 $F_{\gamma}=-\gamma v$ 。所以质点在简谐运动中的受力情况就可以写成 $ma=-kx-\gamma v\Rightarrow a=-\frac{k}{m}x-\frac{\gamma}{m}v$ 。因为以前我们就知道了 $\omega = \sqrt{\frac{ k}{m}}$ 。相似的这里我们令 $\beta = \frac{\gamma}{m}$ 称之为阻尼因子。所以原式就可以写成 $a+2\beta v + \omega^{2}x=0 \Rightarrow \frac{d^{2}x}{dt^{2}}+2\beta \frac{dx}{dt} + \omega^{2}x=0$ 。接下来就是解微分方程了，求出共轭复根。
*   当 $\beta > \omega$ 解出来的方程实际是 $x=e^{-\beta t}(C_{1}e^{pt}+C_{2}e^{-pt})$ 。这里的 $p=\sqrt{\beta^{2}-\omega^{2}}$ 。但是当 $\beta \ll \omega$ ，再换言之 $\gamma$ 比较小的时候。 就可以利用三角恒等式化成 $x=A_{0}e^{-\beta t}cos(\omega t + \varphi_{0})$ 。当 $\beta = \omega$ ，解出来 $x=(C_{1}+C_{2}t)e^{-\beta t}$ 。

*   **阻力系数** $\gamma$ 。满足方程 $F_{\gamma}=-\gamma v$ 。
*   **阻尼因子** $\beta$ 。 $\beta = \frac{\gamma}{m}$ 。它与 $\omega$ 之间的关系决定了方程的解，也等于决定了物体的运动情况。

*   **弱阻尼：** $x=A_{0}e^{-\beta t}cos(\omega t + \varphi_{0})$ 一般应用于$ \beta \ll \omega$ ，但是 $\beta < \omega$ 都是满足的。

*   物体在平衡位置来回振动，但是振幅不断衰竭，呈指数衰减。
*   具有准周期。因为振幅在衰减，所以严格说来不是周期。 $T=\frac{2\pi}{\sqrt{\omega^{2} - \beta^{2}}} > \frac{2\pi}{\omega}$

*   **临界阻尼：** $x=(C_{1}+C_{2}t)e^{-\beta t}$ $\left( \beta = \omega \right)$

*   在物体刚刚到达平衡位置的时候就停下来，不会再继续振动。

*   **过阻尼：** $x=e^{-\beta t}(C_{1}e^{pt}+C_{2}e^{-pt})$ 这里 $p=\sqrt{\beta^{2}-\omega^{2}}$ 。 $\left( \beta >\omega \right)$

*   物体到达平衡位置就停下

![](\pic%20Mechanical%20vibration/10.jpg)  

---
## 受迫振动
----

*   证明与定义：一个原本静止的物体，受到一个驱动力的作用，还有阻尼作用的情况下开始振动。


* 当驱动力与阻尼效应达到满足简谐运动的平衡时（简谐运动的力满足 $F=-kx$ ）系统进入平衡状态。平衡时的频率一定和驱动力的频率相同。

*   稳定状态： $x= Acos(pt + \varphi)$ 。其中 $A=\frac{f_{0}}{\sqrt{ (\omega^{2}-p^{2})^{2}+ 4\beta^{2} p^{2}}}$ 。 $p$ 是驱动力的周期。 $\varphi=arctan(-\frac{2\beta p}{\omega^{2}-p^{2}})$ 。
*   非稳定状态： $x=A_{0}e^{-\beta t}cos (\omega_{1} t + \varphi_{0}) + Acos(pt + \varphi)$
---
## 共振
---
其实共振就是一种特殊的受迫振动。我们刚刚算了振幅是与驱动力的频率有关的 $A=\frac{f_{0}}{\sqrt{ (\omega^{2}-p^{2})^{2}+ 4\beta^{2} p^{2}}}$ 。当振幅最大的时候也就是我们共振现象。求函数的极值点。最后得到 $p=\sqrt{\omega^{2} - 2\beta^{2}}$ 。我们就将这个 $\omega$ 称之为固有频率（在弹簧振子中等于 $\frac{k}{m}$ ）。阻尼因子 $\beta$ 越小，共振角频率 $p$ 越接近于系统的固有频率 $\omega$ ，同时共振振幅 $A$ 也越大。

![](\pic%20Mechanical%20vibration/11.jpg)  

