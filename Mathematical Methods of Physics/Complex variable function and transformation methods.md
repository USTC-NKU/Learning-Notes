---
title: Complex variable function and transformation methods
math: true
tags: Complex variable function
categories: Mathematical Methods of Physics
date: 2021-10-13 14:32
---

***
[toc]
***

# 复变函数的概念
## §    映射
* 设X和Y是两个集合，映射f是这两个集合之间的一种对应关系，在f的作用下，使X中的每一个元素对应Y中唯一的一个元素，我们称f是一个从X到Y的**映射**，记为
  * $$\begin{equation}
      f：X\rightarrow Y
      \end{equation}$$ 
  或者记为，$\forall x \in X$，有
  * $$\begin{equation}
      f：x\rightarrowtail y
      \end{equation}$$  
  我们称y为在f映射下x的像，亦可写为f(x)=y.
* 从映射的定义可以看出，两个集合间的映射，只能是一对一或多对一的映射，而不能是一对多的映射.
* 函数关系是映射的一种，映射比函数关系更广泛，它可以表示一种变换、一种算子的运算、泛函等等的映射关系.    
## §    复数
* 当我们对实数域加以扩充，定义了虚数单位i，即$i^2=-1$，我们对一个有序的实数对$(x,y),x,y\in R$，定义了复数$z=x+iy$.所有的复数z构成复数域，记为C.我们称x为复数z的实部，称y为复数的虚部
* 共轭复数$z^*=x-iy$
* 共轭复数的模$\vert z\vert=z\cdot z^*=x^2+y^2$
* 由复数域C构成的空间是线性空间，满足线性空间的运算律，不再赘述
* 由于复数描述了有序实数对，因此复数域C可以用复平面表示.由原点到复平面上任一点构成一个向量，向量与x轴的夹角称为复数z的**幅角**，记为$\theta=\mathrm{Arg}(z)$，半径r为复数z的模，即该向量的长度，$r=\vert z\vert$
* 在复平面上，所有的复数都可以用$(r,\theta)$来表示
  * $$\begin{equation}
      z =x+iy=r(\cos\theta+i\sin\theta)
      \end{equation}$$
* 与实平面$R^2$不同，复平面中x轴是实轴，y轴是虚轴，这两轴的性质是不同的.
* **欧拉公式**
  * $$\begin{equation}
      \sin\theta = \sum_{n=1}^{\infty}(-1)^{n+1}\frac{\theta^{2n-1}}{(2n-1)!}
      \end{equation}$$
  * $$\begin{equation}
      \cos\theta = \sum_{n=1}^{\infty}(-1)^{n+1}\frac{\theta^{2n-2}}{(2n-2)!}
      \end{equation}$$
  * $$\begin{equation}
      e^\theta = \sum_{n=0}^{\infty}\frac{\theta^n}{n!}
      \end{equation}$$
  * $$\begin{equation}
      e^{i\theta}=\sum_{n=0}^{\infty}\frac{(i\theta)^{n}}{n!}=\cos\theta+i\sin\theta
      \end{equation}$$
* 由Euler公式，我们可以把复数z表示成
  * $$\begin{equation}
      z=x+iy=r(\cos\theta+i\sin\theta)=re^{i\theta}
      \end{equation}$$
* 由Euler定理，我们可以得到如下运算公式
  * $$\begin{equation}
      z_1\cdot z_2=r_1\cdot r_2e^{i(\theta_1+\theta_2)}
      \end{equation}$$
  * $$\begin{equation}
      z^n=r^ne^{in\theta}
      \end{equation}$$
  * $$\begin{equation}
      \vert z_1z_2\vert=\vert z_1\vert\vert z_2\vert
      \end{equation}$$
  * $$\begin{equation}
      arg(z_1z_2)=arg(z_1)+arg(z_2)
      \end{equation}$$
  * $$\begin{equation}
      arg(\frac{z_1}{z_2})=arg(z_1)-arg(z_2)
      \end{equation}$$
* **复球面**
  ![复球面](\pic/复球面.jpg)
* 在x-iy复平面C上，以原点O为南极，以N为北极做一条直径为1的球面，在直角坐标系$(\xi,\eta,\zeta)$中，$\xi$轴与x轴重合，$\eta$轴与iy轴重合，$O\zeta$垂直于$\xi-\eta$平面，球面的球心坐标为(0,0,0.5)，我们确定如下法则使得球面上的点与复平面C上的点构成一一对应的关系：取平面上的点z=x+iy与球面北极N以直线连接，交于球面的点P，则C平面上的每一点都与球面上唯一的一点P相对应.如果把球面的北极N点挖掉，没有北极N点的开球面与C平面完全同构，这两组坐标有如下对应关系
  * $$\begin{equation}
    \xi=\frac{1}{2}\frac{z+z^*}{1+zz^*}
    \end{equation}$$ 
  * $$\begin{equation}
    \eta=\frac{1}{2i}\frac{z-z^*}{1+zz^*}
    \end{equation}$$
  * $$\begin{equation}
    \zeta=\frac{zz^*}{1+zz^*}
    \end{equation}$$
  * $$\begin{equation}
    x=\frac{\xi}{1-\zeta}
    \end{equation}$$
  * $$\begin{equation}
    y=\frac{\eta}{1-\zeta}
    \end{equation}$$
* 当z点从C平面的原点O出发沿着任一条C平面上的涉嫌趋于无穷时，点P将沿着球面的一条经线趋于北极N点，因此我们也称N点为复平面C的无穷原点
## §    复变函数
* 如果我们把复变函数定义为复平面C到复平面C的隐射f，$f:C\rightarrow C$，f具有一般的形式为
  * $$\begin{equation}
    f(z)=u(x,y)+iv(x,y)
    \end{equation}$$
  其中u(x,y)和v(x,y)是x,y的实函数，即$u,v：R^2\rightarrow R$，这就要求f把定义域C(以x和iy为轴的复平面)上的点映射到值域C(以u和iv为轴的复平面)上唯一的一点上.但作为定义域的复数，由于其幅角的多值性，使得一些函数的映射关系不能满足单值性的要求，因此不能把复变函数简单定义为复平面到复平面的映射
  * 举个栗子
  例如函数$f(z)=\sqrt{z}$，由于$z=e^{i(\theta+2k\pi)}$，显然当k=0和k=1时开方运算的结果时不同的，因此该函数是一个多值函数，就不能简单定义为复平面到复平面的映射
  * 要定义这个映射，我们必须将自变量z的复平面重新构造，将幅角所构成的多值性定义域分开，使得每一个定义域都构成一个单值映射区域，这就需要黎曼面的引入
* **黎曼面(Riemann面)**
  * 黎曼面符号记为$C^R$，对于黎曼面有$f(z)：C^R\rightarrow C$
  * **枝点**
    * 对于f(z)的定义域C，若存在$z_o\in C$，当自变量z绕$z_o$旋转一圈回到原来的位置时，函数值f(z)不还原，则称$z_o$为**枝点**，当z绕$z_o$旋转最少的n圈后能使f(z)的数值还原，则称$z_o$为f(z)的**n-1阶枝点**
    * 一般来说，使$f(z)=0$或$f(z)=\infty$的点可能是f(z)的枝点，而且**枝点是成对出现的，即枝点的个数为偶数**
  * 构造黎曼面的方式
    * 将两个枝点用一条直线或曲线连接起来，一般情况下尽可能取直线，自变量z不能越过此线作连续变化，即把原来自变量的定义域用线隔开了，我们把这两个枝点间的联线称为**割线**，用割线割开的定义域就变成一个单值分支定义域，所有的这些单值分支定义域的割线上下沿互相粘接起来，就构成了黎曼面
* **复变函数的严格定义**
  * 复变函数是Riemann面到复平面上的映射
    $$\begin{equation}
    f(z): C^R\rightarrow C
    \end{equation}$$
* **几种常见的复变函数**
  1. 有理函数
     $$\begin{equation}
     f(z)=\frac{\sum_{i=1}^{n}a_iz^i}{\sum_{j=1}^{m}b_jz^j}
     \end{equation} \quad a_i,b_j\in C\quad m,n\in Z$$
  2. 指数函数
     $$\begin{equation}
     f(z)=e^z
     \end{equation}$$
  3. 对数函数
     $$\begin{equation}
     f(z)=\ln(z)
     \end{equation}$$
  4. 幂函数
     $$\begin{equation}
     f(z)=z^a
     \end{equation}$$
  5. 三角函数
     $$\begin{equation}
     \cos z=\frac{e^{iz}+e^{-iz}}{2}
     \end{equation}$$
     $$\begin{equation}
     \sin z =\frac{e^{iz}-e^{-iz}}{2i}
     \end{equation}$$

     * 他们满足实数域上的三角函数的形式，唯一不同的是其模可能大于1
  6. 双曲函数
     $$\begin{equation}
     \sh z=\frac{e^z-e^{-z}}{2}
     \end{equation}$$
     $$\begin{equation}
     \ch z=\frac{e^z+e^{-z}}{2}
     \end{equation}$$

