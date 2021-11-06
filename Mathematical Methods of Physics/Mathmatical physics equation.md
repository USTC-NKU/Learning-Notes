---
title: Mathematical physics equation
math: true
tags: Complex variable function
categories: Mathematical Methods of Physics
date: 2021-10-30 22:48
author: USTC-elbitsiserri
---
  本文是数学物理方法的第三部分，也是最后一部分.本文的核心议题只有一个——数学物理方程.物理学的研究过程中需要建立诸多物理模型，建立物理模型后需要定量化地得到数学模型.数学模型的建立主要有两种方法，一是根据物理量描述的物理学基本定律搭建体系地微分方程；二是由已经建立的物理模型写出描述物理系统的拉格朗日量或哈密顿量，根据变分原理或哈密顿原理得到体系的方程.本文将分别从这两种方法展入介绍.
***
[toc]
***
<!-- 
# 波动方程、运输方程、泊松方程及其定解问题
## §    二阶线性偏微分方程的普遍形式
- 对于n维线性空间和一维时间坐标$x_0$构成的n+1维空间，其二阶偏微分方程可以表示为
  $$\begin{equation}
  Lu(x_0,x_1,\cdots,x_n)=f(x_0,x_1,\cdots,x_n)
  \end{equation}$$
  式中u表示所要求解的物理场量，右侧f为非齐次项，表示使物理场量u产生变化的外界源的分布，**L为二阶线性偏微分算子**，它具有以下普遍形式
  $$\begin{equation}
  L=a_{ij}(x_0,x_1,\cdots,x_n)\frac{\partial^2 }{\partial x_i\partial x_j }+b_i(x_0,x_1,\cdots,x_n)\frac{\partial }{\partial x_i}+c(x_0,x_1,\cdots,x_n)
  \end{equation}$$
  其中采用爱因斯坦求和法则,i,j=0,1,...
  [点我传送：爱因斯坦求和约定](https://zhuanlan.zhihu.com/p/46006162)
- 线性算子L具有如下性质：若$L_1,L_2$为线性算子，则
  $$\begin{equation}
  \alpha(L_1+L_2)=\alpha L_1+\alpha L_2
  \end{equation}$$
  $$\begin{equation}
  (\alpha+\beta)L=\alpha L+\beta L
  \end{equation}$$
  $$\begin{equation}
  (\alpha\beta)L=\alpha(\beta L)
  \end{equation}$$
- 如果不存在外界源分布的影响，$(1)$式就称为齐次方程，满足解的线性叠加性，这里不再赘述.
- 具体对于研究的三维欧氏空间和一维时间组合成3+1维的时空的物理体系而言
  1. 当算子L的$a_{00}=1$时，$a_{11}=a_{22}=a_{33}=-a^2$，其余交叉项为零，则
     $$\begin{equation}
     L=\frac{\partial^2 }{\partial t^2}-a^2\nabla^2
     \end{equation}$$
     此算子称为**双曲算子**，也称**波动算子**，则方程Lu=f的形式为
     $$\begin{equation}
     u_{tt}-a^2\nabla^2u=f
     \end{equation}$$
     此方程就是双曲方程即波动方程的标准式，a为波速
     **双曲算子即波动算子在时间和空间上具有反演性，因此齐次的波动方程在空间和时间上是可逆的**
  2. 若算子L中的$b_0=1$,$a_{11}=a_{22}=a_{33}=-a^2$，其他的系数全为零，则
     $$\begin{equation}
     L=\frac{\partial }{\partial t}-a^2\nabla^2
     \end{equation}$$
     此算子称为**抛物算子**，也称**运输算子**，则方程的形式为
     $$\begin{equation}
     u_t-a^2\nabla^2u=f
     \end{equation}$$
     此方程就是抛物方程即运输方程的标准式，a为运输系数
     **抛物算子即运输算子在时间上是不对称的，因此运输方程对时间的解是不可逆的**
  3. 若算子L中的$a_{11}=a_{22}=a_{33}=1$，其他系数均为零，则
     $$\begin{equation}
     L=\nabla^2
     \end{equation}$$
     为Laplace算子，方程的形式为
     $$\begin{equation}
     \nabla^2u=f
     \end{equation}$$
     此方程为**椭圆方程**，也称**泊松方程**，它是描述稳定场分布的方程.当f为零时，方程退化为Laplace方程
     $$\begin{equation}
     \nabla^2u=0
     \end{equation}$$
## §    波动方程
* 波动方程的推导
  设有一条长为l，线密度为$\rho$的细弦，让其各点在垂直外力作用下离开平衡位置作微小振动.振动发生在同一平面内，且振幅很小.弦的平衡位置在x轴，左端点为原点，右端点为l，u轴描述各点的位移，弦上任一点在时间的位移为u(x,t).
  取一微元分析，数据标注在下图
  ![波动方程推导图](\pic/波动方程.jpg)
  由于水平方向上不存在运动，故水平方向受力平衡
  $$\begin{equation}
  T_x\cos\alpha-T_{x+\mathrm{dx}}\cos\beta=0
  \end{equation}$$
  振幅很小，做角度近似处理，于是得到
  $$\begin{equation}
  T_x=T_{x+\mathrm{dx}}\equiv T
  \end{equation}$$
  这段微元受到的单位长度的外力可以视为单位长度外力$f_0(x,t)$，作用在一点上，因此竖直方向上的动力学方程为
  $$\begin{equation}
  T_{x+\mathrm{dx}}\sin\beta-T_x\sin\alpha+f_0(x,t)\mathrm{dx}=\rho\mathrm{dx}u_{tt}
  \end{equation}$$
  两个夹角角度趋于零，近似处理，有
  $$\begin{equation}
  \sin\alpha=\tan\alpha=\frac{\partial u}{\partial x}|_{x}
  \end{equation}$$
  $$\begin{equation}
  \sin\beta=\tan\beta=\frac{\partial u}{\partial x}|_{x+\mathrm{dx}}
  \end{equation}$$
  方程变为
  $$\begin{equation}
  T\big(\frac{\partial u}{\partial x}|_{x+\mathrm{dx}}-\frac{\partial u}{\partial x}|_{x} \big)+f_0(x,t)\mathrm{dx}=\rho \mathrm{dx}u_{tt}
  \end{equation}$$
  注意到
  $$\begin{equation}
  \frac{\partial u}{\partial x}|_{x+\mathrm{dx}}-\frac{\partial u}{\partial x}|_{x}=\frac{\partial^2 u}{\partial x^2}\mathrm{dx}
  \end{equation}$$
  $$\begin{equation}
  u_{tt}-\frac{T}{\rho}u_{xx}=\frac{1}{\rho}f_0(x,t),\quad 0<x<l,t>0
  \end{equation}$$
  对比标准的一维波动方程
  $$\begin{equation}
  u_{tt}-a^2u_{xx}=f(x,t)
  \end{equation}$$
  其中$a^2=\frac{T}{\rho}$，a是振动在弦上传播的速度，$f(x,t)=\frac{1}{\rho}f_0(x,t)$称为外力密度，是单位长度单位密度上所施加的外力，一般就称为外力.当外力为零时方程就是一维齐次波动方程.
  当它描述无界弦的运动时，它是弦的自由振动方程.而对于具体弦的运动描述，方程还需要满足**初始条件**和**边界条件**，这些条件称为**方程的定解条件**
- 初始条件
  初始条件即给出我们开始观察的初始时刻，弦上个点的位移分布和速度分布
  $$\begin{equation}
  u(x,0)=\varphi(x) \quad 0\le x\le l
  \end{equation}$$
  $$\begin{equation}
  u_t(x,0)=v(x) \quad 0\le x \le l
  \end{equation}$$
- 边界条件
  边界条件是考虑我们所观察的物理系统以外的环境通过系统的边界对弦施加的作用，它表现在弦的边界点状态的变化上，边界条件一般分为三类
  1. **第一类边界条件**
     已知弦两个端点的位移随时间的变化关系，即边界上场量随时间的变化关系
     $$\begin{equation}
     u_(0,t)=g_1(t) \quad t\ge 0
     \end{equation}$$
     $$\begin{equation}
     u_(l,t)=g_2(t) \quad t\ge 0
     \end{equation}$$
     当$g_1(t)、g_2(t)=0$时，称此弦具有固定端点，即外力将弦两个端点固定，这种边界条件称为**第一类齐次边界条件**，是最基本的边界条件
  2. **第二类边界条件**
     已知弦两个端点的位移u沿x轴的梯度对时间的依赖关系，即场量沿边界的外法向的梯度对时间的依赖关系
     $$\begin{equation}
     -T\frac{\partial u}{\partial x}|_{x=0}=h_1(t)
     \end{equation}$$
     $$\begin{equation}
     T\frac{\partial u}{\partial x}|_{x=l}=h_2(t)
     \end{equation}$$
     负号表示在x = 0点，张力T的方向与偏导数方向相反
     当$h_1(t)、h_2(t)=0$时，即弦的两个端点不受外力的作用，此时弦具有自由端，这种边界条件称为**第二类齐次边界条件**
  3. **第三类边界条件**
     已知弦的两个端点的位移与所受到的垂直于弦的外力的线性组合，视为是第一第二类边界条件的叠加
     $$\begin{equation}
     -T\frac{\partial u}{\partial x}|_{x=0}+a_1u(0,t)=h_1(t) \quad t\ge 0
     \end{equation}$$
     $$\begin{equation}
     T\frac{\partial u}{\partial x}|_{x=l}+a_2u(l,t)=h_2(t) \quad t\ge 0
     \end{equation}$$
     当$h_1(t)、h_2(t)=0$时，此边界条件称为**第三类齐次边界条件**
- 我们把物理体系所遵从的偏微分方程称为**泛定方程**


## §    运输方程
- 运输方程的标准形式为
  $$\begin{equation}
  u_t-a^2\nabla^2u=f(x,y,z,t)
  \end{equation}$$
  它是描述物理上的运输过程(如热传导、扩散等)的运输规律.u(x,y,z,t)表示被运输的物理场量，a为运输系数(如热传导系数、扩散系数等),f(x,y,z,t)是源项.此方程对时间是不可逆的，不具有时间上的对称性
- 热传导方程
  ![热传导方程](\pic/热传导方程.jpg)
  在一个三维空间区域$\Omega$内，有均匀的各向同性的介质，由于区内内的温度场不均匀，将会发生热量从温度高的地方向温度低的地方运输的过程.我们定义**热流强度**q(x,y,z,t)这一物理量，它表示单位时间内通过单位截面积的热量.区域内温度场的分布函数为u(x,y,z,t)，温度的不均匀程度由温度场分布函数的梯度场表征
  根据**傅里叶热传导定律**
  $$\begin{equation}
  \vec{q}=-k\nabla u
  \end{equation}$$
  k为热传导系数，温度梯度的正向是由温度低向温度高的方向，因此热流强度的正向与温度梯度的正向相反，故存在负号
  在上图中，区域$\Omega$内均匀物质的密度$\rho$，比热容为c，在区域内有热源，由热量强度F(x,y,z,t)表征，它表示t时刻在区域中某一点处在单位时间单位体积中产生的热量.当F < 0时表示热量汇集，即吸收热量的源.我们考虑热传导系数k为常数，基于区域中的热量守恒，在单位时间内有
  $$\begin{equation}
  \frac{\partial }{\partial t}\int_{\Omega}c\rho\mathrm{d\Omega}u=\int_{\Omega}F(x,y,z,t)\mathrm{d\Omega}-\int_{\partial\Omega}\vec{q}\mathrm\cdot{d\vec{\sigma}}
  \end{equation}$$
  方程左侧表示在t时刻区域中的热量在单位时间内的变化.方程右侧第一项表示区域内热源在单位时间内产生的热量，右侧第二项表示区内通过边界与外界进行热交换的量
  根据傅里叶热传导定律
  $$\begin{equation}
  -\int_{\partial \Omega}\vec{q}\cdot\mathrm{d\vec{\sigma}}=\int_{\partial\Omega}k\nabla u\cdot\mathrm{d\vec{\sigma}}
  \end{equation}$$
  根据Gauss公式(散度定理)
  $$\begin{equation}
  \int_{\partial\Omega}k\nabla u\cdot\mathrm{d\vec{\sigma}}=\int_{\Omega}k\nabla^2u\cdot\mathrm{d\Omega}
  \end{equation}$$
  热量守恒方程变更为
  $$\begin{equation}
  \int_{\Omega}c\rho \frac{\partial u}{\partial t}\mathrm{d\Omega}-\int_{\Omega}k\nabla^2u\cdot\mathrm{d\Omega}=\int_{\Omega}F(x,y,z,t)\mathrm{d\Omega}
  \end{equation}$$
  即可得到
  $$\begin{equation}
  c\rho\frac{\partial u}{\partial t}-k\nabla^2 u=F(x,y,z,t)
  \end{equation}$$
  对比标准运输方程可以得到$a^2=\frac{k}{c\rho}$,$f=\frac{F}{c\rho}$
- 初始条件
  由于热传导方程中仅仅含有时间的一阶导数项，故初始条件只需要给出在初始时刻区内的温度分布即可
  $$\begin{equation}
  u(x,y,z,0)|_{\Omega}=\varphi()
  \end{equation}$$
- 边界条件
  1. **第一类边界条件**
     已知边界上温度分布随时间的变化关系
     $$\begin{equation}
     u(x,y,z,t)|_{\partial\Omega}=g(\partial\Omega,t)
     \end{equation}$$
     当g = 0时是**第一类齐次边界条件**
  2. **第二类边界条件**
     已知通过边界上的热流强度q的分布随时间的变化关系$h(\partial\Omega,t)$.**由于热量交换只能通过边界的法向才能进行**，热流强度的切向分量是沿界面的切平面方向，不与平面进行热交换
     设n为边界面$\partial\Omega$的外法向，$q_n$表示流出界面的热流强度，$-q_n$表示流入界面的热流强度.根据傅里叶热传导定律，在界面上我们有
     $$\begin{equation}
     -q_n|_{\partial\Omega}=k\frac{\partial u}{\partial n}|_{\partial\Omega}
     \end{equation}$$
     $$\begin{equation}
     则第二类边界条件可以表示为
     -q_n|_{\partial\Omega}=h(\partial\Omega,t)
     \end{equation}$$
     即
     $$\begin{equation}
     \frac{\partial u}{\partial n}|_{\partial\Omega}=\frac{1}{k}h(\partial\Omega,t)
     \end{equation}$$
     若h = 0，此边界条件为**第二类齐次边界条件**
  3. **第三类边界条件**
     第三类边界条件是第一第二类边界条件的线性组合，可由**牛顿冷却定律**描述.当区域内的物质通过边界面自由冷却时，在系统边界与环境的温度相差不大时，通过界面与环境进行热交换，与边界的温度高低有关.
     牛顿热冷却定律
     $$\begin{equation}
     q_n|_{\partial\Omega}=H(u|_{\partial\Omega}-u_0)
     \end{equation}$$
     H > 0称为冷却系数，$u_0$为外界的环境温度，根据傅里叶热传导定律改写上式
     $$\begin{equation}
     -k\frac{\partial u}{\partial n}|_{\partial\Omega}=H(u|_{\partial\Omega}-u_0)
     \end{equation}$$
     即
     $$\begin{equation}
     (\frac{\partial u}{\partial n}+\frac{H}{k}u)|_{\partial\Omega}=\frac{H}{k}u_0
     \end{equation}$$
     此为第三类边界条件的标准形式
     当外界温度为零时，这时的边界条件称为**第三类齐次边界条件**
- 扩散方程
  扩散现象是运输现象的一种
  在半导体工艺中掺杂单晶硅的过程，就是杂志在单晶硅中的扩散过程.扩散定律同傅里叶热传导定律、牛顿冷却定律等均为实验定律，其数学形式为
  $$\begin{equation}
  \vec{q}=-D\nabla u
  \end{equation}$$
  u为扩散物质的浓度分布，q为扩散强度，即单位时间内内通过单位横截面积的扩散量，D为扩散系数
  ![扩散方程](\pic/扩散方程.jpg)
  在半导体工艺中，杂志沿着硅片表面S向垂直于表面的方向进行扩散，具有对称性，我们将之视为一维问题
  一维扩散定律为
  $$\begin{equation}
  q=-D\frac{\partial u}{\partial x}  \quad D>0
  \end{equation}$$
  u(x,t)为杂志的浓度分布，考虑一个线微元，单位时间内杂志的变化量与扩散强度的关系为，扩散由高浓度向低浓度扩散
  $$\begin{equation}
  \frac{\partial u(x,t)}{\partial t}\mathrm{dx}=q(x,t)-q(x+\mathrm{dx},t)
  \end{equation}$$
  由扩散定律可得
  $$\begin{equation}
  D\frac{\partial^2 u(x,t)}{\partial x^2}=\frac{\partial u(x,t)}{\partial t}
  \end{equation}$$
  对比标准扩散方程可知$a^2=D$，三维扩散方程形式为
  $$\begin{equation}
  u_t-a^2\nabla u=f(x,y,z,t)
  \end{equation}$$
  
## §    Poisson泊松方程
- Poisson方程也称为**稳定场方程**，它不含有对时间的微商项，场量不随时间变化，其标准形式为
  $$\begin{equation}
  \nabla^2u(x,y,z)=f(x,y,z)
  \end{equation}$$
  它的场量和源都不含有时间变量，它描述场在空间中的稳定分布.当源f为零时，Poisson方程退化为Laplace方程
  $$\begin{equation}
  \nabla^2u(x,y,z)=0
  \end{equation}$$ 
- Poisson是描述稳定场的，因此它不存在初始条件，只需要边界条件.由于其稳定场的特性，需要对某些条件加以限制
- 边界条件
  1. **第一类边界条件**
     在考虑的区域中，已知稳定场u在区域边界上的值
     $$\begin{equation}
     u|_{\partial\Omega}=g(\partial\Omega)
     \end{equation}$$
  2. **第二类边界条件**
     已知稳定场u在边界法向上的导数的值
     $$\begin{equation}
     \frac{\partial u}{\partial n}|_{\partial\Omega}=g(\partial\Omega)
     \end{equation}$$
     n为边界的外法向.这类边界问题通常称为**Neumann纽曼问题**
  3. **第三类边界条件**
     已知在边界上稳定场u和它的法向导数的某种线性组合
     $$\begin{equation}
     (\alpha u+\beta\frac{\partial u}{\partial n})|_{\partial\Omega}=g(\partial\Omega)
     \end{equation}$$

## §    拉普拉斯方程与调和函数
- Laplace方程的解u称为调和函数.在[点我传送：复变函数和函数变换](https://ustc-nku.github.io/2021/10/13/Complex%20variable%20function%20and%20transformation%20methods/)一文中我们介绍过复变函数中的解析函数满足二维Laplace方程，其实部和虚部满足Cauchy-Riemann条件，这表明其实部和虚部函数都是二维调和函数
- **调和函数的基本性质**
  根据Green格林定理  {如果忘了[点我传送：向量分析](https://ustc-nku.github.io/2021/10/06/Vector%20analysis/)}
  $$\begin{aligned}
   \int_{\Omega}(v\nabla^2 u+\nabla v\nabla u)\mathrm{d\Omega} &=\int_{\partial\Omega}v\nabla u\cdot\mathrm{d\vec{\sigma}} \\
   &=\int_{\partial\Omega} v\frac{\partial u}{\partial n}\mathrm{d\sigma}
  \end{aligned}$$
  $$\begin{aligned}
   \int_{\Omega}(v\nabla^2 u-u\nabla^2 v)\mathrm{d\Omega}=\int_{\partial\Omega}(v\frac{\partial u}{\partial n}-u\frac{\partial v}{\partial n})\mathrm{d\sigma}
  \end{aligned}$$
  我们可以得到调和函数的两个基本性质
  - 在我们观察区域中的调和函数u，其在边界上的法相方向导数在整个边界上的积分为零
    $$\begin{equation}
    \int_{\partial\Omega}\frac{\partial u}{\partial n}\mathrm{d\sigma}=0
    \end{equation}$$
  - **调和函数平均值定理**
    设u(x,y,z)是区域上的调和函数，则u在区域内的一点$P(x_0,y_0,z_0)$的值可以表示为
    $$\begin{equation}
    u_(x_0,y_0,z_0)=\frac{1}{4\pi R^2}\int_{S_R}u\mathrm{d\sigma}
    \end{equation}$$
    其中$S_R$是以P点为圆心，以R为半径的球面，且此球面完全包含在区域中

---
# 分离变量法
## §    齐次方程边界条件下的分离变量法
- 我们以有界弦的自由振动来展开介绍
  考虑长度为l的两端固定的弦满足的波动方程和初值、边界条件
  $$\begin{cases}
  u_{tt}-a^2u_{xx}=0 \quad (0<x<l,t>0)       \\\\
  u(0,t)=u(l,t)=0    \quad (t>0)     \\\\
  u(x,0)=\varphi(x)  \quad (0<x<l)      \\\\
  u_{t}(x,o)=v(x)    \quad (0<x<l)    
  \end{cases}$$
  用分离变量法，设u(x,t)可以表示为
  $$\begin{equation}
  u(x,t)=X(x)T(t)
  \end{equation}$$
  带入方程可以得到
  $$\begin{equation}
  \frac{T''}{a^2 T}=\frac{X''}{X}
  \end{equation}$$
  此方程左端只是时间的函数，右端只是位置的函数，两边在其各自定义域上始终相等，则只能为常数$-\lambda$，$\lambda\ge 0$.注意，如果将方程两端的常数设置为等于$\lambda$而不是$-\lambda$，($\lambda\ge 0$)，方程的解不能满足端点为零的条件
  $$\begin{equation}
  T''+a^2\lambda T=0
  \end{equation}$$
  $$\begin{equation}
  X''+\lambda X=0
  \end{equation}$$
  齐次边界条件在分离变量下变更为
  $$\begin{equation}
  X(0)T(t)=X(l)T(t)=0
  \end{equation}$$
  要求微分方程的解u具有非平凡解，即具有非零解，则必然在端点处要求为零
  $$\begin{equation}
  X(0)=X(l)=0
  \end{equation}$$
  因此我们得到了X(x)所满足的常微分方程及其边界条件的方程组
  $$\begin{cases}
  X''+\lambda X=0    \\\\
  X(0)=X(l)=0
  \end{cases}$$
  利用高等数学的基础知识，容易得到方程的解为
  $$\begin{equation}
    X(x)=C\sin\sqrt{\lambda}x+D\cos\sqrt{\lambda}x
  \end{equation}$$
  由边界条件X(0)=0可得D=0
  由边界条件X(l)=0可得$\sqrt{\lambda}l=n\pi,n\in N^{+}$，因此$\lambda$只能取一系列特定的值，称为**本征值**，每个本征值对应的解称为**本征函数**
  $$\begin{equation}
  X_n(x)=C\sin\frac{n\pi}{l}x ,\quad n\in N^{+}
  \end{equation}$$
  因此T(t)的通解为
  $$\begin{equation}
  T_n=A_n\sin a\frac{n\pi}{l}t+B_n\cos a\frac{n\pi}{l}t ,\quad n\in N^{+}
  \end{equation}$$
  若令$\omega_n=\frac{an\pi}{l}$，称为**本征频率**
  对于每个特定的本征值，其**本征解**为
  $$\begin{equation}
  u_n(x,t)=(A_n\sin\frac{an\pi}{l}t+ B_n\cos\frac{an\pi}{l}t)\sin\frac{n\pi}{l}x ,\quad n\in N^{+}
  \end{equation}$$
  其中积分常数$A_n、B_n$由初始条件确定
  因此原微分方程的解即为这些本征解的线性叠加
  $$\begin{equation}
  u(x,t)=\sum_{n=1}^{\infty}u_n(x,t)
  \end{equation}$$
  现在来确定各个积分常数.应当注意到X(x)表达式的三角函数系是一个完备正交系，这一点我们之前多次提及过.由于初始条件中的$\varphi(x)、v(x)$都是定义在区间[0，l]上的函数，故可在安备的正交函数系{$X_n(x)$}上作Fourier展开
  $$\begin{equation}
  \varphi(x)=\sum_{n=1}^{\infty}\varphi_n\sin\frac{n\pi}{l}x
  \end{equation}$$
  $$\begin{equation}
  v(x)=\sum_{n=1}^{\infty}v_n\sin\frac{n\pi}{l}x
  \end{equation}$$
  他们的展开式系数分别为
  $$\begin{equation}
  \varphi_n=\frac{2}{l}\int_{0}^{l}\varphi(x)\sin\frac{n\pi}{l}x\mathrm{dx}
  \end{equation}$$
  $$\begin{equation}
  v_n=\frac{2}{l}\int_{0}^{l}v(x)\sin\frac{n\pi}{l}x\mathrm{dx}
  \end{equation}$$
  由其初始条件可以得到下列方程
  $$\begin{equation}
  \varphi(x)=u(x,0)=\sum_{n=1}^{\infty}B_n\sin\frac{n\pi}{l}x
  \end{equation}$$
  $$\begin{equation}
  v(x)=u_t(x,0)=\sum_{n=1}^{\infty}\frac{an\pi}{l}A_n\sin\frac{n\pi}{l}x
  \end{equation}$$
  对照，可以得到积分系数的表达式
  $$\begin{equation}
  A_n=\frac{2}{an\pi}\int_{0}^{l}\varphi(x)\sin\frac{n\pi}{l}x\mathrm{dx}
  \end{equation}$$
  $$\begin{equation}
  B_n=\frac{2}{l}\int_{0}^{l}\varphi(x)\sin\frac{n\pi}{l}x\mathrm{dx}
  \end{equation}$$
  我们将每一个本征值对应的本征解改写为如下形式
  $$\begin{equation}
  u_n(x,t)=C_n\sin\frac{an\pi}{l}x\cdot\sin(\omega_nt +\delta_n)
  \end{equation}$$
  本征解$u_n(x,t)$表示第n个振动模式，其中
  $$\begin{cases}
   C_n=\sqrt{A_n^2+B_n^2}   \\\\
   \delta_n=\arctan\frac{B_n}{A_n}   \\\\
   \omega_n=\frac{an\pi}{l}
  \end{cases}$$
  $\omega_n$称为第n个振动模式的频率，$\delta_n$称为这一振动模式的初相位，可以看出其振幅显然与坐标位置有关.使得振幅为零的点称为**波节**，振幅达到最大的位置称为**波腹**.n = 1为该弦振动的**基波**，其余n称为弦振动的**n次谐波**.上面分析的波的运动形式是**驻波**的形式

## §    斯特姆-刘维尔本征值问题
- **一：Sturm-Liouville本征值问题**
  斯特姆-刘维尔本征值问题简称S-L本征值问题，是含有参数$\lambda$的特定二阶常微分方程，即Sturm-Liouville方程在特定边界条件下所构成的本征值问题
  具有如下形式带参数$\lambda$的二阶常微分方程称为**Sturm-Loiuville方程**，简写成S-L方程
  $$\begin{equation}
  \frac{\mathrm{d}}{\mathrm{dx}}[k(x)y'(x)]-q(x)y(x)+\lambda\rho(x)y(x)=0
  \end{equation}$$
  在S-L方程中参数$\lambda$称为**本征参数或本征值**，函数$\rho(x)$称为**权重函数**
  若我们把S-L方程写成算子形式，定义线性算子
  $$\begin{equation}
  L=-\frac{\mathrm{d}}{\mathrm{dx}}[k(x)\frac{\mathrm{d}}{\mathrm{dx}}]+q(x)
  \end{equation}$$
  则S-L方程可以写为
  $$\begin{equation}
  Ly(x)=\lambda\rho(x)y(x)
  \end{equation}$$
  下面我们讨论S-L方程在一定边界条件下的本征值问题，为了方便讨论，我们限定$k(x)\ge 0,q(x)\ge 0,\rho(x)>0$,我们的讨论限制在如下三种边界上
  - 1. **三类齐次边界条件**
       在 x = a, x = b 的边界点上，下面四个参数均不为负数，有
       $$\begin{equation}
       [\alpha_1 y-\beta_1 y'] =0,  \quad x=a
       \end{equation}$$
       $$\begin{equation}
       [\alpha_2 y+\beta_2 y'] =0,  \quad x=b
       \end{equation}$$
       其中
       - 当$\beta_1,\beta_2 =0$时为第一类边界条件
       - 当$\alpha_1,\alpha_2=0$时为第二类边界条件
       - 当$\alpha,\beta$都不为零时为第三类边界条件
       - 第一式子中y'前的负号是因为在 x = a 边界点的外法向方向与该点导数的方向相反
  - 2. **自然边界条件**
       当k(a)=k(b)=0 时，称为自然边界条件
  - 3. **周期边界条件**
       当k(a)=k(b) 且y(a)=y(b),y'(a)=y'(b) 时，称为周期边界条件
  下面我们介绍S-L方程的一些性质
  - **本征函数的正交性质**
    如上在S-L方程形式的限制下和三种边界条件下，S-L方程存在本征解，对应每一个本征值$\lambda_n$有本征函数$y_n(x)$,则所有的本征解{$y_n(x)$}构成一个完备的正交函数系
  - 在三类齐次边界条件下，或者在周期边界条件下，S-L问题具有无穷多个非负的本征值，所有本征值组成一个单调递增以无穷远点为凝聚点的序列
    $$\begin{equation}
    0\le \lambda_1 <\lambda_2<\cdots<\lambda_n<\cdots, \quad \lim_{n\to \infty}\lambda_n=\infty
    \end{equation}$$

- **二：本征函数系上的广义傅里叶展开**
  无穷多个本征值对应的无穷很多个本征函数构成的一个完备的正交函数系{$y_n(x)$}，任何一个定义在$x\in [a,b]$上的满足Direchlet条件的函数f(x)，都可以在该正交函数系上作广义傅里叶展开
  $$\begin{equation}
  f(x)=\sum_{n=1}^{\infty}C_n y_n(x)
  \end{equation}$$
  $$\begin{equation}
  C_n=\frac{1}{\int_{a}^{b}|y_n(x)|^2\rho(x)\mathrm{dx}}\cdot\int_{a}^{b}f(x)\rho(x)y_n^{\star}(x)\mathrm{dx}
  \end{equation}$$
$$\begin{equation}\end{equation}$$
$$\begin{equation}\end{equation}$$
## §    非齐次方程齐次边界条件下的分离变量法
- 我们以弦的受迫振动为例来展开描述
  设弦受到已知外力f(x,t)的作用，其定解问题如下
  $$\begin{cases}
   u_{tt}-a^2u_{xx}=f(x,t) \quad 0<x<l,t>0   \\\\
   u(0,t)=u(l,t)=0  \\\\
   u(x,0)=\varphi(x)  \\\\
   u_t(x,0)=v(x)
  \end{cases}$$
  其对应的齐次方程的定解问题
  $$\begin{cases}
   u_{tt}-a^2u_{xx}=0   \\\\
   u(0,t)=u(l,t)=0  \\\\
   u(x,0)=\varphi(x)  \\\\
   u_t(x,0)=v(x)
  \end{cases}$$
  的解前文中我们已经获得.其S-L本征值问题的本征函数系为{$\sin\frac{n\pi}{l}x,n=\in N^{+}$}.将t作为参数，将函数f(x,t)在此函数系中作带参数的展开
  $$\begin{equation}
  f(x,t)=\sum_{n=1}^{\infty}f_n(t)\sin\frac{n\pi}{l}x
  \end{equation}$$
  $$\begin{equation}
  f_n(t)=\frac{2}{l}\int_{0}^{l}f(x,t)\sin\frac{n\pi}{l}x\mathrm{dx}
  \end{equation}$$
  而上述齐次方程齐次边界条件的解的形式为
  $$\begin{equation}
  u(x,t)=\sum_{n=1}^{\infty}T_n(t)\sin\frac{n\pi}{l}x
  \end{equation}$$
  将上两式带入非齐次方程组和初始条件中，定解问题变为
  $$\begin{cases}
   \sum_{n=1}^{\infty}(T_n''+\frac{n^2\pi^2a^2}{l^2})\sin\frac{n\pi}{l}x=\sum_{n=1}^{\infty}f_n(t)\sin\frac{n\pi}{l}x  \\\\
   \sum_{n=1}^{\infty}T_n(0)\sin\frac{n\pi}{l}x=\varphi(x)=\sum_{n=1}^{\infty}\varphi_n\sin\frac{n\pi}{l}x   \\\\
   \sum_{n=1}^{\infty}T_n'(0)\sin\frac{n\pi}{l}x=v(x)=\sum_{n=1}^{\infty}v_n\sin\frac{n\pi}{l}x
  \end{cases}$$
  上述的丁姐问题可以化归为
  $$\begin{cases}
   T_n''+\omega_n^2T_n=f_n(t)  \\\\
   T_n(0)=\varphi_n  \\\\
   T_n'(0)=v_n
  \end{cases}$$
  其中$\omega_n$一如既往地称为本征频率
  $$\begin{equation}
  \omega_n=\frac{an\pi}{l}
  \end{equation}$$
  $$\begin{equation}
  f_n(t)=\frac{2}{l}\int_{0}^{l}f(x,t)\sin\frac{n\pi}{l}x\mathrm{dx}
  \end{equation}$$
  $$\begin{equation}
  \varphi_n=\frac{2}{l}\int_{0}^{l}\varphi(x)\sin\frac{n\pi}{l}x\mathrm{dx}
  \end{equation}$$
  $$\begin{equation}
  v_n=\frac{2}{l}\int_{0}^{l}v(x)\sin\frac{n\pi}{l}x\mathrm{dx}
  \end{equation}$$
  因此在外力f(x,t)作用下两端固定地弦的定解问题变为$T_n(t)$的非齐次二阶常微分方程的定解问题
- 共振情形
  当外力f(x,t)为特殊形式,且边界位置分布函数和位置速度函数全为零时
  $$\begin{equation}
  f(x,t)=A(x)\sin\omega t 
  \end{equation}$$
  $$\begin{equation}
  A(x)\sin\omega t=\sin\omega t\sum_{n=1}^{\infty}a_n\sin\frac{n\pi}{l}x
  \end{equation}=f_n\sin\omega t$$
  $$\begin{equation}
  a_n=\frac{2}{l}\int_{0}^{\infty}A(x)\sin\frac{n\pi}{l}x\mathrm{dx}
  \end{equation}$$
  解该二阶非齐次线性常微分方程并通过边界条件确定积分系数可以得到解的形式为
  $$\begin{equation}
  T_n=\frac{a_n}{\omega_n(\omega^2-\omega_n^2)}(\omega\sin\omega_n t-\omega_n\sin\omega t)
  \end{equation}$$
  当外力的频率趋于本征频率时，有洛必达法则可以得到
  $$\begin{equation}
  T=\lim_{\omega\to \omega_k}\frac{a_k}{2\omega_k^2}\sin\omega_k t-\frac{a_k}{2\omega_k}t\cos\omega_k t
  \end{equation}$$
  于是在弦振动方程中会出现两部分，一部分是对 n ≠ k 部分的求和，另一部分即为**共振项**，可以看到共振项的振幅是时间的线性函数，随时间延绵振幅将会无限增大，形成**共振**
  实际现象中，共振往往只会发生于外力的频率趋于基波频率时，而对趋于高次谐波时的本征频率却不容易出现。这是因为高次谐波是具有节点的驻波，当振幅增大时，可能破坏其驻波结构而产生某些非线性效应，这将阻碍振幅的增大
## §    非齐次方程边界条件下的分离变量法
- S-L方程本征值问题是基于齐次方程和齐次边界条件的，而当边界条件为非齐次时，我们需要运用函数变换理论构造一个新的函数将边界齐次化，进而求解
- 下面以一个构造的栗子供揣摩体会
  $$\begin{cases}
   u_{tt}-a^2u_{xx}=f(x,t) \quad (0<x<l,t>0) \\\\
   u(0,t)=g_1(t) \\\\
   u(l,t)=g_2(t) \\\\
   u(x,0)=\varphi(x) \\\\
   u_t(x,0)=v(x)
  \end{cases}$$
  **我们知道波动方程是线性方程，其解具备线性叠加性质，因此我们假设 u = w + k，并且其中一部分与边界条件的非齐次项抵消，这样另一部分的边界就是齐次边界了**
  $$\begin{equation}
  u(x,t)=k(x,t)+w(x,t)
  \end{equation}$$
  按照上述说法，我们使
  $$\begin{equation}
  k(0,t)=g_1(t) \quad k(l,t)=g_2(t)
  \end{equation}$$
  则可以得到
  $$\begin{equation}
  w(0,t)=0 \quad w(l,t)=0
  \end{equation}$$
  在此做法之下方程组就化为我们前一节讲述的内容
  $$\begin{cases}
   w_{tt}-a^2w_{xx}=f(x,t)-k_{tt}+a^2k_{xx} \\\\
   w(x,0)=\varphi(x)-k(x,0)=\Phi(x) \\\\
   w_t(x,0)=v(x)-k_t(x,0)=V(x)
  \end{cases}$$
  然后我们假设k(x,t)的函数形式就为最简单的线性函数，值得一提的是k(x,t)函数的形式显然是不唯一的
  $$\begin{equation}
  k(x,t)=A(t)x+B(t)
  \end{equation}$$
  并由初值条件(即最开始的假设)可以解到
  $$\begin{equation}
  k(x,t)=\frac{1}{l}[g_2(t)-g_1(t)]x+g_1(t)=\frac{x}{l}g_2+\frac{l-x}{l}g_1
  \end{equation}$$
  确定里k(x,t)的形式后，带入我们熟悉的前述方程组并按照之前的办法就可以得到相应的解，至此，我们边将非齐次的边界化归为齐次边界并能很好的解决


---
# 曲线坐标系下方程的分离变量
## §    球坐标系下方程的分离变量法
- **一：Laplace方程在球坐标下的分离变量**
  Laplace方程是纯空间变量的方程，在球坐标系下
  $$\begin{equation}
  \nabla^2u(r,\theta,\varphi)=0
  \end{equation}$$
  Laplace算子在球坐标系下的表达式为
  $$\begin{equation}
  \nabla^2=\frac{1}{r^2}\frac{\partial }{\partial r}(r^2\frac{\partial }{\partial r})+\frac{1}{r^2\sin\theta}\frac{\partial }{\partial \theta}(\sin\theta\frac{\partial }{\partial \theta})+\frac{1}{r^2\sin^2\theta}\frac{\partial^2 }{\partial \varphi^2}
  \end{equation}$$
  设球坐标系下场函数u可以分解为径向部分R和角度部分Y
  $$\begin{equation}
  u(r,\theta\varphi)=R(r)Y(\theta,\varphi)
  \end{equation}$$
  则球坐标系下Laplace方程的表征式为
  $$\begin{equation}
  \frac{Y}{r^2}\frac{\mathrm{d}}{\mathrm{dr}}(r^2\frac{\mathrm{dR}}{\mathrm{dr}})+\frac{R}{r^2\sin\theta}\frac{\partial }{\partial \theta}(\sin\theta\frac{\partial Y}{\partial \theta})+\frac{R}{r^2\sin^2\theta}\frac{\partial^2 Y}{\partial \varphi^2}
  \end{equation}$$
  方程两边同时乘以$\frac{r^2}{RY}$得
  $$\begin{equation}
  \frac{1}{R}\frac{\mathrm{d}}{\mathrm{dr}}(r^2\frac{\mathrm{dR}}{\mathrm{dr}})=-\frac{1}{Y\sin\theta}\frac{\partial }{\partial \theta}(\sin\theta\frac{\partial Y}{\partial \theta})-\frac{1}{Y\sin^2\theta}\frac{\partial^2 Y}{\partial \varphi^2}
  \end{equation}$$
  此等式左侧为R的函数，右侧为角度Y的函数，令他们等于一个常数，该常数记为$l(l + 1)$,即得到
  $$\begin{equation}
  \frac{1}{R}\frac{\mathrm{d}}{\mathrm{dr}}(r^2\frac{\mathrm{dR}}{\mathrm{dr}})=l(l+1)
  \end{equation}$$
  进一步可以表征为
  $$\begin{equation}
  r^2\frac{\mathrm{d^2R(r)}}{\mathrm{dr^2}}+2r\frac{\mathrm{dR(r)}}{\mathrm{dr}}-l(l+1)R(r)=0
  \end{equation}$$
  此方程称为**径向方程**，它是**Euler型方程**
  同样地。角度Y的函数部分可以表示为
  $$\begin{equation}
  \frac{1}{\sin\theta}\frac{\partial }{\partial \theta}(\sin\theta\frac{\partial Y}{\partial \theta})+\frac{1}{\sin^2\theta}\frac{\partial^ Y}{\partial \varphi^2}+l(1+l)Y=0
  \end{equation}$$
  此方程称为**球函数方程**
  我们再进一步将角度函数进行分离变量
  $$\begin{equation}
  Y(\theta,\varphi)=\Theta(\theta)\Phi(\varphi)
  \end{equation}$$
  球函数方程可以进一步表示为
  $$\begin{equation}
  \frac{\Phi}{\sin\theta}\frac{\mathrm{d}}{\mathrm{d\theta}}(\sin\theta\frac{\mathrm{d\Theta}}{\mathrm{d\theta}})+\frac{\Theta}{\sin^2\theta}\frac{\mathrm{d^2\Phi}}{\mathrm{d\varphi^2}}+l(l+1)\Theta\Phi=0
  \end{equation}$$
  $$\begin{equation}
  \frac{\sin\theta}{\Theta}\frac{\mathrm{d}}{\mathrm{d\theta}}(\sin\theta\frac{\mathrm{d\Theta}}{\mathrm{d\theta}})+l(l+1)\sin^2\theta=-\frac{1}{\Phi}\frac{\mathrm{d^2\Phi}}{\mathrm{d\varphi^2}}
  \end{equation}$$
  等式的左侧和右侧分别为独立变量的函数，同样地，我们令两边都等于同一常数$\lambda$，关于$\Phi(\varphi)$的方程为
  $$\begin{equation}
  \Phi''+\lambda\Phi=0
  \end{equation}$$
  一般情况下，当$\varphi$转过一圈后，我们要求$u(r,\theta,\varphi)$与$u(r,\theta,\varphi+2\pi)$表示同一个场值，这是一种周期性的边界条件，它与式$(115)$构成本征值问题，其本征值为$\lambda=m^2,m=0,\pm 1\cdots$
  $$\begin{equation}
  \phi''+m^2\Phi=0
  \end{equation}$$
  关于$\Theta(\theta)$的方程为
  $$\begin{equation}
  \frac{1}{\sin\theta}\frac{\mathrm{d}}{\mathrm{d\theta}}(\sin\theta\frac{\mathrm{d\Theta}}{\mathrm{d\theta}})+[l(l+1)-\frac{m^2}{\sin^2\theta}]\Theta=0
  \end{equation}$$
  取变换，令$\cos\theta=x,\Theta(\theta)=y(x),|x|<1,\mathrm{dx}=-\sin\theta\mathrm{d\theta}$，则方程变为
  $$\begin{equation}
  (1-x^2)\frac{\mathrm{d^2y}}{\mathrm{dx^2}}-2x\frac{\mathrm{dy}}{\mathrm{dx}}+[l(l+1)-\frac{m^2}{1-x^2}]y=0
  \end{equation}$$
  这一方程称为**连带Legendre(勒让德)方程**
  当我们考虑的问题具有极轴对称性时，即此时与$\varphi$角参数无关，此时$m=0,\Phi(\varphi)=1,u(r,\theta,\varphi)=R(r)\Theta(\theta)$，此时方程就退化为**Legendre勒让德方程**
  $$\begin{equation}
  (1-x^2)\frac{\mathrm{d^2y}}{\mathrm{dx^2}}-2x\frac{\mathrm{dy}}{\mathrm{dx}}+l(l+1)y=0
  \end{equation}$$

- **二：Helmhotz方程在球坐标下的分离变量**
  将波动方程标准形式进行空间和时间的变量分离,$U(\vec{r},t)=u(\vec{r})T(t)$，即得到
  $$\begin{equation}
  u_{tt}-a^2\nabla^2u=0 
  \end{equation}$$
  $$\begin{equation}
  \frac{T''}{T}=\frac{a^2\nabla^2u}{u}=-\lambda
  \end{equation}$$
  $$\begin{equation}
  \nabla^u + k^2u=0, \quad k^2=\frac{\lambda}{a^2}
  \end{equation}$$
  此方程称为**亥姆霍兹方程**
  当然地，对运输方程进行时空剥离后也能得到同样地方程，此处不再赘述
  亥姆霍兹方程在球坐标系下的表示显然等于Laplace方程的球坐标形式附加$k^2u$一项即可
  $$\begin{equation}
  \frac{1}{r^2}\frac{\partial }{\partial r}(r^2\frac{\partial u}{\partial r})+\frac{1}{r^2\sin\theta}\frac{\partial }{\partial \theta}(\sin\theta\frac{\partial u}{\partial \theta})+\frac{1}{r^2\sin^2\theta}\frac{\partial^2 u}{\partial \varphi^2}+k^2u=0
  \end{equation}$$
  同样熟悉而类似地操作，将函数拆分为径向和角度函数两部分
  $$\begin{equation}
  \frac{r^2}{R}[\frac{1}{r^2}\frac{\mathrm{d}}{\mathrm{dr}}(r^2\frac{\mathrm{dR}}{\mathrm{dr}})+k^R]=-\frac{1}{Y\sin\theta}\frac{\partial }{\partial \theta}(\sin\theta\frac{\partial Y}{\partial \theta})-\frac{1}{Y\sin^2\theta}\frac{\partial^2 Y}{\partial \varphi^2}
  \end{equation}$$
  此式左侧同样为径向部分，右侧为角度部分，令其等于常数$l(l + 1)$,可以得到
  $$\begin{equation}
  \frac{\mathrm{d^2R}}{\mathrm{dr^2}}+\frac{2}{r}\frac{\mathrm{dR}}{\mathrm{dr}}+[k^2-\frac{l(l+1)}{r^2}]R=0
  \end{equation}$$
  此方程称为**球贝塞尔方程**
  角度部分的方程为
  $$\begin{equation}
  \frac{1}{\sin\theta}\frac{\partial }{\partial \theta}(\sin\theta\frac{\partial Y}{\partial \theta})+\frac{1}{\sin^2\theta}\frac{\partial^2 Y}{\partial \varphi^2}+l(l+1)Y=0
  \end{equation}$$
  此方程就是**球函数方程**，同样地，将角度部分进一步变量分离可以得到
  $$\begin{equation}
  (1-x^2)\frac{\mathrm{d^2y}}{\mathrm{dx^2}}-2x\frac{\mathrm{dy}}{\mathrm{dx}}+[l(l+1)-\frac{m^2}{1-x^2}]y=0
  \end{equation}$$
  此方程即为连带Legendre方程


## §    柱坐标系下方程的分离变量法
- 可以看出Laplace方程是Helmhotz方程的特殊情形，因此接下来的讨论将以一更为般的Helmhot方程展开阐述
- 亥姆霍兹方程在柱坐标下的方程形式为
  $$\begin{equation}
  \frac{1}{\rho}\frac{\partial }{\partial \rho}(\rho\frac{\partial u}{\partial \rho})+\frac{1}{\rho^2}\frac{\partial^2 u}{\partial \varphi^2}+\frac{\partial^2 u}{\partial z^2}+k^2u=0
  \end{equation}$$
  我们对此方程进行彻底的变量分离后可以得到方程的形式为
  $$\begin{equation}
  u(\rho,\varphi,z)=R(\rho)\Phi(\varphi)Z(z)
  \end{equation}$$
  $$\begin{equation}
  \frac{\rho}{R}\frac{\partial }{\partial \rho}(\rho\frac{\partial R}{\partial \rho})+\frac{\rho^2}{Z}\frac{\partial^2 Z}{\partial z^2}+k^2\rho^2=-\frac{1}{\Phi}\frac{\partial^2 \Phi}{\partial \varphi^2}
  \end{equation}$$
  等式方程左侧为双变量$\rho,z$的函数，右侧为角度的函数，两侧始终相等，则只能等于与任意变量都无关的常数$v^2$
  方程右侧满足的方程为
  $$\begin{equation}
  \Phi''+v^2\Phi=0
  \end{equation}$$
  方程左侧满足的方程为
  $$\begin{equation}
  \frac{1}{R\rho}\frac{\partial }{\partial \rho}(\rho\frac{\partial R}{\partial \rho})+k^2-\frac{v^2}{\rho^2}=-\frac{1}{Z}\frac{\partial^2 Z}{\partial z^2}
  \end{equation}$$
  令方程两侧等于同一个常数$-\lambda$
  $$\begin{equation}
  Z''-\lambda z=0
  \end{equation}$$
  $$\begin{equation}
  \frac{1}{\rho}\frac{\partial }{\partial \rho}(\rho\frac{\partial R}{\partial \rho})+(k^2+\lambda-\frac{v^2}{\rho^2})R=0
  \end{equation}$$
  令$x=\sqrt{k^2+\lambda}\rho,R(\rho)=y(x)$，方程进一步变为
  $$\begin{equation}
  \frac{\mathrm{d^2 y}}{\mathrm{dx^2}}+\frac{1}{x}\frac{\mathrm{dy}}{\mathrm{dx}}+(1-\frac{v^2}{x^2})y=0
  \end{equation}$$
  此方程称为**Bessel贝塞尔方程**，也称为v阶贝塞尔方程


## §    二阶线性常微分方程的级数解法
- 二阶线性齐次常微分方程的标准形式为
  $$\begin{equation}
  \frac{\mathrm{d^2u(z)}}{\mathrm{dz^2}}+p(z)\frac{\mathrm{du(z)}}{\mathrm{dz}}+q(z)u(z)=0
  \end{equation}$$
  这里采用的是复变量，实变量知识复变量的一种特殊形式，因此我们讨论更为一般的形式，以便阐述方程的解析性质
  方程的标准形式中复变函数p(z)或q(z)是已知的复变函数，设他们在所研究的区域内只存在若干的孤立奇点，此外的其他点处均解析.我们把研究区域内的点分为两类
   1. 方程的正常点，也称为正则点：如果p(z),q(z)在某点及其邻域内是解析的，则该点称为方程的正常点
   2. 方程的奇点：如果某点是p(z)或q(z)的孤立奇点，则称该点为方程的奇点.方程的奇点可以分为两类
      2.1 正则奇点：如果某一点是方程的奇点，但该奇点至多为p(z)的一阶极点，且同时至多为q(z)的二阶极点，则奇点为正则奇点，换言之，即$(z-z_0)p(z)$为解析函数，且$(z-z_0)^2q(z)$亦为解析函数
      2.2 非正则奇点：如果某点是方程的奇点，但不是正则奇点，就称为非正则奇点
- 常微分方程级数解法的基本思想是：在微分方程的定义区域内，考察点$z_0$的邻域内，并把已知函数p(z),q(z)展开成级数.再假设解u(z)再此邻域内也可以展开成幂级数的形式，代入方程，通过比较系数就可以得到u(z)的技术表达式
- **定理**
  对于二阶线性齐次常微分方程
  $$\begin{aligned}
  \frac{\mathrm{d^2u(z)}}{\mathrm{dz^2}}+p(z)\frac{\mathrm{du(z)}}{\mathrm{dz}}+q(z)u(z)=0
  \end{aligned}$$
  其解u(z)具有如下性质
  1. 对于方程的正常点，在此正常点及其邻域内，方程具有两个线性无关的解析解，它们的形式都为
     $$\begin{equation}
     u(z)=\sum_{k=0}^{\infty}a_k(z-z_0)^{k}
     \end{equation}$$
  2. 对方程的正则奇点，方程在此奇点的邻域内，存在两个线性无关的解，他们的形式分别为
     $$\begin{equation}
     u_1(z)=(z-z_0)^{\rho_1}\sum_{k=0}^{\infty}a_k(z-z_0)^{k}
     \end{equation}$$
     $$\begin{equation}
     u_2(z)=(z-z_0)^{\rho_2}\sum_{k=0}^{\infty}b_k(z-z_0)^{k}
     \end{equation}$$
  3. 对于方程的非正则奇点，方程的解析解可能不存在，这类方程一般没有通用的解法，但方程的两个线性无关的解可以形式上表示为
     $$\begin{equation}
     u_1(z)=(z-z_0)^{\rho_1}\sum_{k=0}^{\infty}a_k(z-z_0)^{k}
     \end{equation}$$
     $$\begin{equation}
     u_2(z)=(z-z_0)^{\rho_2}\sum_{k=1\infty}^{\infty}b_k(z-z_0)^{k}+Au_1\ln(z-z_0)
     \end{equation}$$


---
# 球函数
## §    勒让德多项式
- Laplace方程在球坐标系下的分离变量，其角度部分函数Y满足球函数方程.当这一稳定场的分布具有轴对称性时，即场$Y(\theta,\varphi)$与角度$\varphi$无关时，此时$\Theta(\theta)$满足的连带Legendre方程退化为Legendre方程
  $$\begin{equation}
  (1-x^2)\frac{\mathrm{d^2y}}{\mathrm{dx^2}}-2x\frac{\mathrm{dy}}{\mathrm{dx}}+l(l+1)y=0 ,\quad |x|\le 1
  \end{equation}$$
  将勒让德方程标准化归为二阶齐次线性微分方程，不难发现它有两个正则奇点 x = ± 1，由于我们所研究的问题是从具体的物理问题中得到的，因此我们所求的物理量的场均为有限值，即要求$|y(x)|$在x的定义域上为有限制，这种要求是一种自然的边界条件，它与Legendre方程一起构成了S-L本征值问题
  $$\begin{cases}
   (1-x^2)\frac{\mathrm{d^2y}}{\mathrm{dx^2}}-2x\frac{\mathrm{dy}}{\mathrm{dx}}+l(l+1)y=0, \quad -1\le x\le 1   \\\\
   |y(x)|<\infty ,\quad   -2\le x\le 1
  \end{cases}$$
  我们首先给出x的正常点上的解，我们在方程的正常点x = 0的解有级数形式
  $$\begin{equation}
  y(x)=\sum_{k=0}^{\infty}C_kx^k
  \end{equation}$$
  带入上面方程组有
  $$\begin{equation}
  \sum_{k=0}^{\infty}k(k-1)C_kx^{k-2}-\sum_{k=0}^{\infty}[k(k+1)-l(l+1)]C_kx^k=0
  \end{equation}$$
  对此方程从x的零次幂项开始，各个幂次项的系数都要为零，一般项$x^k$的系数为零，需要满足
  $$\begin{aligned}
  (k+2)(k+1)C_{k+2}-[k(k+1)-l(l+1)]C_k=0
  \end{aligned}$$
  $$\begin{equation}
  C_{k+2}=-\frac{(l-k)(l+k+1)}{(k+2)(k+1)}C_k
  \end{equation}$$
  这就是Legendre方程在$x = 0$点邻域内级数解的递推关系，注意到指数标差2，因此显然需要进行奇偶分组，分别递推可得$(n=1,2,3\cdots)$
  $$\begin{cases}
   C_{2n}=\frac{(-1)^nl(l-2)(l-4)\cdots (l-2n+2)(l+1)(l+3)\cdots (l+2n-1)}{(2n)!}C_0  \\\\
   C_{2n+1}=\frac{(-1)^n(l-1)(l-3)\cdots (l-2n+1)(l+2)(l+4)\cdots (l+2n)}{(2n+1)!}C_1
  \end{cases}$$
  由上述关系，我们可以用$C_0$和$C_1$表示组成解y的所有系数，组成解分为偶次幂项$y_0$和奇次幂项$y_1$
  $$\begin{cases}
   y_0=C_0+C_2x^2+C_4x^4+\cdots    \\\\
   y_1=C_1x+C_3x^3+C_5x^5+\cdots
  \end{cases}$$
  该级数的收敛半径R为
  $$\begin{equation}
  R=\lim_{k\to \infty}|\frac{C_k}{C_{k+2}}|=\lim_{k\to \infty}|\frac{(k+2)(k+1)}{k(k+1)-l(l+1)}|=1
  \end{equation}$$
  因此级数解在$|x|<1$时收敛，而在等于时级数解显然是发散的
  从级数的递推式我们可以发现，当$k=l$时就会有$C_{k+2}=0$成立，显然，当$k>l$后的每一项$C_{k+2}$系数都将为零，此时方程的解就退化为最高次幂为l的多项式，**l称为本征参数**.由于l存在奇偶性问题，当l为奇数时，方程的解的奇数部分退化为最高次幂为l的奇次幂多项式，而此时偶次幂仍未无穷发散奇数，为此我们需要选取$C_0=0$，使得解$y(x)=y_1(x)$，当l为偶数时同理
  至此我们得到了满足自然边界条件的S-L本征值问题，当本征参数为l时，其本征值为$l(l+1)$。相应的本征函数是以l为做高次幂的多项式
  $$\begin{equation}
  y_l(x)=C_0+C_2x^2+\cdots+C_lx^l ,\quad l=0,2,4,\cdots
  \end{equation}$$
  $$\begin{equation}
  y_l(x)=C_1x+C_3x^3+\cdots+C_lx^l ,\quad l=1,3,5,\cdots
  \end{equation}$$
  为了求出具体的表达式，当$k=l-1$时，我们反向进行系数递推可得
  $$\begin{equation}
  C_{l-2n}=(-1)^n\frac{(l!)^2(2l-2n)!}{(2l)!n!(l-2n)!(l-n)!}C_l
  \end{equation}$$
  到此，我们可以把相应于本征值$l(l+1)$的本征函数$y_l(x)$写成
  $$\begin{equation}
  y_l(x)=C_l\sum_{n=0}^{N}\frac{(-1)^n(l!)^2(2l-2n)!}{(2l)!n!(l-2n)!(l-n)!}x^{l-2n}
  \end{equation}$$
  $$N=\begin{cases}
   \frac{l}{2}  ，\quad l为偶数 \\\\
   \frac{l-1}{2}  ，\quad  l为奇数
  \end{cases}$$
  若我们取$C_l$的值为
  $$\begin{equation}
  C_l=\frac{(2l)!}{2^l(l!)^2}
  \end{equation}$$
  相应的$y_l(x)$记为$P_l(x)$
  $$\begin{equation}
  P_l(x)=\sum_{n=0}^{N}\frac{(-1)^n(2l-2n)!}{2^ln!(l-n)!(l-2n)!}x^{l-2n}
  \end{equation}$$
  $$N=\begin{cases}
   \frac{l}{2}  ，\quad l为偶数 \\\\
   \frac{l-1}{2}  ，\quad  l为奇数
  \end{cases}$$
  $P_l(x)$称为**Legendre多项式**，也称为**Legendre函数，满足Legendre方程的解统称为Legendre函数**，通常称为第一类Legendre多项式，它是Legendre方程在$|x|\le 1$时，在自然边界条件下对应于本征值为l(l + 1)的本征解


## §    勒让德多项式的性质
- **一：Legendre多项式的微分表达式**
  $$\begin{equation}
  P_l(x)=\frac{1}{2^{l}l!}\frac{\mathrm{d^{l}}}{\mathrm{dx^{l}}}(x^2-1)^{l}
  \end{equation}$$
  此表达式称为**罗德里格斯公式**

- **二：Legendre多项式的生成函数**
  $$\begin{equation}
  f(r)=\frac{1}{\sqrt{1+r^2-2r\cos\theta}}=\frac{1}{\sqrt{1+r^2-2rx}} ,\quad r<1
  \end{equation}$$
  其中$r=|\vec{r}|,x=\cos\theta,|x|\le 1$
  将函数f(r)在$r=0$点进行泰勒展开，可以得到
  $$\begin{equation}
  \frac{1}{\sqrt{1+r^2-2rx}}=\sum_{l=0}^{\infty}P_l(x)r^{l}
  \end{equation}$$
  即f(r)展开式的系数即为Legendre多项式
  我们把函数f(r)称为**Legendre多项式的生成函数或称为母函数**
  Legendre生成函数的物理意义可以解释为一个球心在原点的单位球，在其极轴上(即单位球的北极点)放置一个电荷量为$4\pi\varepsilon_0$的点电荷，则单位球内任意一点的电势即为f(r)，这是该点电荷产生的静电场的稳定分布
- **三：Legendre多项式的递推公式**
  将Legendre多项式的生成函数的Taylor展开式的两边求r的微商(即式$(155)$)，就可以得到
  $$\begin{equation}
  -\frac{r-x}{(1+r^2-2rx)^{\frac{3}{2}}}=\sum_{l=0}^{\infty}lP_l(x)r^{l-1}
  \end{equation}$$
  对两边同时乘以$(1+r^2-2rx)$就可以得到
  $$\begin{equation}
  (x-r)\sum_{l=0}^{\infty}P_l(x)r^{l}=(1+r^2-2rx)\sum_{l=1}^{\infty}lP_l(x)r^{l-1}
  \end{equation}$$  
  即
  $$\begin{equation}
  \sum_{l=0}^{\infty}xP_l(x)r^{l}-\sum_{l=0}^{\infty}P_l(x)r^{l+1}=\sum_{l=0}^{\infty}lP_l(x)r^{l-1}+\sum_{l=0}^{\infty}lP_l(x)r^{l+1}-\sum_{l=0}^{\infty}2xlP_l(x)r^{l}
  \end{equation}$$
  比较两侧$r^{l}$项的系数可以得到
  $$\begin{aligned}
   xP_l(x)-P_{l-1}(x)=(l+1)P_{l+1}(x)+(l-1)P_{l-1}(x)-2xlP_{l}(x)
  \end{aligned}$$
  即
  $$\begin{equation}
  x(1+2l)P_l(x)-(l+1)P_{l+1}(x)-lP_{l-1}(x)=0
  \end{equation}$$
  这就是Legendre多项式的一个基本递推关系
  Legendre多项式的另一个基本递推关系就是对x求微商，并用上面如出一辙的方法，进行整理，比较$r^{l+1}$项系数可以得到
  $$\begin{equation}
  P_l(x)=P_{l+1}'(x)+P_{l-1}'(x)-2xP_l'(x)
  \end{equation}$$
  这就是Legendre多项式的另一个基本递推关系
  有了这两个基本递推关系式，我们可以还可以得到几个常用的递推关系式
  $$\begin{equation}
  (2l+1)P_l(x)=P_{l+1}'(x)-P_{l-1}'(x)
  \end{equation}$$
  $$\begin{equation}
  (l+1)P_l(x)=P_{l+1}'(x)-xP_{l}'(x)
  \end{equation}$$
  $$\begin{equation}
  lP_l(x)=xP_l'(x)-P_{l-1}'(x)
  \end{equation}$$
  $$\begin{equation}
  (x^2-1)P_l'(x)=lxP_l(x)-lP_{l-1}(x)
  \end{equation}$$

- **四：Legendre多项式的正交性**
  - 命题 
    设$f_{k}(x)$为x的k次多项式，$P_{l}(x)$是Legendre多项式，当$k<l$时，有
    $$\begin{equation}
    \int_{-1}^{1}f_k(x)P_l(x)\mathrm{dx}=0
    \end{equation}$$
  - 根据上述命题，令$f_k(x)=P_k(x)$，我们可以得到当$k\neq l$时，$P_l(x)$的正交关系式
    $$\begin{equation}
    \int_{-1}^{1}P_k(x)P_l(x)\mathrm{dx}=0 ,\quad k\neq l
    \end{equation}$$
    $$\begin{equation}
    \int_{-1}^{1]}P_l(x)P_l(x)\mathrm{dx}=\frac{2}{2l+1} ,\quad k=l
    \end{equation}$$
    因此当k=l时，我们得到了它的归一化系数为$\sqrt{\frac{2l+1}{2}}$，即可以把归一化后的legendre多项式的正交关系写成标准的形式
    $$\begin{equation}
    \int_{-1}^{1}\sqrt{\frac{2k+1}{2}}P_k(x)\sqrt{\frac{2l+1}{2}}P_l(x)\mathrm{dx}=\delta_{i,j}
    \end{equation}$$
    $$\begin{equation}
    \delta_{n,m}=\frac{1}{2\pi}\int_{0}^{2\pi}e^{i(n-m)\theta}\mathrm{d\theta}
    \end{equation}$$
    这就构成了正交归一化的函数系，这是Legendre方程的S-L本征值问题的本征解，因此正交归一的Legendre多项式构成了正交归一的完备的函数系，该函数系可以作为Hilbert空间的基向量，张成一个Hilbert空间
## §    具有对称轴的拉普拉斯方程的求解
- Laplace方程式描述的是一个无源区域中的稳定场分布方程，其球坐标系形式以及在球坐标系下的变量分离，我们已经在之前讲过，下面我们直接搬过来
  $$\begin{equation}
  \frac{1}{r^2}\frac{\partial }{\partial r}(r^2\frac{\partial u}{\partial r})+\frac{1}{r^2\sin\theta}\frac{\partial }{\partial \theta}(\sin\frac{\partial u}{\partial \theta})+\frac{1}{r^2\sin^2\theta}\frac{\partial^2 u}{\partial \varphi^2}=0
  \end{equation}$$
  $$\begin{equation}
  \frac{\mathrm{d^2R(r)}}{\mathrm{dr^2}}+\frac{2}{r}\frac{\mathrm{dR(r)}}{\mathrm{dr}}-\frac{l(l+1)}{r^2}R(r)=0
  \end{equation}$$
  $$\begin{equation}
  \frac{\mathrm{d^2\Phi(\varphi)}}{\mathrm{d\varphi^2}}+m^2\Phi(\varphi)=0 ,\quad m\in Z
  \end{equation}$$
  $$\begin{equation}
  (1-x^2)\frac{\mathrm{d^2y(x)}}{\mathrm{dx^2}}-2x\frac{\mathrm{dy(x)}}{\mathrm{dx}}+[l(l+1)-\frac{m^2}{1-x^2}]y(x)=0
  \end{equation}$$
  前面我们说过，当所研究的定解问题具有对称轴时，我们取对称轴为坐标系的z轴，这时的问题就变成与角度参数$\varphi$无关的问题，故此时函数u只依赖于$(r,\theta)$，它表现为在连带Legendre方程中m = 0，即$\Phi(\varphi)$为常数，不失普遍性，我们取$\Phi(\varphi)=1$,这样具有轴对称的Laplace方程的求解就变成求解径向方程和Legendre方程
  $$\begin{equation}
  \frac{\mathrm{d^2R(r)}}{\mathrm{dr^2}}+\frac{2}{r}\frac{\mathrm{dR(r)}}{\mathrm{dr}}-\frac{l(l+1)}{r^2}R(r)=0
  \end{equation}$$
  $$\begin{equation}
  (1-x^2)\frac{\mathrm{d^2y(x)}}{\mathrm{dx^2}}-2x\frac{\mathrm{dy(x)}}{\mathrm{dx}}+l(l+1)y(x)=0
  \end{equation}$$
  而Legendre方程在自然边界条件下的解就为Legendre多项式$y(x)=P_l(x)$
  径向方程是Euler型方程，对于标准的Euler型方程
  $$\begin{equation}
  a_0x^n\frac{\mathrm{d^ny}}{\mathrm{dx^n}}+a_1x^{n-1}\frac{\mathrm{d^{n-1}y}}{\mathrm{dx^{n-1}}}+\cdots+a_{n-1}x\frac{\mathrm{dy}}{\mathrm{dx}}+a_ny=0
  \end{equation}$$
  其通常的解法是令$x=e^t$作变量代换解出
  分析不难发现径向方程的奇点只有$r=0,r=\infty$两点，因此显然可以用二阶线性常微分方程的级数解发得到解析解
  但在这里，我们注意到当R(r)仅为r的某一幂次项时，方程中的各项的幂指数都是一致相同的，因此我们可以用极其熟练的待定系数法获得解析解
  令$R(r)=r^k$，代入径向方程可得到
  $$\begin{equation}
  k(k-1)r^{k-2}+2kr^{k-2}-l(l+2)r^{k-2}=0
  \end{equation}$$
  此方程的解为k=l,k=-(l+1)
  故径向方程的解为两个线性无关的解的线性组合，其待定系数由方程的定解条件确定
  $$\begin{equation}
  R(r)=C_lr^{l}+D_lr^{-(l+1)}
  \end{equation}$$
  至此，轴对称问题的Laplace方程在自然边界条件下要求的解的形式为
  $$\begin{equation}
  u(r,\theta)=\sum_{l=0}^{\infty}(C_lr^{l}+D_lr^{-(l+1)})P_l(\cos\theta)
  \end{equation}$$

## §    连带勒让德函数
- 当我们考虑的物理问题不具备极轴对称性时，而只是对角变量$\varphi$的函数要求具有单值性时，即对分离变量后的角变量$\varphi$的函数要求具有周期性的边界条件$\Phi(\varphi)=\Phi(\varphi+2n\pi)$，我们就需要求解连带Legendre方程
  $$\begin{equation}
  (1-x^2)\frac{\mathrm{d^2y}}{\mathrm{dx^2}}-2x\frac{\mathrm{dy}}{\mathrm{dx}}+[l(l+1)-\frac{m^2}{1-x^2}]y=0
  \end{equation}$$
  令$y=P_l(x)$,代入Legendre方程，并对x求m次微商
  $$\begin{equation}
  \frac{\mathrm{d^m}}{\mathrm{dx^m}}[(1-x^2)\frac{\mathrm{d^2P_l(x)}}{\mathrm{dx^2}}]-\frac{\mathrm{d^m}}{\mathrm{dx^m}}[2x\frac{\mathrm{dP_l(x)}}{\mathrm{dx}}]+l(l+1)\frac{\mathrm{d^m}}{\mathrm{dx^m}}P_l(x)=0
  \end{equation}$$
  对前两项应用Leibnitz莱布尼兹公式
  $$\begin{equation}
  (uv)^{(n)}=uv^{(n)}+nu'v^{(n-1)}+\frac{n(n-1)}{2}u''v^{(n-2)}+\cdots+u^{(n)}v
  \end{equation}$$
  可以得到
  $$\begin{equation}
  (1-x^2)\frac{\mathrm{d^2}}{\mathrm{dx^2}}[\frac{\mathrm{d^m}}{\mathrm{dx^m}}P_l]-2x(m+1)\frac{\mathrm{d}}{\mathrm{dx}}[\frac{\mathrm{d^m}}{\mathrm{dx^m}}P_l]+[l(l+1)-m(m+1)]\frac{\mathrm{d^m]}}{\mathrm{dx^m}}P_l(x)=0
  \end{equation}$$
  通过试探解我们可以得到解的形式为(玄学)
  $$\begin{equation}
  y(x)=(1-x^2)^{\frac{m}{2}}\frac{\mathrm{d^m}}{\mathrm{dx^m}}P_l(x)
  \end{equation}$$
  该解满足连带Legendre方程，同时对于本征值$l(l+1),l=0,1,2\cdots$，有y(x)亦满足自然边界条件$|y(x)|<\infty$，因此y(x)的形式就是我们所求的连带Legendre方程本征问题的本征解
  $$\begin{equation}
  P_{l}^{m}(x)=y(x)=(1-x^2)^{\frac{m}{2}}\frac{\mathrm{d^m}}{\mathrm{dx^m}}P_l(x)
  \end{equation}$$
  $P_{l}^{m}(x)$称为**连带Legendre函数**，亦称为m阶l次连带Legendre函数
  由于连带Legendre方程中含有m平方项，因此$P_l^{-m}$亦是方程的解.$P_l^{m}$与$P_l^{-m}$的关系为
  $$\begin{equation}
  P_l^{-m}(x)=(-1)^m\frac{(l-m)!}{(l+m)!}P_l^{m}(x), \quad m>0
  \end{equation}$$
- $P_{l}^{m}$的正交关系
  $$\begin{equation}
  \int_{0}^{\pi}P_{l}^{m}(\cos\theta)P_{l'}^{m}(\cos\theta)\sin\theta\mathrm{d\theta}=\frac{2}{2l+1}\cdot\frac{(l+m)!}{(l-m)!}\delta_{ll'} ,\quad m>0
  \end{equation}$$
  归一化因子为
  $$\begin{equation}
  \int_{-1}^{1}[P_l^m(x)]^2\mathrm{dx}=\frac{2}{2l+1}\frac{(l+m)!}{(l-m)!}
  \end{equation}$$


## §    球函数
- 球函数亦称为**球谐函数或球面调和函数**.
- 球函数在完全分离变量后所满足的S-L本征值问题为
  $$\begin{cases}
   \frac{1}{\sin\theta}\frac{\partial }{\partial \theta}(\sin\theta\frac{\partial Y}{\partial \theta})+\frac{1}{\sin^2\theta}\frac{\partial^ Y}{\partial \varphi^2}+l(l+1)Y=0  \\\\
   \Theta(\theta)|<\infty  \quad 0\le \theta\le \pi \\\\
   \Phi(\varphi)=\Phi(\varphi+2\pi)  \quad 0\le \varphi \le 2\pi
  \end{cases}$$
  我们之前得到的两个角度函数的本征函数分别为
  $$\begin{aligned}
   \Phi(\varphi) \sim e^{im\varphi}
  \end{aligned}$$
  $$\begin{aligned}
   \Theta(\theta) \sim P_l^{m}(\cos\theta)
  \end{aligned}$$
  对于每个本征值$l(l+1),l=0,1,2\cdots$和对应每个l的本征值$m\in Z$的本征函数$Y_{l,m}(\theta,\varphi)$的形式为
  $$\begin{equation}
  Y_{l,m}(\theta,\varphi)\sim P_l^m(\cos\theta)e^{im\varphi}
  \end{equation}$$
  由$P_l^m$的正交性和$e^{im\varphi}$的正交性，显然Y也能构成一组正交函数族，前面我们分别计算过二者的模，因而我们很容易得到正交归一化的球函数
  $$\begin{equation}
  Y_{l,m}(\theta,\varphi)=\sqrt{\frac{(2l+1)(l-m)!}{4\pi(l+m)!}}P_l^m(\cos\theta)e^{im\varphi}
  \end{equation}$$
  其中$P_l^m$和$e^{im\varphi}$的归一化因子分别为我们计算过的结果
  $$\begin{cases}
   \int_{0}^{2\pi}[e^{im\varphi}]^2\mathrm{d\varphi}=2\pi  \\\\
   \int_{-1}^{1}[P_l^m(x)]^2\mathrm{dx}=\frac{2}{2l+1}\frac{(l+m)!}{(l-m)!}
  \end{cases}$$
  我们称$Y_{l,m}(\theta,\varphi)$为**l阶球函数**，$l=0,1,\cdots,m\in Z$
  之前我们说过当$m\rightarrow -m$时，由
  $$\begin{equation}
  P_l^{-m}(\cos\theta)=(-1)^m\frac{(l-m)!}{(l+m)!}P_l^m(\cos\theta)
  \end{equation}$$
  我们有
  $$\begin{equation}
  Y_{l,-m}(\theta,\varphi)=(-1)^m\sqrt{\frac{(2l+1)(l-m)!}{4\pi(l+m)!}}P_l^{m}(\cos\theta)e^{-im\varphi}
  \end{equation}$$
  因此我们定义$Y_{l,m}(\theta,\varphi)$的复共轭为
  $$\begin{equation}
  Y_{l,m}^{\star}(\theta,\varphi)=(-1)^mY_{l,-m}(\theta,\varphi)
  \end{equation}$$
  由此定义，我们得到了球函数的正交关系
  $$\begin{equation}
  \int_{0}^{2\pi}\mathrm{d\varphi}\int_{0}^{\pi}Y_{lm}^{\star}Y_{l'm'}\sin\theta\mathrm{d\theta} =\delta_{ll'}\delta_{mm'} 
  \end{equation}$$
  可以看出，球函数可以构成正交归一完备空间的基向量，这一组基向量张成可一个Hilbert空间.对于每一个l，有2l+1个m，则对应有2l+1个基向量，构成一个2l+1维的子空间
  $$\begin{aligned}
   (Y_{lm}(\theta,\varphi),\quad l=0,1,2\cdots,\quad m=0,\pm 1,\cdots,\pm l)
  \end{aligned}$$
  由球函数为基向量张成的Hilbert空间是一个无穷维的函数空间，任何一个球面韩素都可以在其上展开
  $$\begin{equation}
  f(\theta,\varphi)=\sum_{l,m}f_{lm}Y_{lm}(\theta,\varphi)
  \end{equation}$$
  $$\begin{equation}
  f_{l,m}=\int_{0}^{2\pi}\mathrm{d\varphi}\int_{0}^{\pi}f(\theta,\varphi)Y_{lm}^{\star}(\theta,\varphi)\sin\theta\mathrm{d\theta}
  \end{equation}$$


---
# 柱函数
## §    贝塞尔函数
- 在时间和空间的分离变量下，波动方程和运输方程的空间部分为Helmholtz方程
  $$\begin{equation}
  (\nabla^2+k^2)u(\vec{r})=0
  \end{equation}$$
  当k=0时，方程就退化为Laplace方程
  Helmholtz方程在柱坐标系下分离变量得到以下方程
  $$\begin{equation}
  \frac{1}{\rho}\frac{\partial }{\partial \rho}(\rho\frac{\partial R}{\partial \rho})+(k^2+\lambda-\frac{v^2}{\rho^2})R=0
  \end{equation}$$
  $$\begin{equation}
  \Phi''-v^2\Phi=0 ,\quad v为实数
  \end{equation}$$
  $$\begin{equation}
  Z''-\lambda Z=0 ,\quad \lambda 为实数
  \end{equation}$$
  把径向方程进行变量代换，令$x=\sqrt{k^2+\lambda}\rho$，记$R(\rho)=y(x)$，就得到Bessel方程
  $$\begin{equation}
  \frac{\mathrm{d^xy}}{\mathrm{dx^2}}+\frac{1}{x}\frac{\mathrm{dy}}{\mathrm{dx}}+(1-\frac{v^2}{x^2})y=0
  \end{equation}$$
  此方程称为**v阶Bessel方程**
- **一：Bessel方程的解——Bessel函数**
  观察Bessel方程可知x=0是方程的正则奇点，在x=0的邻域内，可设方程方程的解具有级数形式
  $$\begin{equation}
  y(x)=x^s\sum_{k=0}^{\infty}a_kx^k,\quad a_0\neq 0
  \end{equation}$$
  带入Bessel方程可得
  $$\begin{equation}
  \sum_{k=0}^{\infty}a_k[(k+s)^2-v^2]x^k+\sum_{k=0}^{\infty}a_kx^{k+2}=0
  \end{equation}$$
  比较x的各幂次项系数，由$a_0\neq 0$，故由$x^0$项的系数可得指标方程
  $$\begin{equation}
  s^2-v^2=0
  \end{equation}$$
  由$x^1$项的系数，并考虑上式的结果有
  $$\begin{equation}
  a_1(2s+1)=0
  \end{equation}$$
  由于$s=\pm v$，而v是适合方程的定解问题，因此我们总是选取$a_1=0$
  对$x^k$项的系数进行反复递推可得
  $$\begin{equation}
  a_{2k}=(-1)^k\frac{1}{k!\prod_{i=1}^{k}(s+i)}\cdot\frac{1}{2^{2k}}a_0
  \end{equation}$$
  $$\begin{equation}
  a_{2k+1}=0 \quad (\because a_1=0)
  \end{equation}$$
  由于$s=\pm v$，当我们取$s_1=v$时，并取$a_0=\frac{1}{2^v\Gamma(1+v)}$，可得Bessel方程的级数解为
  $$\begin{equation}
  y_1(x)=\sum_{k=0}^{\infty}\frac{(-1)^k}{k!\Gamma(k+v+1)}(\frac{x}{2})^{2k+v}
  \end{equation}$$
  $$\begin{equation}
  \Gamma(z)=\int_{0}^{\infty}e^{-t}t^{z-1}\mathrm{dt} \quad t\in R
  \end{equation}$$
  $$\begin{equation}
  \Gamma(n+1)=n!
  \end{equation}$$
  把$y_1(x)$记为$J_v(x)$，即
  $$\begin{equation}
  J_v(x)=\sum_{k=0}^{\infty}\frac{(-1)^k}{k!\Gamma(k+v+1)}(\frac{x}{2})^{2k+v}
  \end{equation}$$
  当取$s_2=-v$时，并取$a_0=\frac{(-1)^k}{2^v\Gamma(-v+1)}$时，可得另一线性无关的级数解
  $$\begin{equation}
  J_{-v}(x)=y_2(x)=\sum_{k=0}^{\infty}\frac{(-1)^k}{k!\Gamma(k-v+1)}(\frac{x}{2})^{2k-v}
  \end{equation}$$
  两级数的收敛半径均为$R=\infty$
  因此在v不为整数时，Bessel方程的通解为
  $$\begin{equation}
  y(x)=C_1J_v(x)+C_2J_{-v}(x)
  \end{equation}$$
  当v为整数时，根据常微分方程级数解的理论，只能得到一个级数解，另一个级数解的形式参照前文中对二阶常微分线性方程解法中的介绍

- **二：整数阶Bessel函数**
- 对于众多的物理问题，在Helmholtz方程进行柱坐标下的分离变量时，对$\Phi(\varphi)$满足的方程要求具有自然周期边界条件$\Phi(\varphi)=\Phi(\varphi+2\pi)$，此时v的取值为整数m，此时Bessel方程的解为
  $$\begin{equation}
  J_m(x)=\sum_{k=0}^{\infty}\frac{(-1)^k}{k!(m+k)!}(\frac{x}{2})^{m+2k}
  \end{equation}$$
  $J_m(x)$称为m阶Bessel函数，它是整数阶Bessel函数.
  由伽马函数的性质
  $$\begin{aligned}
   \Gamma(n+1)=n\Gamma(n)
  \end{aligned}$$
  $$\begin{aligned}
   |\Gamma(0)|=|\Gamma(-1)|=|\Gamma(-n)| =\infty \quad n为正整数
  \end{aligned}$$
  因此对于$J_{-m}(x)$，当k < m时，求和部分的前m项均为零，即
  $$\begin{aligned}
  J_{-m}(x) &=\sum_{k=0}^{\infty}\frac{(-1)^k}{k!\Gamma(k-m+1)}(\frac{x}{2})^{-m+2k} \\\\
  &=(-1)^m\sum_{n=0}^{\infty}\frac{(-1)^n}{n!\Gamma(n+m+1)}(\frac{x}{2})^{m+2n} \\\\
  &=(-1)^mJ_m(x)     \quad n=k-m
  \end{aligned}$$
  这表明两个解是线性相关的，即不是Bessel方程的线性独立的解，因此我们需要寻求另一个线性独立的解
  我们说过，当v不是整数时，两个解是线性无关的，因此我们可以寻找由$J_v(x)$与$J_{-v}(x)$的线性组合，使之对任何v都与之线性无关.这样的解称为**Neumann诺伊曼函数$N_v(x)$**
  $$\begin{equation}
  N_v(x)=\frac{\cos v\pi J_v(x)-J_{-v}(x)}{\sin v\pi}
  \end{equation}$$
  Neumann函数通常也称为**第二类Bessel函数**，而前面说的$J_v(x)$称为**第一类Bessel函数**
  对于Neumann函数，当$v\rightarrow m$时，它是$\frac{0}{0}$型未定式，由L’Hospital洛必达法则可以得到
  $$\begin{equation}
  N_m(x)=\lim_{v\to m}N_v(x)=\frac{1}{\pi}\Big[(\frac{\partial J_v}{\partial v})\_{v=m}-(-1)^m(\frac{\partial J_{-v]}}{\partial v})\_{v=m}\Big]
  \end{equation}$$
  具体的表达式需将第一类Bessel函数代入计算
  $$\begin{aligned}
   N_m(x)=&\frac{2}{\pi}J_m(x)\ln\frac{x}{2}-\frac{1}{\pi}\sum_{k=0}^{m-1}\frac{(m-k-1)}{k!}(\frac{x}{2})^{2k-m} \\\\
  &-\frac{1}{\pi}\sum_{k=0}^{\infty}(-1)^k\frac{1}{k!(m+k)!}[\Phi(m+k+1)+\Phi(k+1)](\frac{x}{2})^{2k+m}
  \end{aligned}$$
  其中$m=0,1,2,\cdots$，并约定当m=0时，右边第二项的求和式要从等式中去掉
  $\Phi$函数的定义是：$\Phi$=\frac{\Gamma'(z)}{\Gamma(z)},则$\Phi(k+1)=-\gamma+1+\frac{1}{2}+\cdots+\frac{1}{k}$，其中$\gamma$为Euler常数，$\Phi(1)=-\gamma=-0.577216$
  于是当m为整数时，整数阶Bessel方程的两个线性独立的解为$J_m(x)$和$N_m(x)$-

- **三：整数阶Bessel函数的简单性质**
  由m阶Bessel函数的表达式可知
  $$\begin{aligned}
  J_m(x)=\sum_{k=0}^{\infty}\frac{(-1)^k}{k!(m+k)!}(\frac{x}{2})^{m+2k}
  \end{aligned}$$
  $$\begin{equation}
  J_m(-x)=(-1)^mJ_m(x)
  \end{equation}$$
  由此关系可以看出，当m为偶数时，函数为偶函数，当m为奇数时，函数为奇函数
  由其表达式可以知道$J_m(x)$在x=0点的性质
  $$\begin{equation}
  J_{0}(0)=1 ,\quad  J_m(0)=0,(m\neq 0)
  \end{equation}$$
  同时，由$J_m(x)$和$J_{-m}(x)$的关系可得
  $$\begin{equation}
  N_{-m}(x)=(-1)^mN_m(x)
  \end{equation}$$
  因此他们也是线性相关的


## §    贝塞尔函数的递推关系
- 根据第一类Bessel函数的表达式，我们做如下微商
  $$\begin{aligned}
   \frac{\mathrm{d}}{\mathrm{dx}}(x^vJ_v)&=\frac{\mathrm{d}}{\mathrm{dx}}\Big[2^v\sum_{k=0}^{\infty}\frac{(-1)^k}{k!\Gamma(v+k+1)}(\frac{x}{2})^{2(v+k)}\Big] \\\\
   &=2^v\sum_{k=0}^{\infty}\frac{(-1)^k(v+k)}{k!\Gamma(k+v+1)}(\frac{x}{2})^{2(v+k)-1} \\\\
   &=x^v\sum_{k=0}^{\infty}\frac{(-1)^k}{k!\Gamma(v+k)}(\frac{x}{2})^{v-1+2k} \\\\
   &=x^vJ_{v-1}(x)
  \end{aligned}$$
  同样可得
  $$\begin{aligned}
  \frac{\mathrm{d}}{\mathrm{dx}}(x^{-v}J_v)=-x^{-v}J_{v+1}(x)
  \end{aligned}$$
  **特别地，当v=0时可得**
  $$\begin{equation}
  J_{0}'(x)=-J_1(x)
  \end{equation}$$
  有了此关系和我们旋即推出的Bessel函数基本关系就可以计算出所有整数阶Bessel函数
  另一方面，直接根据求导法则我们有
  $$\begin{aligned}
  \frac{\mathrm{d}}{\mathrm{dx}}(x^vJ_v(x))=v\cdot x^{v-1}J_v(x)+x^vJ_v'(x)
  \end{aligned}$$
  $$\begin{aligned}
   \frac{\mathrm{d}}{\mathrm{dx}}(x^{-v}J_v(x))=-vx^{-v-1}J_v(x)+x^{-v}J_v'(x)
  \end{aligned}$$
  互相对比可得
  $$\begin{equation}
  vJ_v+xJ_v'=xJ_{v-1}
  \end{equation}$$
  $$\begin{equation}
  -vJ_v+xJ_v'=-xJ_{v+1}
  \end{equation}$$
  于是我们可以得到**Bessel函数的基本递推关系**,下述的基本递推关系完全适用于第二类Bessel函数，即Neumann函数
  $$\begin{equation}
  J_{v-1}+J_{v+1}=\frac{2v}{x}J_v
  \end{equation}$$
  $$\begin{equation}
  J_{v-1}-J_{v+1}=2J_v'
  \end{equation}$$
  $$\begin{equation}
  N_{v-1}+N_{v+1}=\frac{2v}{x}N_v
  \end{equation}$$
  $$\begin{equation}
  N_{v-1}-N_{v+1}=2N_v'
  \end{equation}$$
  根据最开始得到的两个微商递推式我们还可以得到如下两个关系式
  $$\begin{equation}
  (\frac{\mathrm{d}}{x\mathrm{dx}})^m(x^vJ_v)=x^{v-m}J_{v-m}
  \end{equation}$$
  $$\begin{equation}
  (\frac{\mathrm{d}}{x\mathrm{dx}})^m(x^{-v}J_v)=(-1)^m x^{-(v+m)}J_{v+m}
  \end{equation}$$
  通过这两个式子我们可以得到半整数阶的Bessel函数
  对于Bessel函数$J_v(x)$，当n为半整数时，即$v=n+\frac{1}{2}，n\in Z$，称为半整数阶Bessel函数
  取n=0研究$v=\frac{1}{2}$的Bessel函数
  $$\begin{equation}
  J_{\frac{1}{2}}(x)=\sum_{k=0}^{\infty}\frac{(-1)^k}{k!\Gamma(k+\frac{3}{2})}(\frac{x}{2})^{2k+\frac{1}{2}}
  \end{equation}$$
  由$\Gamma$函数的倍乘公式
  $$\begin{equation}
  \Gamma(2z)=2^{2z-1}\pi^{-\frac{1}{2}}\Gamma(z)\Gamma(2+\frac{1}{2})
  \end{equation}$$
  并令$z=x,x=k+1$可得
  $$\begin{aligned}
   2^{2k+1}\Gamma(k+1)\Gamma(k+\frac{3}{2})=\pi^{\frac{1}{2}}\Gamma(2k+2)
  \end{aligned}$$
  代入可得
  $$\begin{equation}
  J_{\frac{1}{2}}(x)=\sqrt{\frac{2}{\pi x}}\sum_{k=0}^{\infty}\frac{(-1)^k}{(2k+1)!}x^{2k+1}=\sqrt{\frac{2}{\pi x}}\sin x
  \end{equation}$$
  类似地可得
  $$\begin{equation}
  J_{-\frac{1}{2}}(x)=\sqrt{\frac{2}{\pi x}}\cos x
  \end{equation}$$
  
## §    柱函数的定义
- 如果函数$y_v(x)$满足如下递推关系式
  $$\begin{equation}
  y_{v-1}+y_{v+1}=\frac{2v}{x}y_v
  \end{equation}$$
  $$\begin{equation}
  y_{v-1}-y_{v+1}=2y_v'
  \end{equation}$$
  或者满足与上面两式等价的关系
  $$\begin{equation}
  \frac{\mathrm{d}}{\mathrm{dx}}(x^vy_v)=x^vy_{v-1}
  \end{equation}$$
  $$\begin{equation}
  \frac{\mathrm{d}}{\mathrm{dx}}(x^{-v}y_v)=x^{-v}y_{v+1}
  \end{equation}$$
  则我们把这类函数称为**柱函数**
  **柱函数必须满足Bessel方程，但满足Bessel方程的不一定是柱函数** -->


## §    整数阶贝塞尔函数的生成函数







$$\begin{equation}\end{equation}$$
$$\begin{equation}\end{equation}$$
$$\begin{equation}\end{equation}$$
## §    贝塞尔方程的本征值


## §    虚宗量贝塞尔函数


## §    汉克尔函数


## §    球贝塞尔函数

---
# 格林函数法
## §    微分算子的基本解和格林函数


## §    拉普拉斯算子的基本解


## §    拉普拉斯算子的格林函数


## §    拉普拉斯算子的镜像格林函数法


## §    亥姆霍兹算子的基本解


## §    运输算子的格林函数


## §    波动算子的基本解

---
# 其他求解方法及方程
## §    积分变换法


## §    行波法


## §    冲量定理法


## §    薛定谔方程与谐振子腔


## §    埃尔米特多项式的性质


---
# 非线性数学物理方程
## §    惠更斯等时摆问题


## §    KdV方程和孤立波


## §    非线性方程的其次平衡解法

---
# 泛函分析
## §    泛函的概念
- 泛函这一概念时函数概念的推广.我们知道函数是指由数域K到K上的映射.泛函从较广泛的意义上讲可以定义为从线性空间L到数域K上的映射，记为F[L].
  $$\begin{equation}
  F[L]：L\rightarrow K
  \end{equation}$$
- 线性空间包括了n维实数域和n为复数域，以及定义在他们上面的函数空间，例如Hilbert空间
- **我们接下来讲述的泛函是狭义的泛函，并且是实函数**，它是指实函数的集合到实数域上的映射.设定义在$R^n$上k阶连续可微的实函数的集合记为$C^k(R^n)$，则映射记为
  $$\begin{equation}
  C^k(R^n)\rightarrow R
  \end{equation}$$
  若$x\in R$，(x为浓缩写法，即$x=(x_1,x_2,\cdots,x_n)$，y(x)为定义在n维实空间中k阶连续可微的实函数，$y(x)\in C^k(R^n)$，则泛函F[y(x)]为
  $$\begin{equation}
  F[y(x)]: y(x)\mapsto a,\quad a\in R
  \end{equation}$$
  y(x)称为**泛函F[y(x)]的宗量**，泛函的定义域称为**容许函数类**.上式表示，对于容许函数类中的每一个确定的函数y(x)，泛函F[y(x)]有一确定的实数值a.
  **通俗地讲，泛函就是一类函数作为自变量的函数，或简单地说泛函就是函数的函数**

## §    泛函的变分
- 首先我们要对泛函F[y(x)]的宗量y(x)(或称自变量)引入**接近度**的概念.设宗量y(x)都是定义在区域$\Omega\in R^n$上的函数，对于某一宗量$y_0(x)$，若有另一个宗量y(x)非常地接近它，即在他们的定义域内，对于一切$x\in\Omega$，存在着一个大于零的小量，使二者之差的模满足
  $$\begin{equation}
  |y(x)-y_0(x)|<\delta
  \end{equation}$$
  我们称宗量$y(x)$与$y_0(x)$有**零阶的接近度**
- 若对于$y(x)$与$y_0(x)$的k阶微商，有
  $$\begin{equation}
  |y^k(x)-y_0^k(x)|<\delta
  \end{equation}$$
  我们称$y(x)$与$y_0(x)$有**k阶的接近度**
- 下面我们将陈述泛函的连续性，线性泛函和泛函变分的概念，处于方便考虑，我们将仅仅讨论一维实空间$x\in R$的宗量y(x)的情况
- **定义**
  如果对于一个任意给定的小正数$\varepsilon$，可以找到这样的$\delta$，当
  $$\begin{aligned}
   |y(x)-y_0(x)|<\delta \\\\
   |y'(x)-y_0'(x)|<\delta \\\\
   \cdots \\\\
   |y^k(x)-y_0^k(x)|<\delta
  \end{aligned}$$
  时，有
  $$\begin{equation}
  |F[y(x)]-F[y_0(x)]|<\varepsilon
  \end{equation}$$
  我们称泛函F[y(x)]在$y(x)=y_0(x)$处是**k阶接近的连续泛函**.
- **定义**
  如果泛函F[y(x)]满足
  $$\begin{equation}
  F[ay_1(x)+by_2(x)]=aF[y_1(x)]+bF[y_2(x)]
  \end{equation}$$
  我们称泛函为**线性泛函**
- **定义**
  泛函的宗量的增量是指两个函数之间的差
  $$\begin{equation}
  \Delta y=y(x)-y_0(x)
  \end{equation}$$
  当$y(x)$与$y_0(x)$是零阶或k阶接近的，则
  $$\begin{equation}
  \delta y=y(x)-y_0(x)
  \end{equation}$$
  称为泛函F[y(x)]的**宗量y(x)的变分**，$\delta y$仍然是x的函数，并且有
  $$\begin{equation}
  (\delta y)^{(k)}=y^{(k)}(x)-y_0^{(k)}(x)=\delta y^{(k)}(x)
  \end{equation}$$
- **定义**
  若线性泛函F[y(x)]
  $$\begin{equation}
  \Delta F[y(x)]=F[y(x)+\Delta y]-F[y(x)]
  \end{equation}$$
  称为**泛函的增量**
  若泛函的增量可以表示为
  $$\begin{equation}
  \Delta F(y(x))=L[y(x),\delta y]+\beta(y(x),\delta y)\cdot \max|\delta y|
  \end{equation}$$
  其中$L[y(x),\delta y]$称为对于$\delta y$的泛函增量$\Delta F$中的**线性主部**，我们称$L[y(x),\delta y]$为**泛函F[y(x)]的变分**
- **泛函的变分与函数微商的关系**
  在早已学过的高等数学或数学分析中，我们以单变量函数y(x)为例，当自变量产生一个固定的微小增量时，我们引入参量$\alpha$，考虑带参数$\alpha$的函数$y(x+\alpha\Delta x)$，有
  $$\begin{aligned}
  &\lim_{\Delta x\to 0}\frac{\partial }{\partial \alpha}y(x+\alpha\Delta x)\Big|\_{\alpha=0} \\\\
  &=\lim_{\Delta x\to 0}[y'(x+\alpha\Delta x)\cdot\frac{\partial }{\partial \alpha}(x+\alpha\Delta x)]_{\alpha=0} \\\\
  &=y'(x)\cdot\mathrm{dx} \\\\
  &= \mathrm{dy}
  \end{aligned}$$
  上式表明函数$y(x)$的微分可以看成带参数$\alpha$的函数对$\alpha$的微商在$\alpha=0$的点的值
  因此，对于泛函，我们也可以进行这样的操作，我们可以将泛函F[y(x)]的变分$\delta F$看成带参数$\alpha$的泛函$F[y(x)+\alpha\delta y]$对$\alpha$的微商在$\alpha=0$点的值
  $$\begin{equation}
  \delta F[y(x)]=\frac{\partial }{\partial \alpha}F[y(x)+\alpha\delta y]_{\alpha=0}
  \end{equation}$$
  将右侧的偏微分进一步计算
  $$\begin{aligned}
  &\frac{\partial }{\partial \alpha}F[y(x)+\alpha\delta y]\\\\
  &=\frac{\partial F[y(x)+\alpha\delta y]}{\partial [y(x)+\alpha\delta y]}\cdot\frac{\partial [y(x)+\alpha\delta y]}{\partial \alpha} \\\\
  &=\frac{\partial F[y(x)]}{\partial y}\cdot\delta y
  \end{aligned}$$
  因此我们得到泛函的变分与微商之间的关系
  $$\begin{equation}
  \delta F[y(x)]=\frac{\partial F[y(x)]}{\partial y}\cdot\delta y
  \end{equation}$$
  即可表述为泛函的变分等于泛函的偏导数乘以泛函的宗量的变分
  这是泛函的小增量的线性主部的表达式，是**泛函变分最基本的运算法则**
  对于线性泛函，我们有
  $$\begin{equation}
  L[y(x),\alpha\delta y]=\alpha L[y(x),\delta y]
  \end{equation}$$

---
# 变分法原理
## §    泛函的极值
- **定义：泛函的极值**
  若泛函F[y(x)]对与$y=y_0(x)$接近的宗量$y(x)$，都有
  $$\begin{equation}
  \Delta F=F[y(x)]-F[y(x_0)]\ge 0
  \end{equation}$$
  则称泛函F[y(x)]在$y=y_0(x)$上达到极小值
  同理若满足
  $$\begin{equation}
  \Delta F=F[y(x)]-F[y(x_0)]\le 0
  \end{equation}$$
  则称泛函F[y(x)]在$y=y_0(x)$上达到极大值
- **定理**
  如果具有变分的泛函F[y(x)]在$y=y_0$达到极值(极大值或极小值)，则在$y=y_0(x)$上有
  $$\begin{equation}
  \delta F[y_0(x)]=0
  \end{equation}$$


## §    变分原理与欧拉-拉格朗日方程
- 本节我们仅考虑以如下定积分形式出现的一类简单泛函I[y(x)]
  $$\begin{equation}
  I[y(x)]=\int_{x_A}^{X_B}f(x,y,y')\mathrm{dx}
  \end{equation}$$
  其中f(x,y,y')为已知的数学形式，且f(x,y,y')对其宗量x、y(x)、y'(x)具有二阶连续的偏导数，同时对于$x_A$，$x_B$两点，有$y(x_A)=y_A$和$y(x_B)=y_B$都是已知的，即在二维平面上两个端点是固定的
  ![变分原理](\pic/变分原理.png)
  如上图所示，我们引入单参数比较函数$\bar{y}(x,\alpha)$,且其满足下列三个条件

     1. $\bar{y}(x_A,\alpha)=y(x_A)=y_A$
     $\bar{y}(x_B,\alpha)=y(x_B)=y_B$
     上述俩式对一切参数都成立
     2. $\bar{y}(x,0)=y(x)$为所期望的极值函数
     3. $\bar{y}(x,\alpha)$对$x,\alpha$的一阶、二阶微商都是连续函数 
     
  因此由比较函数构成的泛函为
  $$\begin{equation}
  I[\alpha]=\int_{x_A}^{x_B}f(x,\bar{y}(x,\alpha),\frac{\partial }{\partial x}\bar{y}(x,\alpha))\mathrm{dx}
  \end{equation}$$
  根据泛函极值的必要条件可知
  $$\begin{equation}
  \delta I[y(x)]=\frac{\mathrm{d}}{\mathrm{d\alpha}}I(\alpha)\Big|_{\alpha=0}=0
  \end{equation}$$
  在此条件下我们导出泛函I[y(x)]的宗量y(x)满足的运动方程，由
  $$\begin{aligned}
   \frac{\mathrm{dI}}{\mathrm{d\alpha}}&=\int_{x_A}^{x_B}[\frac{\partial f}{\partial \bar{y}}\cdot\frac{\mathrm{d\bar{y}}}{\mathrm{d\alpha}}+\frac{\partial f}{\partial \bar{y'}}\cdot\frac{\mathrm{d\bar{y'}}}{\mathrm{d\alpha}}]\mathrm{dx} \\\\
   &=\int_{x_A}^{x_B}[\frac{\partial f}{\partial \bar{y}}\cdot\frac{\mathrm{d\bar{y}}}{\mathrm{d\alpha}}+\frac{\partial f}{\partial \bar{y'}}\cdot\frac{\mathrm{d}}{\mathrm{dx}}(\frac{\mathrm{d\bar{y}}}{\mathrm{d\alpha}})]\mathrm{dx}
  \end{aligned}$$
  对上式右端积分的第二项进行分部积分
  $$\begin{aligned}
  \int_{x_A}^{x_B}\frac{\partial f}{\partial \bar{y'}}\cdot\frac{\mathrm{d}}{\mathrm{dx}}
  \end{aligned}$$



  


$$\begin{equation}\end{equation}$$
$$\begin{equation}\end{equation}$$
$$\begin{equation}\end{equation}$$
$$\begin{equation}\end{equation}$$
## §    哈密顿原理


## §    哈密顿泛函和正则方程


## §    带约束条件的泛函变分


## §    诺德定理
---