***
# 解析函数
## §    复变函数的导数
* **一：复变函数的连续性**
  * 复变函数f(z)在$z_0$及其邻域有定义，当自变量z以任何路径趋于$z_0$时，有
    $$\begin{equation}
    \lim_{z\to z_0}f(z)=f(z_0)
    \end{equation}$$
    则称f(z)在$z_0$**连续**.如果复变函数f(z)在整个区域$\Omega$内的所有点都连续，则称f(z)在$\Omega$内连续
  * 复变函数的连续型等价于f(z)=u(x,y)+iv(x,y)的表达式中两个二元函数u(x,y)、v(x,y)都是连续函数  
* **二：复变函数的导数**
  * 对于$z_0$为复变函数f(z)的定义域$\Omega$内的一点，当z以任何路径区域$z_0$时，即$\Delta z=z-z_0$趋于0时，若极限
    $$\begin{equation}
    \lim_{\Delta z\to 0}\frac{f(z_0+\Delta z)-f(z_0)}{\Delta z}
    \end{equation}$$
    存在且唯一，则称f(z)在$z_0$点**可导**
* **三：柯西-黎曼条件**
  * 由于f(z)可以表示为f(z)=u(x,y)+iv(x,y)，z=x+iy，则导数也可以表示为
    $$\begin{equation}
    f'(z)=\frac{\Delta u+\Delta iv}{\Delta x+\Delta iy }
    \end{equation}$$
    当取两种特殊的路径使$\Delta z$趋于零时
    * (1) 取平行于x轴的路径趋于零
      $$\begin{equation}
      f'(z)=\frac{\Delta u +\Delta iy}{\Delta x}=\frac{\partial u}{\partial x}+i\frac{\partial v}{\partial x}
      \end{equation}$$
    * (2) 取平行于y轴的路径趋于零
      $$\begin{equation}
      f'(z)=\frac{\Delta u + i\Delta v}{i\Delta y}=-i\frac{\partial u}{\partial y}+\frac{\partial v}{\partial y}
      \end{equation}$$
    * 因为可导，因此不同路径得到的极限需要存在且相等，于是
      $$\begin{equation}
      \frac{\partial u}{\partial x}=\frac{\partial v}{\partial y} \quad \frac{\partial u}{\partial y}=-\frac{\partial v}{\partial x}
      \end{equation}$$
    * 上一方程就称为**Cauchy-Riemann方程或Cauchy-Riemann条件**，简称C-R条件.C-R条件是可导的必要不充分条件

## §    复变函数的解析性
* 如果复变函数f(z)在$z_0$点可导，并且在$z_0$的邻域内每一点都可导，则我们称f(z)在$z_0$是**解析**的，复变函数的解析性比可导要严格许多
* 如果复变函数f(z)在其定义域$\Omega$内每一点都是可导的，则称f(z)在其定义域$\Omega$内是**解析**的，或称为**全纯**的
* **复变函数为解析函数的充要条件**
  * 定理
    复变函数f(z)=u(x,y)+iv(x,y)在区域$\Omega$内为解析函数的**充分必要条件**是
     1. 在复平面区域$\Omega$相应的实平面区域内u(x,y),v(x,y)可微
     2. 并且u(x,y),v(x,y)满足C-R条件
* 命题组
  * 若f(z)为区域$\Omega$上的解析函数，且f(z)为实函数，即$f(z)=f^*(z)$则f(z)为常数
  * 若f(z)为区域$\Omega$上的解析函数，则在区域$\Omega$上有$\frac{\partial f(z)}{\partial z^*}=0$，即f(z)不依赖于$z^*$
  * 在复平面区域$\Omega$解析的函数，f(z)=u(x,y)+iv(x,y)，其实部和虚部都为(x,y)平面内的调和函数，即满足调和场方程，也就是二维Laplace方程. 
     $$\begin{equation}
     \nabla^2 u=0 \quad \nabla^2 v=0
     \end{equation}$$

## §    复势
* 命题
  解析函数f(z)=u(x,y)+iv(x,y)的实部和虚部所构成的两个曲线族$u(x,y)=u_0$、$v(x,y)=v_0$是**相互正交**的 
  * 简证
    解析函数满足C-R方程，取两曲线族的梯度就得到曲线族的法向向量，两个法相向量点乘并结合C-R方程就能得到点乘为零的结果，因此两曲线族是正交的
  * 在二维问题中，我们把u(x,y)看作一个势场函数，其曲线为等势线；把v(x,y)看作通量函数，其曲线为等通量线.由于u(x,y)、v(x,y)满足调和场方程，因此我们称解析函数f(z)=u+iv为**复势**，它是描述场的复函数

## §    解析函数变换
* 解析函数变换通常称为**保角变换**或**共形变换**
* 对于定义在复平面C某一区域$\Omega$中的一个解析函数w=f(z)=u+iv，它是把复平面$\omega$中的元素映射到复函数W平面的某一区域D的一种映射
  $$\begin{equation}
  f:\Omega\rightarrow D
  \end{equation}$$
  $$\begin{equation}
  f:(x,iy)\rightarrow (u,iv)
  \end{equation}$$
  其中(x,iy)为C平面上的坐标，(u,iv)为W平面上的坐标
* 考虑$\Omega$上点z的一个小增量，通过f(z)变换到W平面的区域D中,产生w的一个小增量.由于f(z)是解析函数，因此导函数存在
  $$\begin{equation}
  \arg f'(z)=\arg \lim_{\Delta z\to 0}\frac{\Delta w}{\Delta z}=\arg\Delta w -\arg\Delta z
  \end{equation}$$
  * 由于解析函数在某一点的导函数值存在且唯一，因此其辐角是唯一确定的.这表明不论以什么方式趋近点z时，其辐角经过解析函数映射为w时辐角的增量是一个定值
    $$\begin{equation}
     \arg\Delta w=\arg\Delta z+\arg f'(z)
    \end{equation}$$
  * 同时可以看出，在f(z)的映射下，W平面下模长的增量总是乘以一个定值，而与趋近方式无关
    $$\begin{equation}
    |\Delta w|=|\Delta z|\cdot|f'(z)|
    \end{equation}$$
  * 假设有两条相交曲线过C平面上的同一点z，通过解析函数f(z)将其映射为W平面上过同一点w的两条相交曲线，曲线分别记为$l_1,l_2$、$C_1,C_2$
    $$\begin{aligned}
     \arg C_1&=\arg l_1+\arg f'(z)  \\
     \arg C_2&=\arg l_2+\arg f'(z)  \\
     \arg C_2-\arg C_1 &= \arg l_2 -\arg l_1
    \end{aligned}$$  
    可见变换前后两曲线之间的夹角保持不变，因此我们通常称解析变换为**保角变换**；同时我们也看到变换前后的模长的性质，因此我们也称解析变换为**共形变换**
* **Laplace算子在解析变换下的形式**
  * 考虑将(x,y)平面上的Laplace算子在解析函数w=f(z)=u+iv的变换下，变成(u,v)平面上的形式
    * $$\begin{equation}
      \nabla^2=\frac{\partial^2 }{\partial x^2}+\frac{\partial^2 }{\partial y^2}
      \end{equation}$$
    * $$\begin{equation}
      \frac{\partial }{\partial x}=\frac{\partial u}{\partial x}\frac{\partial }{\partial u}+\frac{\partial v}{\partial x}\frac{\partial }{\partial v}
      \end{equation}$$
    * $$\begin{equation}
      \frac{\partial }{\partial y}=\frac{\partial u}{\partial y}\frac{\partial }{\partial u}+\frac{\partial v}{\partial y}\frac{\partial }{\partial v}
      \end{equation}$$
    * $$\begin{equation}
      \frac{\partial^2 }{\partial x^2}=\frac{\partial^2 u}{\partial x^2}\frac{\partial }{\partial u}+(\frac{\partial u}{\partial x})^2\frac{\partial^2 }{\partial u^2}+(\frac{\partial v}{\partial x})^2\frac{\partial^2 }{\partial u^2}+\frac{\partial^2 v}{\partial x^2}\frac{\partial }{\partial v}+2\frac{\partial u}{\partial x}\frac{\partial v}{\partial x}\frac{\partial^2 }{\partial u \partial v}
      \end{equation}$$
    * $$\begin{equation}
      \frac{\partial^2 }{\partial y^2}=\frac{\partial^2 u}{\partial y^2}\frac{\partial }{\partial u}+(\frac{\partial u}{\partial y})^2\frac{\partial^2 }{\partial u^2}+(\frac{\partial v}{\partial y})^2\frac{\partial^2 }{\partial u^2}+\frac{\partial^2 v}{\partial y^2}\frac{\partial }{\partial v}+2\frac{\partial u}{\partial y}\frac{\partial v}{\partial y}\frac{\partial^2 }{\partial u \partial v}
      \end{equation}$$
    * $$\begin{equation}
      \nabla^2 x=0 \quad \nabla^2 y = 0
      \end{equation}$$
    * $$\begin{equation}
      \frac{\partial u}{\partial x}\frac{\partial v}{\partial x}+\frac{\partial u}{\partial y}\frac{\partial v}{\partial y}=0 
      \end{equation}$$
    * 由$(41)、(44)-(47)$式可以得到
    * $$\begin{equation}
      \nabla^2 =[(\frac{\partial u}{\partial x})^2+(\frac{\partial u}{\partial y})^2]\frac{\partial^2 }{\partial u^2}+[(\frac{\partial v}{\partial x}^2)+(\frac{\partial v}{\partial y})^2]\frac{\partial^2 }{\partial v^2}
      \end{equation}$$
    * 我们取平行于x轴的方式趋近，计算解析函数f(z)的导函数  
    * $$\begin{equation}
      f'(z)=\frac{\Delta(u+iv)}{\Delta x}=\frac{\partial u}{\partial x}+i\frac{\partial v}{\partial x}
      \end{equation}$$
    * 计算导函数的模长
    * $$\begin{equation}
      |f'(z)|^2=(\frac{\partial u}{\partial x})^2+(\frac{\partial v}{\partial x})^2
      \end{equation}$$
    * 注意f(z)满足Cauchy-Riemann条件，于是上式可以变换
    * $$\begin{equation}
      \nabla^2=|f'(z)|^2(\frac{\partial^2 }{\partial u^2}+\frac{\partial^2 }{\partial v^2})
      \end{equation}$$  
  * 结果表明二维Laplace算子经过解析变换后仍然保持二维Laplace方程的形式


***
# 复变函数的积分
## §    复变函数的积分    
* 复变函数的积分是指复变函数f(z)在其有定义的区域$\Omega$中，沿某一曲线C的**有向**线积分，其定义为
  $$\begin{equation}
   \int_C f(z)\mathrm{d}z=\lim_{n\to \infty}\sum_{j=1}^{n}(z_j-z_{j-1})\
  \end{equation}$$
  其中C是由a-b的一段曲线，把C分成n段，每一段的长度$|z_j-z_{j-1}|$都区域零，$\xi_j$是第j段$|z_j-z_{j-1}|$中的某一点

* 根据定义我们看到复变函数曲线的积分是有向的，因此沿着相反方向积分的结果其数值是反号的.根据f(z)=u(x,y)+iv(x,y)，因此有
  $$\begin{equation}
  \int_C f(z)\mathrm{dz}=\int [u(x,y)+iv(x,y)]\mathrm{d(x+iy)}
  \end{equation}$$
  $$\begin{equation}
  \int_Cf(z)\mathrm{dz}=\int_C(u\mathrm{dx}-v\mathrm{dy})+i\int_C(u\mathrm{dy}+v\mathrm{dx})
  \end{equation}$$
* 式(54)表明复变函数f(z)的积分与两个实变函数的线积分等价.一般来说，复变函数的线积分与积分的起点和终点位置有关，也与积分路径C的选取有关
* **复变函数积分的性质**
  1. $$\begin{equation}
     \int_C (f(z)\pm g(z))\mathrm{dz}=[\int_Cf(z) + \int_Cg(z)]\mathrm{dz}
   \end{equation}$$
  2. $$\begin{equation}
     \int_Cf(z)\mathrm{dz}=-\int_{-C}f(z)\mathrm{dz}
   \end{equation}$$
  3. $$\begin{equation}
     \int_{C1}+\int_{C2}=\int_C
   \end{equation}$$
  4. $$\begin{equation}
     |\int_C f(z)\mathrm{dz}| \le \int|f(z)||\mathrm{dz}|
   \end{equation}$$
## §    柯西积分定理
* **单连通区域的柯西积分定理**
  * 在单连通区域$\Omega$上解析的函数f(z)，当积分路径为该单连通区域内任一闭合曲线C时，有
  $$\begin{equation}
  \oint_Cf(z)\mathrm{dz}=0
  \end{equation}$$
  * 该定理可以等价表述为：**在单连通区域上解析函数的积分与积分路径无关，只与路径的起点和终点有关**
  * 单连通区域
    设D是一区域，若属于D内任一简单闭曲线的内部都属于D，则称D为单连通区域，单连通区域也可以这样描述：D内任一封闭曲线所围成的区域内只含有D中的点。更通俗地说，单连通区域是没有“洞”的区域
  * 简要证明：
    将上述积分展开为式$(54)$形式，利用实函数的格林公式，并注意解析函数满足Cauchy-Riemann方程即可得到结论 
* **多连通区域的柯西积分定理**
  ![多连通区域下的柯西积分定理](\pic/多连通区域jpg.jpg)
  * f(z)在多连通区域上解析，该多连通区域具有k内边界$C_i$.取逆时针方向绕行回路，对于每一个内边界，在其上任意选取一点与回路C上的点做割线，例如C与$C_1$的割线上沿为$A_1A_1'$，下沿为$B_1B'_1$，这样操作后就得到一个新的闭合回路L (即图中曲线所包围的空间范围)
  * $$\begin{equation}
    L=PA_1+A_1A_1'+C_1+B_1'B_1+\cdots
    \end{equation}$$
  * $$\begin{equation}
    C=PA_1+B_1A_2+\cdots+B_kP
    \end{equation}$$  
  * 应当注意到对于同一个内边界割线对应的上下边沿满足下式成立
  * $$\begin{equation}
    [\int_{A_1}^{A_1'} + \int_{B_1'}^{B_1}]f(z)\mathrm{dz}=0
    \end{equation}$$
  * 解析函数f(z)在新构成的单连通区域L上显然满足下式成立  
  * $$\begin{equation}
    \oint_Lf(z)\mathrm{dz}=[\oint_C +\sum_{i=1}^{k}\oint_{C_i}]f(z)\mathrm{dz}=0
    \end{equation}$$
  * 应注意C绕行为逆时针，而各个内边界闭环绕行为顺时针，综合$(60)-(63)$可以得到下式结果
  * $$\begin{equation}
    \oint_C f(z)\mathrm{dz} = \sum_{i=1}^{k}\oint_{C_i} f(z)\mathrm{dz}
    \end{equation}$$ 
  * **注意**：此时右侧各个内边界积分区域绕行也全部为逆时针   
* 式$(64)$就是**复连通区域的柯西积分定理**，表明在此类区域中的回路积分值等于该回路所包含全部内边界积分值之和，显示出内边界对整个回路积分的影响  
## §    柯西积分公式
* **柯西积分公式**
  * 如果f(z)在闭合回路C所包围的区域内解析，$z_0$是区域中的一点，则
  $$\begin{equation}
  \oint\frac{f(z)\mathrm{dz}}{z-z_0}=2\pi if(z_0)
  \end{equation}$$
  上式称为**柯西积分公式**
* 证明
  * 注意到被积函数g(z)在区域C上显然不解析，$z_0$为奇异点，为此，我们采取高等数学中经典的挖洞法，挖去以$z_0$为圆心取半径为r的圆域C'，并在C'与C之间做一条割线，利用多连通区域的柯西定理可以快速得到下式
  $$\begin{equation}
  \oint_Cg(z)\mathrm{dz}=\oint_{C'}g(z)\mathrm{dz}
  \end{equation}$$
  * $|z-z_0|=r$，回路C'上点满足$z=z_0+re^{i\theta}$
  $$\begin{equation}
  \oint_{C'} g(z)\mathrm{dz}=\int_0^{2\pi}\frac{f(z_0+re^{i\theta})}{re^{i\theta}}ire^{i\theta}\mathrm{d\theta}
  \end{equation}$$
  * r是趋于零的，因此就可得到柯西积分公式
  $$\begin{equation}
  \oint_Cg(z)\mathrm{dz}=i2\pi f(z_0)
  \end{equation}$$
## §    解析函数高阶导数的积分表达式
* 设f(z)在区域$\Omega$内解析，C为$\Omega$内任一闭合回路，对于C所包围区域内的任意一点z，由柯西积分公式可将f(z)表示为
  $$\begin{equation}
  f(z)=\frac{1}{z\pi i}\oint_C\frac{f(\xi)}{\xi-z}\mathrm{d\xi}
  \end{equation}$$
* 解析函数f(z)的一阶导数可以表征为
  $$\begin{equation}
  f'(z)=\lim_{\Delta z\to 0}\frac{1}{\Delta z}[f(z+\Delta z)-f(z)]
  \end{equation}$$
  $$\begin{aligned}
   & =\frac{1}{2\pi i}\lim_{\Delta z\to 0}\frac{1}{\Delta z}\oint_C\frac{f(\xi)\Delta z}{(\xi-z-\Delta z)(\xi-z)}\mathrm{d\xi} \\
   & = \frac{1}{z\pi i}\oint_C\frac{f(\xi)}{(\xi-z)^2}\mathrm{d\xi}
  \end{aligned}$$
* 上式结当然也可以直接对解析函数的积分表达式求导数，得到的结果是一致的
* **解析函数导数的一般表达式**
  $$\begin{equation}
  f^{(n)}(z)=\frac{\mathrm{d^n}}{\mathrm{dz^n}}f(z)
  \end{equation}$$
  $$\begin{aligned}
   & = \frac{n!}{2\pi i}\oint_C\frac{f(\xi)}{(\xi-z)^{(n+1)}}\mathrm{d\xi}
  \end{aligned}$$
* 解析函数具有一个很重要的性质：**解析函数存在任意阶导数，且任意阶导数都为解析函数**，这一点与实变函数有很大区别，存在一阶导数的实变函数是不能保证其高阶导数的存在的
* 从上面的一般公式我们可以得到一个重要式子，当被积函数存在奇异性时，其闭合回路积分存在，其结果为
  $$\begin{equation}
  \oint_C\frac{f(\xi)}{(\xi-z)^{(n-1)}}\mathrm{d\xi}=\frac{2\pi i}{n!}f^{(n)}(z)
  \end{equation}$$
  
***


# 复变函数的级数展开
## §    复变函数项级数
* 一个复变函数项的无穷级数可以表示为
  $$\begin{equation}
  w_1(z)+w_2(z)+\cdots+w_k(z)+\cdots=\sum_{k=1}^{\infty}w_k(z)\equiv S(z)
  \end{equation}$$
* 级数收敛的**必要条件**是
  $$\begin{equation}
  \lim_{k\to \infty}w_k(z)=0
  \end{equation}$$
* **级数的部分和**
  $$\begin{equation}
  S_n(z)=\sum_{k=1}^{n}w_k
  \end{equation}$$
* 级数在其定义域内某点z的极限$\lim_{n\to \infty}S_n(z)$存在，则称级数在z点收敛，否则为发散
* **收敛区间**
  级数所有收敛点的集合$\Omega$称为级数的**收敛区间**
* **绝对收敛**
  若级数每一项的模长构成的级数在z点(或者$\Omega$)上收敛，则称级数$\sum_{k=1}^{\infty}w_k(z)$在z点(或$\Omega$)上**绝对收敛**
* **一致收敛**
  设级数的收敛区间为$\Omega$，对于任意给定的$\varepsilon>0$，存在与z无关的正整数N，使得当n>N时，级数的部分和满足
  $$\begin{equation}
  |S(z)-S_n(z)|<\varepsilon
  \end{equation}$$
  则称级数在$\Omega$上**一致连续**
* 级数的绝对收敛与一致收敛是两个不同的概念，**绝对收敛不一定一致收敛，一致收敛不一定绝对收敛**，但绝对收敛的级数必定收敛
* 级数绝对收敛的判别法
  1. **达朗贝尔(d'Alembert)判别法**
     * 对级数$\sum_{k=1}^{\infty}w_k(z)$，当
       $$\begin{equation}
       \lim_{k\to \infty}|\frac{w_{k+1}}{w_k}|=p
       \end{equation}$$
     * 当p<1时，级数绝对收敛
       当p>1时，级数发散
       当p=1时，无法判读
  2. **柯西(Cauchy)判别法**
     * 对级数$\sum_{k=1}^{\infty}w_k(z)$，当
       $$\begin{equation}
       \sqrt[k]{|w_k|}=p
       \end{equation}$$
    * 当p<1时，级数绝对收敛
      当p>1时，级数发散
      当p=1时，无法判读
* 级数一致收敛的判别法
  1. **魏尔斯特拉斯判别法**
     * 在级数$\sum_{k=1}^{\infty}$的收敛区域$\Omega$内，若存在与z无关的$a_k$，当
       $$\begin{equation}
       |w_k(z)|<a_k
       \end{equation}$$
       且级数收敛，则级数在$\Omega$内**绝对且一致收敛** 
## §    解析函数的泰勒展开
* **定理**
  设$z_0$为f(z)解析区域$\Omega$内的一点，以$z_0$为圆心的圆周C在$\Omega$内，则f(z)可以在C内展开成Taylor级数
  $$\begin{equation}
  f(z)=\sum_{n=0}^{\infty}a_n(z-z_0)^n
  \end{equation}$$
  $$\begin{equation}
  a_n=\frac{f^{(n)(z_0)}}{n!}=\frac{1}{2\pi i}\oint \frac{f(z)}{(z-z_0)^{(n+1)}}\mathrm{dz}
  \end{equation}$$
* 当$z_0=0$时泰勒级数就变更为麦克劳林级数
* **收敛半径R**
  $$\begin{equation}
  R=\lim_{n\to \infty}|\frac{a_n}{a_{n+1}}|
  \end{equation}$$
* **重要提示**
  由于复变函数是黎曼面到复数平面的映射，因此当所需展开的函数存在枝点时，要选择展开点所在的那一叶黎曼面进行展开，割线的构造应当避开以指定展开点为圆心，展开点到之间之间的距离为半径的圆.若选择的展开点就是枝点，则不能在该点进行泰勒展开
## §    泰勒展开的理论应用
* **最大模定理**
  * 任何解析函数f(z)的模的最大值只能在其解析区域的边界上达到，除非f(z)为常数，否则在解析区域内部不可能取得最大模长

* **刘维尔(Liouville)定理**
  * 在全平面内解析且非奇异(说明有界)的函数是常值函数

## §    解析函数的洛朗(Laurent)展开
* **复变函数的零点和奇点**
  * 函数f(z)在z=$z_0$点，有$f(z_0)=0$，则称$z_0$为函数的**零点**.若$\frac{f(z)}{(z-z_0)^k}$是非零的解析函数，则称$z_0$为函数f(z)的k阶零点
  * 函数f(z)在z=$z_0$点的导数不存在或不唯一，则$z_0$点称为函数f(z)的**奇点**
* 函数奇点的分类
  1. 孤立奇点
     若$z_0$为函数f(z)的奇点，而在此点处的任意小邻域内，函数f(z)解析，则称$z_0$为f(z)的**孤立奇点**
  2. 非孤立奇点
     若$z_0$为函数f(z)的奇点，而在$z_0$点的任意小邻域内，除了该点还存在其他奇点，则称$z_0$为**非孤立奇点**
* 孤立奇点的分类
  1. 极点
     $z_0$为函数f(z)的孤立奇点，若存在一个正整数k，使得$(z-z_0)^kf(z)$为非零的解析函数，则称$z_0$为f(z)的k阶**极点**.即f(z)具有$(z-z_0)$的最高负幂次项为$(z-z_0)^{-k}$.
  2. 本性奇点
     $z_0$为f(z)的孤立奇点，若不存在一个正整数k，使得$(z-z_0)^kf(z)$为非零的解析函数，则称$z_0$为f(z)的**本性奇点**.即f(z)具有$(z-z_0)$的无穷负幂次项
  3. 可去奇点
     $z_0$为f(z)的孤立奇点，f(z)在$z_0$的定义域没有确定值，但f(z)在$z_0$的邻域内解析，此时可以重新定义$z_0$点的极限值就为其函数值使得在该点处解析，则称该点为**可去奇点**
* **解析函数的洛朗展开**
  * **解析函数的洛朗展开定理**
    函数f(z)在以$z_0$为圆心，半径为$R_1,R_2$的两个圆周$C_1,C_2$所包围的环形区域上解析$(R_1>R_2,C_2\in C_1)$，则在此区域内f(z)可展成Laurent级数
    $$\begin{equation}
    f(z)=\sum_{n=-\infty}^{\infty}a_n(z-z_0)^n
    \end{equation}$$
    $$\begin{equation}
    a_n=\frac{1}{z\pi i}\oint_C\frac{f(\xi)}{(\xi-z_0)^{n+1}}\mathrm{d\xi}
    \end{equation}$$  
    C是任意一条在环形区域内把$C_2$包围在内的闭合曲线
  * 对于一个函数的洛朗展开，其$n\ge 0$的幂级数部分在$z_0$点的邻域内(此邻域内不存在其他奇点)称为洛朗展开式的**正则部分**；对洛朗展开式中n<0的幂级数部分正反映f(z)在$z_0$点的奇异性。我们称这一部分为洛朗展开的**主部**，展开式的最高负幂次反映$z_0$的奇点类型 

***
# 留数定理及其在实积分中的应用
## §    留数定理
* **一：留数的定义** 
  * 考虑函数f(z)在其孤立奇点$z_0$附近作Laurent展开，当我们以一个以$z_0$为圆心，r为半径的圆周C作积分时(C中只存在$z_0$这一个孤立点)
  $$\begin{equation}
  \oint_Cf(z)\mathrm{dz}=\sum_{n=-\infty}^{\infty}\oint_C a_n(z-z_0)^n\mathrm{dz}
  \end{equation}$$
  $$\begin{equation}
  z-z_0=re^{i\theta}
  \end{equation}$$
  $$\begin{equation}
  \oint_Cf(z)\mathrm{dz}=\sum_{n=-\infty}^{\infty}\int_0^{2\pi} a_nir^{n+1}e^{i(n+1)\theta}\mathrm{d\theta}
  \end{equation}$$
  $$\begin{aligned}
   & = \sum_{-\infty}^{\infty}a_nir^{n+1}2\pi\delta_{n,-1} \\
   & = 2\pi ia_{-1} 
  \end{aligned}$$
  $$\begin{equation}
   \int_0^{2\pi}e^{i(n+m)\theta}\mathrm{d\theta}=2\pi\delta_{n,-m}
  \end{equation}$$
  * 式$(87)$表明f(z)在包含有单一孤立奇点$z_0$的回路积分值等于f(z)在$z_0$点的洛朗展开$(z-z_0)^{-1}$项的系数$a_{-1}$乘以$2\pi i$ 
  * 我们定义**f(z)在$z_0$点的留数为$a_{-1}$**，记为
    $$\begin{equation}
    Res f(z_0)=a_{-1}
    \end{equation}$$
    $$\begin{equation}
    \oint_Cf(z)\mathrm{dz}=2\pi iRes f(z_0)
    \end{equation}$$
* **二：留数定理**
  * 如果f(z)在回路C所包围的区域内除有限个孤立点外解析，则f(z)沿C的回路积分值等于f(z)在各个孤立点的留数之和乘以$2\pi i$
    $$\begin{equation}
    \oint_Cf(z)\mathrm{dz}=2\pi i\sum_{j=1}^{k}Res f(z_j)
    \end{equation}$$
  * 回过头来看柯西积分公式
    $$\begin{equation}
    \oint_C \frac{f(z)}{z-z_0}\mathrm{dz}=2\pi if(z_0)
    \end{equation}$$
    f(z)在C内解析，f(z)的泰勒展开为
    $$\begin{equation}
    f(z)=f(z_0)+\sum_{n=1}a_n(z-z_0)^n
    \end{equation}$$
    故被积函数可以表征为
    $$\begin{equation}
    \frac{f(z)}{z-z_0}=\frac{f(z_0)}{z-z_0}+\sum_{n=1}a_n(z-z_0)^{n-1}
    \end{equation}$$
    这正是f(z)的洛朗展开，并能注意到$f(z_0)=a_{-1}$
## §    留数的一般求法
1. 直接把函数在$z_0$点洛朗展开得到$a_{-1}$
2. 如果$z_0$为函数f(z)的一阶极点，则f(z)在$z_0$的洛朗展开为
   $$\begin{equation}
   f(z)=\frac{a_{-1}}{z-z_0}+\sum_{n=1}a_n(z-z_0)^n
   \end{equation}$$
   留数为
   $$\begin{equation}
   a_{-1}=[(z-z_0)f(z)]_{z=z_0}
   \end{equation}$$
3. 当$z_0$为f(z)的m阶极点，则f(z)的洛朗展开为
   $$\begin{equation}
   f(z)=\sum_{n=-m}a_n(z-z_0)^n
   \end{equation}$$
   $$\begin{equation}
   (z-z_0)^mf(z)=\sum_{n=-m}a_n(z-z_0)^{n+m}
   \end{equation}$$
   $$\begin{equation}
   \frac{\mathrm{d^{m-1}}}{\mathrm{dz^{m-1}}}[(z-z_0)^mf(z)]=(m-1)!a_{-1}+\sum_{n=0}\frac{(m+n)!}{(n+1)!}a_n(z-z_0)^{n+1}
   \end{equation}$$
   $$\begin{equation}
   Res f(z_0)=\frac{1}{(m-1)!}\lim_{z\to z_0}\frac{\mathrm{d^{m-1}}}{\mathrm{dz^{m-1}}}[(z-z_0)^mf(z)]
   \end{equation}$$
4. 如果函数f(z)=h(z)/g(z)，$z_0$为f(z)的一阶极点，即$g(z_0)=0$，且h(z)和g(z)在点$z_0$及其邻域解析，则留数可以表示为
   $$\begin{equation}
   Res f(z_0)=\frac{h(z_0)}{g'(z_0)}
   \end{equation}$$

## §    解析函数在无穷远点的留数
* 函数f(z)在无穷远点的邻域内解析，则函数在无穷远点的留数定义如下，其中C为绕无穷远点的任一回路，其方向为**顺时针**方向，在C内除无穷远点外f(z)解析
  $$\begin{equation}
  Res f(\infty)=\frac{1}{2\pi i}\oint_Cf(z)\mathrm{dz}
  \end{equation}$$
  $$\begin{aligned}
   & =\frac{1}{2\pi i}\oint_Cf(z)\mathrm{dz} \\
   & =\frac{1}{2\pi i}\sum_{n=-\infty}^{\infty}C_n\oint z^n\mathrm{dz} \\
   & = -\frac{1}{2\pi i}\sum_{n=-\infty}^{\infty}C_n\oint z^n\mathrm{dz} \quad C逆时针绕行\\
   & =-\sum_{-\infty}^{\infty}C_n\delta_{n,-1} \\
   & =-C_{-1}
  \end{aligned}$$

* **定理**
  若函数f(z)在包含无穷远点的全复平面上只有有限个孤立奇点，则全复平面内的留数之和为零
  该定理告诉我们，当函数f(z)沿闭合回路C的积分为零时，不能说明f(z)在C内全域解析，当环路C中包含有全部的有限个孤立点时，环路积分为零

## §    留数定理在实积分中的应用
* **一：奇异积分(瑕积分))的Cauchy主值问题**
  - 定义
    设积分$\int_{a}^{b}f(x)\mathrm{dx}$的被积函数f(x)在$x_0\in(a,b)$奇异(即瑕积分)，若积分$\lim_{\delta\to 0}\big(\int_{a}^{x_0-\delta}f(x)\mathrm{dx}+\int_{x_0+\delta}^{b}f(x)\mathrm{{dx}}\big)$存在，则称此积分为$\int_{a}^{b}f(x)\mathrm{dx}$的Cauchy主值，记为
    $$\begin{equation}
    P\int_{a}^{b}f(x)\mathrm{dx}=\lim_{\delta\to 0}\big(\int_{a}^{x_0-\delta}f(x)\mathrm{dx}+\int_{x_0+\delta}^{b}f(x)\mathrm{{dx}}\big)
    \end{equation}$$

* **二：无穷限的奇异积分的Cauchy主值** 
  1. 实轴上只有一个一阶极点
  设函数f(z)在上半平面上解析，且当$|z|\rightarrow \infty$时$|f(z)|\rightarrow 0$
  $$\begin{equation}
  P\int_{-\infty}^{\infty}\frac{f(x)}{x-\alpha}\mathrm{dx}=i\pi f(\alpha)=i\pi ResF(\alpha)
  \end{equation}$$

  2. 被积函数F(x)在实轴上有有限K个单极点
  设F(x)具有如下形式且函数f(x)在上半平面上解析，且当$|x|\rightarrow \infty$时$|f(x)|\rightarrow 0$
  $$\begin{equation}
  F(x)=\frac{f(x)}{(x-\alpha_1)\cdots(x-\alpha_k)}
  \end{equation}$$ 
  $$\begin{equation}
  P\int_{-\infty}^{\infty}F(x)\mathrm{dx}=i\pi\sum_{j=1}^{k}ResF(\alpha_j)
  \end{equation}$$
  $$\begin{aligned}
   =i\pi\sum_{j=1}^{k}\frac{f(\alpha_j)}{(\alpha_j-\alpha_1)\cdots(\alpha_j-\alpha_k)}
  \end{aligned}$$

  3. （未命名）
  对于这类积分，我们把被积分函数F(x)变为F(z)，要求F(z)满足
    3.1 F(z)在上半复平面上除有有限个孤立奇点$z_i$外解析
    3.2 当$|z|\rightarrow\infty$时，对$0\le\arg z\le \pi$，有zF(z)一致趋于零
    3.3 F(z)在实轴上只有有限个单极点$\alpha_j$
  $$\begin{equation}
  P\int_{-\infty}^{\infty}F(x)\mathrm{dx}=2i\pi\sum_{i=1}^{m}Res F(z_i)+i\pi\sum_{j=1}^{k}Res F(\alpha_j)
  \end{equation}$$ 

* **三：约当引理**
  * Jordan约当引理
  函数f(z)除在上半复平面上有有限个孤立奇点和在实轴上有有限个单极点外解析，并且当$|z|\rightarrow \infty$，有$|f(z)|\le M(R)\rightarrow 0$，$C_R$为以原点为圆心，以R为半径的半圆周，所有上半复平面的孤立奇点都包含在$C_R$与实轴围成的区域内，则
  $$\begin{equation}
  J=\lim_{R\rightarrow \infty}\int_{C_R}f(z)e^{imz}\mathrm{dz}\rightarrow 0,\quad m>0
  \end{equation}$$

## §    希尔伯特变换
* 在数学物理中，常会遇到一类定义在实轴上的复变函数：f(x)=u+iv，且当$x\rightarrow z$时，f(z)在包括实轴的上复半平面上解析，且有$\lim_{|z|\to \infty}f(z)\rightarrow 0$.询问其实部如何由虚部表示，就涉及到**希尔伯特变换**，也称为**色散关系**.
  $$\begin{equation}
  Ref(x_0)=\frac{1}{\pi}P\int_{-\infty}^{\infty}\frac{Imf(x)}{x-x_0}\mathrm{dx}
  \end{equation}$$

  $$\begin{equation}
  Imf(x_0)=-\frac{1}{\pi}P\int_{-\infty}^{\infty}\frac{Ref(x)}{x-x_0}\mathrm{dx}
  \end{equation}$$
* 希尔伯特变换，即色散关系，给出复函数f(x)在点$x_0$的值的实部或虚部分别由f(x)的虚部或实部的积分表达式

***
# 积分变换与狄拉克函数
* 在物理学中，我们常遇到如下的积分形式
  $$\begin{equation}
  F(\alpha)=\int_{a}^{b}f(x)k(\alpha,x)\mathrm{dx}
  \end{equation}$$
  函数$F(\alpha)$称为由变换核$k(\alpha,x)$产生的函数f(x)的积分变换,$k(\alpha,x)$称为f(x)的积分变换核
* 常见的积分变换类型
  1. **Fourier傅里叶变换**
  2. **Laplace拉普拉斯变换**
  3. **Mellin梅林变换**
  4. **Fourier-Bessel傅里叶-贝塞尔变换**

***
# 傅里叶变换
## §    傅里叶级数
$$\begin{equation}
\frac{1}{\pi}\int_{-\pi}^{\pi}\sin(nx)\sin(mx)\mathrm{dx}=\delta_{n,m}
\end{equation}$$

$$\begin{equation}
\frac{1}{\pi}\int_{-\pi}^{\pi}\cos(nx)\cos(mx)\mathrm{dx}=\delta_{n,m}
\end{equation}$$

$$\begin{equation}
\frac{1}{\pi}\int_{-\pi}^{\pi}\sin(nx)\cos(mx)\mathrm{dx}=0
\end{equation}$$
* 我们知道三角函数族$[\sin(nx),\cos(nx)|n=0,1,2\cdots]$是一个完备的正交函数族，他们可以作为基向量张成一个向量空间，此向量空间称为**Hilbert希尔伯特空间**，空间中的元素是以$2\pi$为周期的实函数
* 任意一个以$2\pi$为周期的实函数f(x)且满足Dirichlet条件，即在$[-\pi,\pi]$区间内允许存在有限个第一类间断点，而且可将此区间分成有限个部分，在每一个部分上f(x)单调变化，则此f(x)为这一Hilbert希尔伯特空间中的一个元素，它可以在这一组基底中展开为傅里叶级数
  $$\begin{equation}
  f(x)=\sum_{k=0}^{\infty}(a_k\cos(kx)+b_k\sin(kx))
  \end{equation}$$

  $$\begin{equation}
  a_k=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)cos(kx)\mathrm{dx} ,\quad k=0,1,\cdots
  \end{equation}$$

  $$\begin{equation}
  b_k=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\sin(kx)\mathrm{dx} ,\quad k=0,1,\cdots
  \end{equation}$$
  * 显然当f(x)为奇函数时$a_k\equiv0$，f(x)为偶函数时$b_k\equiv 0$
* 如果f(x)是以2l为周期的函数(乘以周期因子$\frac{\pi}{l}$)
  $$\begin{equation}
  f(x)=\sum_{k=0}^{\infty}(a_k\cos(\frac{k\pi x}{l})+b_k\sin(\frac{k\pi x}{l}))
  \end{equation}$$

  $$\begin{equation}
   a_k=\frac{1}{l}\int_{-l}^{l}f(x)cos(\frac{k\pi x}{l})\mathrm{dx} ,\quad k=0,1,\cdots
  \end{equation}$$

  $$\begin{equation}
   b_k=\frac{1}{l}\int_{l}^{l}f(x)\sin(\frac{k\pi x}{l})\mathrm{dx} ,\quad k=0,1,\cdots
  \end{equation}$$
* 根据欧拉公式
  $$\begin{equation}
  e^{imx}=\cos(mx)+i\sin(mx)
  \end{equation}$$
  $$\begin{equation}
  \frac{1}{2\pi}\int_{-\pi}^{\pi}e^{i(m-n)x}\mathrm{dx}=\delta_{m,x}
  \end{equation}$$
  * 由线代知识，显然{$e^{imx},m\in Z$}也是希尔伯特空间的一组基向量，以$2\pi$为周期的函数f(x)在这个基底下的展开式为
  $$\begin{equation}
  f(x)=\sum_{k=-\infty}^{\infty}c_ke^{ikx}
  \end{equation}$$
  $$\begin{equation}
  c_k=\frac{1}{2\pi}\int_{-\pi}^{\pi}f(x)e^{-ikx}\mathrm{dx}
  \end{equation}$$
## §    傅里叶变换
* 周期为2l的函数f(x)在一个周期区间$[-l,l]$上的傅里叶展开为
  $$\begin{equation}
  f(x)=\sum_{m=\infty}^{\infty}C_me^{\frac{im\pi }{l}x}
  \end{equation}$$

  $$\begin{equation}
  C_m=\frac{1}{2l}\int_{-l}^{l}f(x)e^{-\frac{im\pi}{l}x}\mathrm{dx}
  \end{equation}$$
* 于是展开式可以写成
  $$\begin{equation}
  f(x)=\sum_{m=-\infty}^{\infty}\big[\frac{1}{2l}\int_{-l}^{l}f(\xi)e^{-\frac{im\pi}{l}\xi}\mathrm{d\xi}\big]e^{\frac{im\pi}{l}x}
  \end{equation}$$
* 令$k=\frac{m\pi}{l}$,相邻两个k的差为$\Delta k=\frac{\pi}{l}$，上式可以改写成
  $$\begin{equation}
  f(x)=\sum_{m=-\infty}^{\infty}[\frac{1}{2\pi}\int_{-l}^{l}f(\xi)e^{-ik\xi}\mathrm{d\xi}]e^{ikx}\Delta k
  \end{equation}$$
* 当$l\rightarrow \infty$
  $$\begin{equation}
  f(x)=\frac{1}{2\pi}\int_{-\infty}^{\infty}C_ke^{ikx}\mathrm{dk}
  \end{equation}$$
  $$\begin{equation}
  C_k=\int_{-l}^{l}f(\xi)e^{-ik\xi}\mathrm{d\xi}
  \end{equation}$$

* 上式就是周期为无穷大，也就是不存在周期的函数的傅里叶积分表达式，也称为**傅里叶变换公式**，$C(k)$称为f(x)的**傅里叶变换**，也称为f(x)的傅里叶变换的**像函数**，记为$C(k)\equiv F[f(x)]$，$f(x)$称为$C(k)$的傅里叶变换的**原函数**
* 
* **傅里叶变换的条件**
  满足以下性质的函数f(x)可以进行傅里叶变换
  1. f(x)为定义在整个实数上的实函数
  2. f(x)在任意区间上满足Dirichlet条件
  3. |f(x)|在全定义域上的积分收敛
  
* **三维空间的傅里叶变换**
  $$\begin{equation}
   f(\vec{r})=\frac{1}{(2\pi)^3}\int_{-\infty}^{\infty}C(\vec{k})e^{i\vec{k}\cdot r}\mathrm{d\vec{k}}
  \end{equation}$$

  $$\begin{equation}
  C(\vec{k})=\int_{-\infty}^{\infty}f(\vec{r})e^{-i\vec{k}\cdot r}\mathrm{d\vec{r}}
  \end{equation}$$
  * $\vec{k}$为三维笛卡尔空间(即欧氏空间)的矢量
    $$\begin{equation}
    \vec{k}=k_1\vec{e_1}+k_2\vec{e_2}+k_2\vec{e_3}
    \end{equation}$$
    $$\begin{equation}
    d\vec{k}=dk_1dk_2dk_3
    \end{equation}$$
## §    傅里叶变换的基本性质
* **一：线性定理**
  设$\alpha_1,\alpha_2$为任意常数
  $$\begin{equation}
  F[\alpha_1f_1(x)+\alpha_2f_2(x)]=\alpha_1F[f_1(x)]+\alpha_2F(f_2(x))
  \end{equation}$$
* **二：延迟定理**
  $$\begin{equation}
  F[f(x-x_0)]=e^{-ikx_0}F[f(x)]
  \end{equation}$$
* **三：位移定理**
  $$\begin{equation}
  F(f(x)e^{ik_0x})=C(k-k_0)
  \end{equation}$$
* **四：梯度变换定理**
  $$\begin{equation}
  F[f(\alpha x)]=\frac{1}{|\alpha|}C(\frac{k}{\alpha})
  \end{equation}$$
* **五：微分定理**
  当函数f(x)具有性质：$|x|\rightarrow \infty$时，$f(x)\rightarrow 0$，则有
  $$\begin{equation}
  F[f'(x)]=ikF[f(x)]
  \end{equation}$$
  $$\begin{equation}
  F[f^{(n)}(x)]=(ik)^nF[f(x)]
  \end{equation}$$
  * **定理**
  $$\begin{equation}
  F[\int_{-\infty}^{x}f(\xi)\mathrm{d\xi}]=\frac{1}{ik}F[f(x)]
  \end{equation}$$
   $$\begin{equation}
  F[\int_{x}^{\infty}f(\xi)\mathrm{d\xi}]=\frac{i}{k}F[f(x)]
  \end{equation}$$
* **六：卷积定理**
  $$\begin{equation}
  F[f_1(x)\star f_2(x)]=F[f_1(x)]F[f_2(x)]
  \end{equation}$$
  $$\begin{equation}
  f_1(x)\star f_2(x)\equiv \int_{-\infty}^{\infty}f_1(x-\xi)f_2(\xi)\mathrm{d\xi}
  \end{equation}$$
  * 两个函数的卷积具有对称性
  

***
# 拉普拉斯变换
## §    Laplace变换
* 对于定义在实变数$t\in [0,\infty)$上的实函数或复函数f(t)，定义f(t)的Laplace变换为
  $$\begin{equation}
  F(p)=\int_0^{\infty}f(t)e^{-pt}\mathrm{dt}
  \end{equation}$$ 
  其中p为复数，$p=s+i\sigma$，$e^{-pt}$称为Laplace变换核，f(t)称为Laplace变换的原函数，F(p)称为Laplace变换的像函数,记为
  $$\begin{equation}
  f(t)\fallingdotseq F(p)
  \end{equation}$$
* Laplace变换与Fourier变换的关系
  $$\begin{equation}
  F(p)=\int_0^{\infty}f(t)e^{-st}e^{i\sigma t}\mathrm{dt}
  \end{equation}$$
  $$g(t)=\begin{cases}
   f(t)e^{-st}, \quad 0\le t\le \infty \\
   0, \quad -\infty\le t\le 0
  \end{cases}$$
  $$\begin{equation}
  F(g(t))=\int_{-\infty}^{\infty}g(t)e^{-i\sigma t}\mathrm{dt}=F(p)
  \end{equation}$$
  * 上式即为f(t)的Laplace变换式
  * g(t)的Fourier变换存在，除要求g(t)满足Drichlet条件外，还需要|g(t)|在$(0,\infty)$上的积分收敛，等价为$|f(t)|\le Me^{s_0t}$，只要当$s>s_0$时，上式就收敛.我们称$s_0$为**收敛横坐标**
## §    $\Gamma$函数及其解析延拓
* $\Gamma$函数的定义
  $$\begin{equation}
  \Gamma(z)=\frac{1}{z}\prod_{n=1}^{\infty}[(1+\frac{z}{n})^{-1}(1+\frac{1}{n})^{z}]
  \end{equation}$$
  $$\begin{aligned}
   & =\lim_{n\to \infty}\frac{1\times2\times\cdots\times n}{z(z+1)\cdots(z+n)}n^z
  \end{aligned}$$
* $\Gamma(z)$的积分定义式
  $$\begin{equation}
  \Gamma(z)\int_0^{\infty}e^{-t}t^{z-1}\mathrm{dt} \quad t\in R
  \end{equation}$$
  对于参数$t\in [0,\infty)$，$\Gamma(z)$在Re z>0时是解析的
* 复变函数的解析延拓
  * 上面我们说$\Gamma$函数只在复平面的右半平面上解析，而z=0是伽马函数的一阶奇点，为此我们将通过解析延拓将解析区域进行扩展
  $$\begin{equation}
  \Gamma(z+1)=\int_0^{\infty}e^{-t}t^{z}\mathrm{dt}
  \end{equation}$$
  $$\begin{aligned}
   & =-t^ze^{-t}\bigg |_{0}^{\infty}+z\int_0^{\infty}e^{-t}t^{z-1}\mathrm{dt} \\
   & =z\Gamma(z) \\
   \Rightarrow \Gamma(z)=\frac{\Gamma(z+1)}{z}
  \end{aligned}$$
  * 通过上式可知z=0为$\Gamma(z)$的一阶极点，因此递推下去就可以得到
  $$\begin{equation}
  \Gamma(z)=\frac{\Gamma(z+n+1)}{z(z+1)\cdots(z+n)}
  \end{equation}$$
  因此$z=0,-1,\cdots,-n$为$\Gamma(z)$的一阶极点，因此我们可以将函数的解析区域延拓到除了上述单极点外的整个复平面，这就是函数的解析延拓
* 复变函数解析延拓的定义
  * 设复变函数$f_1(z)$在$\Omega_1$内解析，$f_2(z)$在$\Omega_2$内解析，在$\Omega_1\cap \Omega_2$内有$f_1(z)=f_2(z)$，则称$f_2(z)$为$f_1(z)$在$\Omega_2$内的解析延拓，反之可以称为$f_1(z)$为$f_2(z)$在$\Omega_1$内的解析延拓，利用上式递推积分可以得到
  $$\begin{equation}
  \Gamma(n+1)=n!
  \end{equation}$$
  $$\begin{equation}
  \Gamma(z)\Gamma(1-z)=\frac{\pi}{\sin(\pi z)}
  \end{equation}$$
  $$\begin{equation}
  \Gamma(z)\Gamma(-z)=\frac{-\pi}{z\sin(\pi z)}
  \end{equation}$$
  $$\begin{equation}
  \Gamma(\frac{1}{2})=\sqrt{\pi}
  \end{equation}$$
  $$\begin{equation}
  \Gamma(n+\frac{1}{2})=\frac{(2n-1)!!}{2^n}\sqrt{\pi}
  \end{equation}$$
  $$\begin{equation}
  \Gamma(z)=\int_{0}^{\infty}t^{2z-1}e^{-t^2}\mathrm{dt}
  \end{equation}$$
## §    Laplace变换的基本性质
* **一：线性定理**
  $$\begin{equation}
  \alpha_1f_1+\alpha_2f_2\fallingdotseq \alpha_1F_1(p)+\alpha_2F_2(p)
  \end{equation}$$
* **二：延迟定理**
  $$\begin{equation}
  f(t-\tau)\fallingdotseq e^{-p\tau}F(p) ,\quad\tau>0
  \end{equation}$$
* **三：位移定理**
  $$\begin{equation}
  e^{-\lambda t}f(t)\fallingdotseq F(p+\lambda)
  \end{equation}$$
* **四：卷积定理**
  $$\begin{equation}
  f_1(t)\star f_2(t)\fallingdotseq F_1(p)F_2(p),\quad t\in[0,\infty)
  \end{equation}$$
* **五：微分定理**
  $$\begin{equation}
  f^{(n)}(t)\fallingdotseq p^nF(p)-\sum_{i=n-1}^{0}p^{i}f^{(n-1-i)}(0)
  \end{equation}$$
  $$\begin{aligned}
   f^{(n)}(t)\fallingdotseq p^{n}F(p)-p^{n-1}f(0)-p^{n-2}f'(0)-\cdots-f^{(n-1)}(0)
  \end{aligned}$$
* **六：标度变换定理**
  $$\begin{equation}
  f(at)\fallingdotseq \frac{1}{a}F(\frac{p}{a}),\quad a>0
  \end{equation}$$
* **七：周期函数变换定理**
  若f(t)=f(t+T)，T为函数的周期，则
  $$\begin{equation}
  f(t)\fallingdotseq \frac{\int_0^{T}f(\tau)e^{-p\tau}\mathrm{d\tau}}{1-e^{pT}}
  \end{equation}$$
## §    Laplace变换的反演
* 利用Laplace变换求解微分方程时，由像函数所满足的代数方程解出像函数的表达式，由像函数利用Laplace变换的基本性质和基本的Laplace变换，可以直接求出原函数，如
  $$\begin{equation}
  1\fallingdotseq\frac{1}{p}
  \end{equation}$$
  $$\begin{equation}
  t^n\fallingdotseq \frac{n!}{p^{n+1}}\fallingdotseq\frac{\Gamma(n+1)}{p^{n+1}}
  \end{equation}$$
  $$\begin{equation}
  e^{at}\fallingdotseq\frac{1}{p-a}
  \end{equation}$$
  $$\begin{equation}
  t^ne^{at}\fallingdotseq\frac{\Gamma(n+1)}{(p-n)^{n+1}}
  \end{equation}$$
  $$\begin{equation}
  \sin(at)\fallingdotseq\frac{a}{p^2+a^2}
  \end{equation}$$
  $$\begin{equation}
  \cos(at)\fallingdotseq\frac{p}{p^2+a^2}
  \end{equation}$$
  $$\begin{equation}
  \sh(at)\fallingdotseq\frac{a}{p^2-a^2}
  \end{equation}$$
  $$\begin{equation}
  \ch(at)\fallingdotseq\frac{p}{p^2-a^2}
  \end{equation}$$
  $$\begin{equation}
  \frac{1}{\sqrt{\pi t}}=\frac{1}{\sqrt{p}}
  \end{equation}$$
* 对像函数的求导公式
  $$\begin{equation}
  F^{(n)}(p)\risingdotseq (-1)^nt^nf(t)
  \end{equation}$$
* 对像函数的积分公式
  $$\begin{equation}
  \int_p^{\infty}F(p)\mathrm{dp}\risingdotseq\frac{f(t)}{t}
  \end{equation}$$

## §    Laplace变换的应用
* Laplace变换通常用来解具有初值问题的常微分方程和偏微分方程.它把微分方程的求解问题，变成方程解的像函数的代数方程的求解问题，由代数方程解出像函数，再通过Laplace变换的反演得出像函数的原函数，也就是微分方程的解

***
# $\delta$函数
## §    $\delta$函数的定义
* 定义
  $\delta$函数是定义在$(-\infty,\infty)$区间上的一个函数，对于某一点$x_0$，有
  $$\delta(x-x_0)=\begin{cases}
   0 \quad x\neq x_0\\
   \infty \quad x=x_0
  \end{cases}$$
  $$\int_a^b\delta(x-x_0)\mathrm{dx}=\begin{cases}
   1 \quad x_0\in(a,b)\\
   0 \quad x_0\notin(a,b)
  \end{cases}$$
## §    $\delta$函数的性质
* 1. 对于连续函数f(x)
  $$\begin{equation}
  \int_{-\infty}^{\infty}f(x)\delta(x-x_0)\mathrm{dx}=f(x_0)
  \end{equation}$$
* 2. $\delta$函数为偶函数
* 3. $\delta$函数满足
  $$\begin{equation}
  f(x)\delta(x-x_0)=f(x_0)\delta(x-x_0)
  \end{equation}$$
* 4. $\delta$函数满足
  $$\begin{equation}
  x\delta(x)=0
  \end{equation}$$
* 5. 性质1.的推广
  $$\begin{equation}
  \int_{-\infty}^{\infty}\delta(x-x_1)\delta(x-x_2)\mathrm{dx}=\delta(x_1-x_2)
  \end{equation}$$
* 6. $\delta$函数满足
  $$\begin{equation}
  \delta(\varphi(x))=\sum_{i=1}^{k}\frac{1}{|\varphi'(x_i)|}\delta(x-x_i)
  \end{equation}$$
  其中$x_i$为函数$\varphi(x)=0$的单根，$\varphi'(x_i)$为在各个单根处的导数值
## §    $\delta$函数的导数
* 由于$\delta$函数是广义函数，故其导数不是在一般数学意义下的导数.而是作为带参数的连续函数的极限引入的
* 1. 带参数的连续函数
  $$\begin{equation}
  \delta'(x) =\lim_{a\to 0}\frac{\partial \delta(x,a)}{\partial x}
  \end{equation}$$
  $$=\begin{cases}
   0\quad x\neq 0\\
   \infty \quad x=0
  \end{cases}$$
* 2. $\delta$函数的导数在积分运算中作为被积函数
  $$\begin{equation}
  \int_a^bf(x)\delta(x-x_0)\mathrm{dx}=-f'(x_0) \quad x_0\in(a,b)
  \end{equation}$$
* 3. $\delta$函数的导数为奇函数
* 4. $\delta$函数的n阶导数
  $$\begin{equation}
  \delta^{(n)}(x-x_0)=\frac{\partial }{\partial x}\delta^{(n-1)}(x-x_0)
  \end{equation}$$
  $$\begin{equation}
  \int_a^bf(x)\delta^{(n)}(x-x_0)\mathrm{dx}=(-1)^nf^{(n)}(x_0)\quad x_0\in(a,b)
  \end{equation}$$

## §    三维$\delta$函数
* 定义
  $$\delta(r-r_0)=\begin{cases}
   0 \quad r\neq r_0\\
   \infty \quad r=r_0
  \end{cases}$$
  $$\begin{equation}
  \int_V\delta(r-r_0)\mathrm{dr}=1 \quad r_0\in V
  \end{equation}$$
* 在不同坐标系中的形式(坐标变换&度量因子)
  1. 笛卡尔坐标系
  $$\begin{equation}
  \delta(r-r_0)=\delta(x-x_0)\delta(y-y_0)\delta(z-z_0)
  \end{equation}$$
  2. 球坐标系
  $$\begin{equation}
  \delta(r-r_0)=\frac{1}{\rho^2\sin\theta}\delta(\rho-\rho_0)\delta(\theta-\theta_0)\delta(\varphi-\varphi_0)
  \end{equation}$$
  3. 柱坐标系
  $$\begin{equation}
  \delta(r-r_0)=\frac{1}{\rho}\delta(\rho-\rho_0)\delta(\varphi-\varphi_0)\delta(z-z_0)
  \end{equation}$$
  [点我传送：Coordinate transformation](https://ustc-nku.github.io/2021/10/11/Coordinate%20transformation/)
* **三维$\delta$函数的重要表达式**
  $$\begin{equation}
  \delta(\vec{r})=-\frac{1}{4\pi}\nabla^2\frac{1}{r}
  \end{equation}$$
## §    $\delta$函数的傅里叶变换和傅里叶展开
* $\delta$函数的傅里叶变换
  由函数的傅里叶变换
  $$\begin{equation}
  f(x)=\frac{1}{2\pi}\int_{-\infty}^{\infty}C(k)e^{ikx}\mathrm{dk}
  \end{equation}$$
  $$\begin{equation}
  C(k)=\int_{-\infty}^{\infty}f(x)e^{-ikx}\mathrm{dx}
  \end{equation}$$
  $$\begin{aligned}
  f(x)&=\frac{1}{2\pi}\int_{-\infty}^{\infty}[\int_{-\infty}^{\infty}f(x')e^{-ikx'}\mathrm{dx'}]e^{ikx}\mathrm{dk} \\
  &=\frac{1}{2\pi}\int_{-\infty}^{\infty}f(x')[\int_{-\infty}^{\infty}e^{ik(x-x')}\mathrm{dk}]\mathrm{dx'}
  \end{aligned}$$
  * 由狄拉克函数的性质
  $$\begin{equation}
  f(x)=\int_{-\infty}^{\infty}f(x')\delta(x-x')\mathrm{dx'}
  \end{equation}$$
  $$\begin{equation}
  \delta(x-x')=\frac{1}{2\pi}\int_{-\infty}^{\infty}e^{ik(x-x')}\mathrm{dk}
  \end{equation}$$
  **上式正是狄拉克函数的傅里叶变换式**
  * 狄拉克函数傅里叶变换的像函数为
  $$\begin{equation}
  C(k)=F[\delta(x-x')]=\int_{-\infty}^{\infty}\delta(x-x')e^{-ik(x-x')}\mathrm{dx}=1
  \end{equation}$$
  * 三维狄拉克函数的傅里叶变换公式
  $$\begin{equation}
  \delta(r-r')=\frac{1}{(2\pi)^3}\int_{-\infty}^{\infty}e^{ik(r-r')}\mathrm{dk}
  \end{equation}$$
  * **帕萨瓦Parseval关系式**
  $$\begin{equation}
  \int_{-\infty}^{\infty}f(x)g^{\star}(x)\mathrm{dx}=\frac{1}{2\pi}\int_{-\infty}^{\infty}F(k)G^{\star}(k)\mathrm{dk}
  \end{equation}$$
  其中f(x),g(x)的傅里叶变换为
  $$\begin{equation}
  f(x)=\frac{1}{2\pi}\int_{-\infty}^{\infty}F(k)e^{ikx}\mathrm{dk}
  \end{equation}$$
  $$\begin{equation}
  g(x)=\frac{1}{2\pi}\int_{-\infty}^{\infty}G(k)e^{ikx}\mathrm{dk}
  \end{equation}$$
  g(x)的复共轭函数$g^{\star}(x)$的傅里叶变换为
  $$\begin{equation}
  g^{\star}(x)=\frac{1}{2\pi}\int_{-\infty}^{\infty}G^{\star}(x)e^{-ikx}\mathrm{dk}
  \end{equation}$$

* $\delta$函数的傅里叶级数展开
  * 设{$\varphi_i(x)$}是向量空间L中的一组正交归一化的函数基底
  $$\begin{equation}
  \int_{-\infty}^{\infty}\frac{1}{2\pi}\varphi_i(x)\varphi_j(x)\mathrm{dx}=\delta_{i,j}
  \end{equation}$$
  则任意函数可在该基底上展开
  $$\begin{equation}
  f(x)=\sum_{i=-\infty}^{\infty}C_i\varphi_i(x)
  \end{equation}$$
  $$\begin{equation}
  C_i=\int_{-\infty}^{\infty}f(x)\varphi_i^{\star}(x)\mathrm{dx}
  \end{equation}$$
  $$\begin{aligned}
   f(x) &=\sum_{i=-\infty}^{\infty}[\int_{-\infty}^{\infty}f(x')\varphi_i^{\star}(x')\mathrm{dx'}]\varphi_i(x) \\
   &=\int_{-\infty}^{\infty}f(x')[\sum_{i=-\infty}^{\infty}\varphi_i^{\star}(x)\varphi_i(x)]\mathrm{dx'}
  \end{aligned}$$
  $$\begin{equation}
  \delta(x-x')=\sum_{i=-\infty}^{\infty}\varphi_i^{\star}(x)\varphi_i(x)
  \end{equation}$$
  上式就是狄拉克函数的广义傅里叶级数展开式
---
