---
title: Electromagnetic basis of optics
math: true
tags: Wave optics
categories: Physics
---

***
[toc]
***
# 光的电磁波性质
***
## 基本理论
麦克斯韦（Maxwell）总结推广了**稳定电磁场**和**似稳电磁场**的基本规律，提出**时变场**情况下的电磁场传播规律，归结为麦克斯韦方程组，它有**积分**和**微分**两种形式，在实际应用中通常用微分形式来求解电磁场中**某一给定点的场量**.表示如下

*   $\nabla \cdot\vec D=\rho$
*   $\nabla \cdot\vec B=0$
*   $\nabla \times\vec E=-\frac{\partial\vec B}{\partial t}$
*   $\nabla \times\vec H=\vec j+\frac{\partial\vec D}{\partial t}$

其中

*   $\vec D$ 表示**电位移矢量**.
*   $\vec E$ 表示**电场强度**.
*   $\vec B$ 表示**磁感应强度**.
*   $\vec H$ 表示**磁场强度**.
*   $\rho$ 表示**电荷密度**.
*   $\vec j$ 表示**传导电流密度**.
*   $\frac{\partial\vec D}{\partial t}$ 表示**位移电流密度**.

在**静止**的，**各向同性**媒质中有

*   $\vec D=\varepsilon\vec E$ 
*   $\vec B=\mu \vec H$ 
*   $\vec j=\sigma \vec E$

其中

*   $\varepsilon$ 是介电常数
*   $\mu$ 是磁导率
*   $\sigma$ 是电导率.

各向同性均匀介质中， $\varepsilon,\mu$ 是常数， $\sigma=0$ .

**真空中**

*   $\varepsilon=\varepsilon_0=8.8542\times 10^{-12}\rm C^2/N\cdot m^2.$
*   $\mu=\mu_0=4\pi\times 10^{-7}\rm N\cdot s^2/C^2.$ （非磁性物质亦如此）

## 电磁场的波动性
若满足以下条件
*   无限大各向同性均匀介质（ $\varepsilon,\mu$ 为常数）.
*   电磁场远离辐射源，不存在自由电荷和传导电流（ $\rho=0,\vec j=0$ ）.

则麦克斯韦方程组化为

*   $\nabla \cdot\vec E=0$
*   $\nabla \cdot\vec B=0$
*   $\nabla \times\vec E=-\frac{\partial\vec B}{\partial t}$
*   $\nabla \times\vec B=\varepsilon\mu\frac{\partial\vec E}{\partial t}$

根据场论的相关知识对上述诸式进行处理，并令 $v=\frac{1}{\sqrt{\varepsilon\mu}}$ 得到

*   $\color{red}{\nabla^2\vec E-\frac{1}{v^2}\frac{\partial^2\vec E}{\partial t^2}=0}$
*   $\color{red}{\nabla^2\vec B-\frac{1}{v^2}\frac{\partial^2\vec B}{\partial t^2}=0}$

其中 $v=\frac{1}{\sqrt{\varepsilon\mu}}$ 即是电磁波的传播速度.电磁波在真空中传播时，由前述数据计算得 $c=\frac{1}{\sqrt{\varepsilon_0\mu_0}}=2.99794\times 10^8\rm m/s.$ 实验结果也与之吻合.

在引入相对介电常数 $\varepsilon_r=\frac{\varepsilon}{\varepsilon_0}$ 与相对磁导率 $\mu_r=\frac{\mu}{\mu_0}$ 的情况下，电磁波在各种介质中的传播速度为 $v=\frac{c}{\sqrt{\varepsilon_r\mu_r}}.$

下面定义介质的**折射率** $n=\frac{c}{v}$ ，可用 $n=\sqrt{\varepsilon_r\mu_r}$ 来**计算**.考虑到**除了磁性物质**，**大多数物质** $\mu_r\approx 1$ ，则可认为 $n=\sqrt{\varepsilon_r}.$

有关电磁场等更详细的知识在电动力学理论当中，光学理论将以此为基础，探究电磁波传播的规律.

**2\. 具体形式**
------------

上述讨论当中，一个比较重要的结论就是将 $\vec E, \vec B$ 的方程化为

*   $\color{red}{\nabla^2\vec E-\frac{1}{v^2}\frac{\partial^2\vec E}{\partial t^2}=0}$
*   $\color{red}{\nabla^2\vec B-\frac{1}{v^2}\frac{\partial^2\vec B}{\partial t^2}=0}$

下面将由此讨论电磁波具体是怎样传播的.

2.1 平面波（Plane Waves）
--------------------

平面波，顾名思义，其波阵面是平面，意味着其传播方向的垂面上各点具有一些相同的属性（ $\vec E, \vec B$ ，主要是相位相同，也称等相面）.

  

$\color{lime}{沿\vec z方向传播}$

不妨假设在直角坐标系Oxyz中平面波沿z轴传播，那么其 $\vec E,\vec B$ 只与 $z$ 的坐标以及时间t相关（即从空间与时间的角度观察）.那么上述 $\vec E,\vec B$ 的**波动方程**可进一步简化为

*   $\frac{\partial^2\vec E}{\partial z^2}-\frac{1}{v^2}\frac{\partial^2\vec E}{\partial t^2}=\rm0$
*   $\frac{\partial^2\vec B}{\partial z^2}-\frac{1}{v^2}\frac{\partial^2\vec B}{\partial t^2}=\rm0$

求解此**波动方程**会有如下形式：

*   $\vec E =f\Big(\frac{z}{v}-t\Big)$
*   $\vec B =f\Big(\frac{z}{v}-t\Big)$

这是波动方程的**通解**，它们表示以**速度** $v$ 沿 $z$ 轴**正方向**传播的**平面波**.可以进一步写出简谐振动形式的**特解**.（**有趣的东西从这里开始**）

*   $\color{red}{\vec E=\vec A\cos\Big[\omega\Big(\frac{z}{v}-t\Big)\Big]}$
*   $\color{red}{\vec B=\vec A'\cos\Big[\omega\Big(\frac{z}{v}-t\Big)\Big]}$

这就出现了一些具体的参数，其中

*   $\vec A,\vec A’$ 分别是**电场**和**磁场**的**振幅矢量**.（其方向表示偏振方向）
*   $v$ 就是平面波在介质中的**传播速度**.
*   $\omega$ 是**角频率**.
*   $\Big[\omega\Big(\frac{z}{v}-t\Big)\Big]$ 是**相位**（phase）.（表示相应**时刻**和**空间**点的**振动状态**）

为了更直观方便地描述，特此引入一些新的量：

*   $\omega=2\pi\nu=\frac{2\pi}{T}$ （显然 $\nu=\frac{1}{T}$ ）
*   $\lambda=vT$ （介质中）以及 $\lambda_0=cT$ （真空中）
*   那么显然就有 $\lambda=\frac{\lambda_0}{n}$

其中

*   $\nu$ 是振动频率（前式揭示了 $\color{blue}{角频率\omega}$ 与 $\color{blue}{振动频率\nu}$ 的关系.应注意：角频率是指**单位时间内相角变化的弧度值**.而振动频率是指**单位时间内完整振动一周的次数**.）
*   $T$ 是振动周期
*   $\lambda$ 是光波波长（ $\lambda_0$ 是真空中的波长）（即一个振动周期内，光传播距离）
*   $n$ 为介质的折射率

> 考虑到光与物质相互作用时起主要作用的是电矢量，那么下面将不在考察 $\vec B$ ，而以 $\vec E$ 作为**光矢量**.

那么综上所述， $\vec E=\vec A\cos\Big[2\pi\Big(\frac{z}{\lambda}-\frac{t}{T}\Big)\Big].$

这样描述依然很繁琐，但若引入波传播方向上的**波矢量** $\vec k=k\vec k_0.$

$k$ 是 $\vec k$ 的模， $\vec k_0$ 是单位矢量.该矢量方向指的是波传播的方向，即波面的法线方向.其大小为 $k=\frac{2\pi}{\lambda}=\frac{\omega}{v}$ （**空间角频率**）.

*   于是描述就变得简单多了： $\color{red}{\vec E=\vec A\cos( kz-\omega t)}.$

  

$\color{lime}{沿任意方向 \vec k 传播}$

注意上式中的 $kz-\omega t$ ，这里 $kz$ 项描述了空间相关的量， $\omega t$ 项描述了时间相关的量.

而对于沿任意方向传播的情况，就要借助k的矢量形式 $\vec k$ 与指定点的位置矢量 $\vec r$ 综合来确定，即 $\color{red}{\vec E=\vec A\cos(\vec k\cdot\vec r-\omega t)}.$

如下图所示， $\vec k\cdot\vec r$ 指的就是 $kz’$ ，其中 $z’$ 是 $r$ 在 $k$ 上的投影，道理和沿 $z$ 轴方向传播的情况相同.

  

![](https://pic1.zhimg.com/v2-04c8ecf75e229c64e7bb353ff5c4db80_b.jpg)  
沿任意方向k传播的电磁波

  

具体而言，也可以写成 $\vec E=\vec A\cos[ k( x\cos\alpha+y\cos\beta+z\cos\gamma)-\omega t].$

其中 $x,y,z$ 是所考察点 $P$ 的坐标，$\cos\alpha,\cos\beta,\cos\gamma$ 是 $\vec k$ 的**方向余弦**.

  

$\color{lime}{复数表示}$

为了**简化计算**，特此引入光波的复数形式的表示

$\vec E=\vec Ae^{i (\vec k\cdot\vec r\mit -\omega t)}$

但上式相当于 $\vec E=\vec A(\cos(\vec k\cdot\vec r-\omega t)+i\sin(\vec k\cdot\vec r-\omega t)).$ 这里应理解为实际只存在复数形式中的**实数部分**.（如此计算并不影响研究其传播规律）

以上的讨论都在同一式中既考虑空间又考虑时间，但更常见的情况是观察某一时刻光波在空间的分布，因此可以将这个复数表示分为**空间相位因子** $e^{i\vec k\cdot\vec r}$ 和**时间相位因子** $e^{i\omega t}.$

*   称 $\color{red}{\tilde {\vec E}=\vec Ae^{i\vec k\cdot\vec r}}$ 为**复振幅**.

具体而言，也可以写成 $\tilde {\vec E}=\vec A e^{i\vec k( x\cos\alpha+y\cos\beta+z\cos\gamma)}.$

2.2 球面波（Spherical Waves）
------------------------

同理，球面波的波阵面是球面，仿照平面波的做法，可以将球面波表示为复数形式 $E=\frac{A_1}{r}e^{i(kr-\omega t)}$

其中 $A_1$ 离开点光源单位距离处的振幅.

注意：

*   球面波与平面波不同，无所谓传播方向，因此不表示为矢量形式.
*   球面波的振幅与传播的距离成反比，这一点与平面波不同，后者振幅一般与传播距离无关.
*   至于其复振幅表示： $\color{red}{发散}$ 的球面波 $\tilde E=\frac{A_1}{r}e^{ikr}$ ； $\color{red}{会聚}$ 的球面波 $\tilde E=\frac{A_1}{r}e^{-ikr}$ .

2.3 柱面波（Cylindrical Waves）
--------------------------

复数形式 $E=\frac{A_1}{\sqrt r}e^{i{kr-\omega t}}$

复振幅表示 $\tilde E=\frac{A_1}{\sqrt r}e^ikr$

2.4电磁波的性质
---------

这里主要讲**平面波**.

对平面波的复数表示取散度得到 $\nabla\cdot\vec E=\vec A\cdot\nabla\cdot e^{i(\vec k\cdot\vec r-\omega t)} = i\vec k\cdot\vec E= 0.$ 可知

*   $\vec k\cdot\vec E=0$ ，二者相**垂直**.
*   同理取 $\vec B$ 的散度得$\vec k\cdot\vec B=0$ ，二者相**垂直**.

（电矢量与磁矢量方向均垂直于传播方向，平面波是横波）

将 $\vec E=\vec A e^{i (\vec k\cdot\vec r -\omega t)}， \vec B=\vec A’ e^{i (\vec k\cdot\vec r -\omega t)}$ 代入 $\nabla \times\vec E =-\frac{\partial \vec B}{\partial t}$ ，利用 $\nabla \times\vec B=\varepsilon\mu\frac{\partial \vec E}{\partial t}$ 运算得到 $i\omega\vec B= ik(\vec k_0\times\vec E)$ .（其中 $\vec k_0$ 是波矢量 $\vec k$ 的单位矢量）

可进一步改写为 $\vec B=\sqrt{\varepsilon\mu}(\vec k_0\times\vec E).$

*   意味着 $\color{red}{\vec E,\vec B,\vec k_0相互垂直}$ ，构成**右手螺旋系**（注意1.1所提及的 $\vec E,\vec D$ **方向相同**， $\vec B,\vec H$ **方向相同**可获得更多结论）.

考虑上式的标量形式，发现 $\frac{E}{B}=\frac{1}{\sqrt{\varepsilon\mu}}=v$ 是一常数.

*   即 $\vec E$ 和 $\vec B$ 的振动始终保持**相位相同**.

以上结论仅适用于**平面波**.

下面从**辐射**的角度考察更一般的**电磁波**.

大部分物体发光属于原子发光，根据经典电磁理论，其发光的本质是原子内部的电偶极子辐射，即电偶极子振荡产生交变电磁场.这里就出现了一个重要的项，电偶极矩 $\vec p$ ，它决定着辐射的电磁场的大小.沿前述，考虑电偶极子做简谐振荡，则 $\vec p=\vec p_0 e^{-i\omega t}$ （其中 $\vec p_0$ 是振幅矢量其模， $p_0$ 表示振幅大小）.

这种情况下，某点的场为

*   $\vec E=\frac{\omega^2(\vec r\times\vec p_0)\times\vec r}{\rm4\pi\varepsilon\mit v^\rm2\mit r^\rm3}\mit e^{\mit i\rm(\mit kr-\omega t\rm)}.$
*   $\vec B=\frac{\omega^2(\vec r\times\vec p_0)}{\rm4\pi\varepsilon\mit v^\rm3\mit r^\rm2}\mit e^{\mit i\rm(\mit kr-\omega t\rm)}.$

写成标量形式就是

*   $E=\frac{\omega^2p_0\sin\psi}{4\pi\varepsilon v^2r}e^{i(kr-\omega t)}$
*   $B=\frac{\omega^2p_0\sin\psi}{4\pi\varepsilon v^3r}e^{i(kr-\omega t)}$

其中

*   $\vec r$ 是从电偶极子中心到所考察点的矢径.
*   $v$ 是电磁波传播速度.
*   这里的 $\omega$ 是电偶极子振荡的角频率，与电磁波角频率相同.
*   $\psi$ 是偶极矩方向 $\vec p$ 与传播方向 $\vec r$ 的夹角.

综上所述 $\vec E=\frac{v}{r}\vec(B\times\vec r).$ 即 $\color{red}{\vec E,\vec B,\vec r相互垂直}$ ，构成**右手螺旋系**. $\vec E$ 在 $\vec p,\vec r$ 确定的平面内振动，但 $\vec B$ 的振动方向与之垂直，这就是电磁波的**偏振性**.

电磁波的能量也随着电磁波传输，现定义**电磁场的能量密度**w为_空间中单位体积的辐射能_.根据电动力学理论， $w=\frac{1}{2}(\vec E\cdot\vec D+\vec H\cdot\vec B)=\frac{1}{2}\Big(\varepsilon E^2+\frac{1}{\mu} B^2\Big).$

进一步用**坡印廷矢量** $\vec S$ 表示_单位时间通过单位面积的能量_.

根据已有结论知 $\vec S$ 的大小 $S=wv=v\varepsilon E^2=\frac{1}{\mu} EB.$ 注意到各向同性介质中能量传播方向与电磁波传播方向相同（ $\vec S,\vec k$ 方向相同）.那么 $\vec S=\frac{1}{\mu}\vec E\times\vec B=\vec E\times\vec H.$ 即 $\color{red}{\vec E,\vec S,\vec B相互垂直}$ ，构成**右手螺旋系**.

由于 $S$ 的瞬时值无法测定，特此取其一段时间内的平均值 $\langle S\rangle$ 定义为**光强** $I$ .

$\langle S\rangle=\langle EH\rangle=\frac{1}{T}\int_0^TSdt=\frac{\omega^4p_0^2\sin^2\psi}{16\pi^2\varepsilon v^3r^2T}\int_0^T\cos^2(kr-\omega t)dt$ $=\frac{\omega^4p_0^2}{32\pi^2\varepsilon v^3r^2}\sin^2\psi$

对于**平面波** $I=\langle S\rangle=\frac{1}{T}\int_0^TSdt=v\varepsilon A^2\frac{1}{T}\int_0^T\cos^2(kr-\omega t)dt$ $=\frac{1}{2}\varepsilon vA^2=\frac{1}{2}\sqrt{\frac{\varepsilon}{\mu}}A^2.$

*   这意味着 $I$ 与 $A^2$ 成正比.对于同一介质中计算两点的相对强度时，可用 $A^2$ 表示光强.
*   从复振幅的角度来说， $I=|\tilde E|^2=\tilde E\cdot\tilde E^*$ （其中 $\tilde E^*$ 是 $\tilde E$ 的共轭复数）

**3\. 折射与反射（Refraction&Reflection）**
------------------------------------

这里我们主要讨论在**电介质**界面上的折返射以及**金属**界面上的折返射.

3.1 电介质界面
---------

通过麦克斯韦方程组可以知道，在两种介质分界面上没有**传导电流**和**自由电荷**的情况下， $ \vec B$ 和 $\vec D$ 在**界面的法向**方向上连续，而 $\vec E$ 和 $\vec H$ 在**界面的切向**方向上连续.

推导过程这里就不抄书了，但关键是要知道下列关系：

边值关系 $\begin{cases}\vec n\cdot(\vec B_1-\vec B_2)\rm =0\\\vec n\cdot(\vec D_1-\vec D_2)\rm=0\\\vec n\times (\vec E_1-\vec E_2)\rm=0\\\vec n\times(\vec H_1-\vec H_2)\rm=0\end{cases}$ ，即 $\begin{cases}B_{1n}=B_{2n}\\D_{1n}=D_{2n}\\E_{1t}=E_{2t}\\H_{1t}=H_{2t}\end{cases}$

其中，作为下标的 $1$ 和 $2$ 用来区别界面两侧介质， $\vec n$ 是指界面的法线方向（由介质 $2$ 指向介质 $1$ ）.

整体来看，光波入射到两介质分界面时会发生反射和折射，这是电磁波与物质相互作用的结果.对于这部分具体的讨论相当复杂，以至于一般的物理光学书中也不详细介绍这些，但我们可以基于已有的波动方程的解（这里用电磁波的复数形式），对这些现象进行讨论，这里研究**平面波**.

而对于考察具体的光波，先确定如下定义

*   光波的**入射面**指界面法线与入射光线组成的平面.
*   光波的**振动面**指电场矢量方向与入射光线组成的平面.
*   振动面与入射面一般不重合，其夹角用**方位角**\\alpha表示.
*   对于光矢量 $\vec E$ ，其振动方向与入射面内的分量称为光矢量的 $p$ 分量（简称 $p$ 波），记作 $E_p$ 而振动方向与入射面垂直的分量称为 $s$ 分量（简称 $s$ 波），记作 $E_s$ .

  

![](https://pic1.zhimg.com/v2-718462ef4690e46e454a05573ccb5300_b.jpg)  
振动面与入射面

  

再说明一下接下来的讨论所要用到的符号表示，以角度 $\theta$ 为例：

*   $\theta_1$ 表示入射角（入射波矢量 $\vec k_1$ 与界面法线的夹角）；
*   $\theta'_1$ 表示反射角（反射波矢量 $\vec k_1’$ 与界面法线的夹角）；
*   $\theta_2$ 表示折射角（折射波矢量 $\vec k_2$ 与界面法线的夹角）.

其它量的表示也遵循此规矩.若有 $s$ 波与 $p$ 波的区别，也会在下标中体现.

  

由前述的 $\vec n\times (\vec E_1-\vec E_2)=0$ ，知 $\vec n\times(\vec E_1+\vec E_1’)=\vec n\times\vec E_2$ ，将电场表达式改写成复数形式，由对应量相等（要求对任何时刻 $t$ 都成立的前提下）即可发现

*   $\omega_1=\omega’_1=\omega_2$ ，即入射，反射，折射波的**角频率相同**.
*   $\vec k_1\cdot\vec r=\vec k_1’\cdot\vec r=\vec k_2\cdot\vec r$ 即 $\vec k_1,\vec k’_1,\vec k_2$ **共面**，都在入射面内.

对于 $\theta$ 系列，考虑界面是 $z=0$ 的平面，则

$k_1\sin\theta_1=k’_1\sin\theta’_1=k_2\sin\theta_2.$

由 $k=\frac{\omega}{v}$ ，知 $k_1=k’_1=\frac{\omega}{v_1}$ 以及 $k_2=\frac{\omega}{v_2}.$

进而 $\theta_1=\theta’_1$ ，同时有 $\frac{\sin\theta_1}{v_1}=\frac{\sin\theta_2}{v_2}$ 即 $\color{red}{n_1\sin\theta_1=n_2\sin\theta_2}.$ 这就是**折射定律**.

以上的讨论都不涉及振幅矢量 $\vec A$ ，对于它，要分 $s$ 波和 $p$ 波来讨论.

$\large\color{red}{\bf s波}$

由边值关系知 $E_{1s}+E’_{1s}=E_{2s}$ ，即对于 $s$ **波入射波**和**反射波**的电场强度大小**之和**等于**折射波**的电场强度大小.

以及对于 $p$ 波有 $H_{1p}\cos\theta_1-H’_{1p}\cos\theta_1=H_{2p}\cos\theta_2.$

根据前述各矢量关系知 $\vec H=\frac{1}{\mu v}(\vec k_0\times\vec E)$

注意到 $\frac{v_1}{v_2}=\frac{n_2}{n_1}$ ，则上述关于 $\vec H$ 的式可改写称 $\frac{n_1}{\mu_1}(E_{1s}-E’_{1s})\cos\theta_1=\frac{n_2}{\mu_2}E_{2s}\cos\theta_2$

综上，可定义 $s$ 波的**复振幅反射系数** $r_s$ 和**复振幅透射系数** $t_s$

*   $\color{red}{\tilde r_s}=\frac{\tilde E’_{1s}}{\tilde E_{1s}}=\frac{\frac{n_1}{\mu_1}\cos\theta_1-\frac{n_2}{\mu_2}\cos\theta_2}{\frac{n_1}{\mu_1}\cos\theta_1+\frac{n_2}{\mu_2}\cos\theta_2}$ $=\frac{n_1\cos\theta_1-n_2\cos\theta_2}{n_1\cos\theta_1+n_2\cos\theta_2}=\color{red}{-\frac{\sin(\theta_1-\theta_2)}{\sin(\theta_1+\theta_2)}}$
*   $\color{red}{\tilde t_s}=\frac{\tilde E_{2s}}{\tilde E_{1s}}=\frac{2\frac{n_1}{\mu_1}\cos\theta_1}{\frac{n_1}{\mu_1}\cos\theta_1+\frac{n_2}{\mu_2}\cos\theta_2}$ $=\frac{2n_1\cos\theta_1}{n_1\cos\theta_1+n_2\cos\theta_2}=\color{red}{\frac{2\sin\theta_2\cos\theta_1}{\sin(\theta_1+\theta_2)}}$

上两式的后两步是考虑非磁性介质， $\mu_1=\mu_2$ 的情况进行简化.（消掉 $n_1,n_2$ 是根据折射定律，分子分母同时化为 $n_1$ 或 $n_2$ 的形式才消掉的）.

$\large\color{red}{\bf p波}$

同理，考虑到 $E_{1p}\cos\theta_1-E’_{1p}\cos\theta_1=E_{2p}\cos\theta_2$ 以及 $H_{1s}+H’_{1s}=H_{2s}$ 并认为 $\mu_1=\mu_2$ 即可定义 $p$ 波的**复振幅反射系数** $r_p$ 和**复振幅透射系数** $t_p$

*   $\color{red}{\tilde r_p}=\frac{\tilde E’_{1p}}{\tilde E_{1p}}=\frac{n_2\cos\theta_1-n_1\cos\theta_2}{n_2\cos\theta_1+n_1\cos\theta_2}=\color{red}{\frac{\tan(\theta_1-\theta_2)}{\tan(\theta_1+\theta_2)}}$
*   $\color{red}{\tilde t_p}=\frac{\tilde E_{2p}}{\tilde E_{1p}}=\frac{2n_1\cos\theta_1}{n_2\cos\theta_1+n_1\cos\theta_2}=\color{red}{\frac{2\sin\theta_2\cos\theta_1}{\sin(\theta_1+\theta_2)\cos(\theta_1-\theta_2)}}$

  

特别地，对于**垂直入射**（ $\theta_1=0$ ）的情况，上述公式化为

*   $\color{red}{r_s=-\frac{n-1}{n+1}}$
*   $\color{red}{t_s=\frac{2}{n+1}}$
*   $\color{red}{r_p=\frac{n-1}{n+1}}$
*   $\color{red}{t_p=\frac{2}{n+1}}$

其中 $n=\frac{n_2}{n_1}$ 是相对折射率.

上述几组关于**复振幅透射/反射系数**的公式都被称为**菲涅耳公式（Fresnel formulate）**.

> 注：结果出现的**正负**数意味着两**振幅方向**相同或相反.各量的**正方向**如下图所示，其中 $E_{1s}$ 的**点**表示垂直 $xOy$ 面，向屏幕外的方向.（由前述关系，由 $\vec E,\vec k$ 可推知 $\vec H$ 的方向）

  

![](https://pic4.zhimg.com/v2-178ffe61617f4cdd365fda7fa826389b_b.jpg)  
反射光和折射光当中，s波与p波的光矢量正方向

  

上述讨论都是基于**复振幅**的.进一步地，基于**能量**也可以定义一组概念，即**透射比**和**反射比**.

沿用之前光强I的表示.首先考虑以任意角度 $\theta_1$ 入射的情况，即可知

入射波光能 $W_1=I_1\cos\theta_1=\frac{1}{2}\sqrt\frac{\varepsilon_1}{\mu_1}A_1^2\cos\theta_1.$

反射波光能 $W’_1=I’_1\cos\theta_1=\frac{1}{2}\sqrt\frac{\varepsilon_1}{\mu_1}{A'}_1^2\cos\theta_1.$

透射波光能 $W_2=I_2\cos\theta_2=\frac{1}{2}\sqrt\frac{\varepsilon_2}{\mu_2}A_2^2\cos\theta_2.$

那么对于**反射比**（reflectivity） $\rho$ 和**透射比**（transmissivity） $\tau$ 的**一般定义**如下：

$\color{red}{\rho}=\frac{W’_1}{W_1}=\frac{I’_1\cos\theta_1}{I_1\cos\theta_1}=\frac{I’_1}{I_1}=\color{red}{\Big(\frac{A’_1}{A_1}\Big)^2}$

$\color{red}{\tau}=\frac{W_2}{W_1}=\frac{I_2\cos\theta_2}{I_1\cos\theta_1}=\color{red}{\frac{n_2\cos\theta_2}{n_1\cos\theta_1}\Big(\frac{A_2}{A_1}\Big)^2}$

由能量守恒， $\color{red}{\rho+\tau=1}$

如果分别讨论**s波**与**p波**，现定义 $s$ 波的反射比 $\rho_s$ ，透射比 $\tau_s$ ； $p$ 波的反射比 $\rho_p$ ，透射比 $\tau_p$ .

$\rho_s=\Big(\frac{I’_{1s}}{I_{1s}}\Big)^2=r_s^2=\frac{\sin^2(\theta_1-\theta_2)}{\sin^2(\theta_1+\theta_2)}$

$\tau_s=\Big(\frac{I_{2s}}{I_{1s}}\Big)^2\frac{n_2\cos\theta_2}{n_1\cos\theta_1}=t_s^2\frac{n_2\cos\theta_2}{n_1\cos\theta_1}$ $=\frac{n_2\cos\theta_2}{n_1\cos\theta_1}\frac{4\sin^2\theta_2\cos^2\theta_1}{\sin^2(\theta_1+\theta_2)}$

$\rho_p=\Big(\frac{I’_{1p}}{I_{1p}}\Big)^2=r_p^2=\frac{\tan^2(\theta_1-\theta_2)}{\tan^2(\theta_1+\theta_2)}$

$\tau_p=\Big(\frac{I_{2p}}{I_{1p}}\Big)^2\frac{n_2\cos\theta_2}{n_1\cos\theta_1}=t_p^2\frac{n_2\cos\theta_2}{n_1\cos\theta_1}$ $=\frac{n_2\cos\theta_2}{n_1\cos\theta_1}\frac{4\sin^2\theta_2\cos^2\theta_1}{\sin^2(\theta_1+\theta_2)}$

那么同样有 $\rho_s+\tau_s=1$ 以及 $\rho_p+\tau_p=1.$

而对于某个**具体的电磁波**通常要考虑**偏振**方向，设其方位角为 $\alpha$ ，容易计算其反射比 $\rho_\alpha=\rho_s\sin^2\alpha+\rho_p\cos^2\alpha.$

那么对于更常见的**自然光**，就做取平均处理 $\rho_n=\frac{1}{2}(\rho_s+\rho_p).$

特别地，对于**正入射**的**自然光**， $\color{red}{\rho_n=\Big(\frac{n-1}{n+1}\Big)^2}$ （其中 $n=\frac{n_2}{n_1}$ ）.

*   值得注意的是， $n_1$ 与 $n_2$ 越**接近**， $\rho_n$ 就越**低**.

下面讲两个关于**入射角**的特殊角度：

*   由**全偏振**引出的**起偏角**（**布儒斯特角**）（Brewster） $\theta_B$ ；
*   由**全反射**（total reflection）引出的**临界角** $\theta_c$ .（只能发生在光密介质入射到光疏介质中）

这两个角都是观察**反射波**的特性发现的.

  

$\large\color{red}{\theta_B}$

*   先考虑光从 $\color{red}{光疏介质}$ （折射率较小）入射到 $\color{red}{光密介质}$ （折射率较大）的情况，以 $n=\frac{n_2}{n_1}=1.5$ 为例，那么根据菲涅耳公式， $r_s,r_p,t_s,t_p$ 与入射角 $\theta_1$ 的关系如下图所示.

![](https://pic2.zhimg.com/v2-c63bb417499758165180d2b194875715_b.jpg)  
从光疏介质入射到光密介质

不难发现，在这种情况下，

对于**透射系数**，无论 $s$ 波 $p$ 波，均随着**入射角**的增大而**减小**，

而**反射系数**（的绝对值）中， $s$ **波**随着 $\theta_1$ 增大而**增大**，但 $p$ **波**却是先减小**至零**然后**增大**（注意**由正到负**）.

也就是说，对于反射波，会有一个入射角 $\theta_B$ ，使反射波只有 $s$ 波，而没有 $p$ 波，这正是**偏振光**（产生**全偏振**现象）.

这就是**布儒斯特定律**.

因此，我们称这个角度（入射角）为**起偏角**（**布儒斯特角**）.

并注意 $r_p$ 的表达式，可知 $\theta_1+\theta_2=\frac{\pi}{2}$ 时才满足 $r_p=0$ ，这意味着 $\theta_B$ 满足关系 $\theta_B+\theta_2=\frac{\pi}{2}$ .进一步地，将此关系代入折射定律会发现 $\color{red}{\tan\theta_B=n}$ ，这就是**布儒斯特公式**.

  

于此，一个很自然的问题就是探究复振幅反/透射系数中的正负.前面已经交代过，这里的正负，表示两量振动方向的相同或相反.

考虑光从**光疏介质**入射到**光密介质**，观察图可发现，对于折射波而言， $t_s,t_p$ 始终是正数，意味着其振动方向与入射波相同.

而对于反射波，无论 $\theta_1$ 如何，它都是负数，即振动方向相反（即使$r_p$ 在入射角较小时是正的，但振幅反射系数整体是负的），如果具体地考虑其_复振幅_的情况，注意到 $e^{i\pi}=-1$ ，这相当于**反射光**矢量产生 $\pi$ 的相位改变，这个现象叫做 $\color{red}{半波损失}$ .（**仅发生在从光疏介质入射到光密介质中**）

* * *

*   另一方面，若是从 $\color{red}{光密介质}$ 入射到 $\color{red}{光疏介质}$ ，同理以 $n=\frac{n_2}{n_1}=\frac{1}{1.5}$ 为例，又有下图

![](https://pic2.zhimg.com/v2-88b512882bef1f3a5b2569f2e2066079_b.jpg)  
从光密介质入射到光疏介质

这种情况下，除了 $r_p$ ，其余量都随着 $\theta_1$ 的增大而增大，而 $|r_p|$ 与上述情况基本相同，还是先减小**至零**然后**增大**（注意**由负到正**）.

  

另外，注意到 $r_s\ne r_p,t_s\ne t_p$ ，说明**反射**、**折射**波的振动面相较于**入射**波发生**偏转**.若以方位角 $\alpha$ 来描述这个变化，

*   $\tan\alpha_1’=\frac{r_s}{r_p}\tan\alpha_1=-\frac{\cos(\theta_1-\theta_2)}{\cos(\theta_1+\theta_2)}\tan\alpha_1.$
*   $\tan\alpha_2=\frac{t_s}{t_p}\tan\alpha_1=\cos(\theta_1-\theta_2)\tan\alpha_1.$

  

$\large\color{red}{\theta_c}$

由折射定律可知，当光从**光密介质**入射到**光疏介质**，折射角总是大于入射角，随着入射角的增大，当折射角到达 $\theta_2=90°$ 时，发生**全反射**，此时的入射角称为**临界角**，记作 $\theta_c$ .由折射定律知， $\color{red}{\sin\theta_c}=\frac{n_2}{n_1}=\color{red}{n}.$ （要使 $\theta_2=90°$ ）发生全反射时，没有折射光，光能无透射损失.

在全反射时，利用**折射定律**和**菲涅耳公式**，经计算，反射系数为

$r_s=\frac{\cos\theta_1-i\sqrt{\sin^2\theta_1-n^2}}{\cos\theta_1+i\sqrt{\sin^2\theta_1-n^2}}=|r_s|e^{i\delta_s}$

$r_p=\frac{n^2\cos\theta_1-i\sqrt{\sin^2\theta_1-n^2}}{n^2\cos\theta_1+i\sqrt{\sin^2\theta_1-n^2}}=|r_p|e^{i\delta_p}$

其中 $\delta_s$ 和 $\delta_p$ 分别是反射波相对于入射波的相位变化，且经计算得

$\tan\frac{\delta_s}{2}=-\frac{\sqrt{\sin^2\theta_1-n^2}}{\cos\theta_1}$

$\tan\frac{\delta_p}{2}=-\frac{\sqrt{\sin^2\theta_1-n^2}}{n^2\cos\theta_1}$

整体上， $\tan\frac{\delta}{2}=\tan\frac{\delta_s-\delta_p}{2}=\frac{\cos\theta_1\sqrt{\sin^2\theta_1-n^2}}{\sin^2\theta_1}$

  

*   对于全反射还有一个不得不提的东西就是**隐失波**\[**evanescent wave**\]（也译作倏逝波、消逝波）

是指全反射时光波投入第二介质约一个波长的深度，**沿着界面**流过波长量级距离后重新返回第一介质，沿着反射光方向射出.这个沿第二介质表面流动的波就是**隐失波**.

这时，对于入射面为 $xz$ **平面**的**透射波**（其实就是倏逝波）可表示为 $E_2=A_2e^{-k_1z\sqrt{sin^2\theta_1-n^2}}e^{i(k_1x\sin\theta_1-\omega t)}$ ，说明透射波沿 $x$ 方向传播（等相面是 $x$ 轴的垂面），振幅在 $z$ 方向指数衰减（等幅面是 $z$ 轴的垂面）.

*   其波长为 $\lambda_2=\frac{2\pi}{k_1\sin\theta_1}=\frac{\lambda_1}{\sin\theta_1}.$
*   其波速为 $v_2=\frac{v_1}{\sin\theta_1}.$
*   定义其**穿透深度** $z_0$ 为振幅减少到界面处振幅的 $\frac{1}{e}$ 时的深度：$z_0=\frac{\lambda_1}{2\pi\sqrt{\sin^2\theta_1-n^2}}.$

3.2 金属表面
--------

**金属中传播**

对于电介质，电导率 $\sigma=0$ ，而对于金属， $\frac{\sigma}{\omega\varepsilon}\gg 1$ （注意金属导电性能与入射波的角频率有关）那么在金属当中，波动方程就要考虑 $\vec j=\sigma\vec E.$

于是得到 $\nabla^2\vec E-\mu\sigma\frac{\partial E}{\partial t}-\mu\varepsilon\frac{\partial^2E}{\partial t^2}=0$

注意到对单色光波有 $\vec E=\tilde{\vec E}e^{i\omega t}$ 以及 $\frac{\partial}{\partial t}=-i\omega$ .则上式化为

$\nabla^2\vec E+\omega^2\mu\Big(\varepsilon+i\frac{\sigma}{\omega}\Big)\vec E=0.$

（对于电介质的情况，也可以此形式改写为 $\nabla^2\vec E+\omega^2\varepsilon\mu\vec E=0$ ）

  

对于这种情况，根据已经定义的量（详见1.1，1.2），要新定义下列量

*   复介电常数 $\tilde\varepsilon=\varepsilon+i\frac{\sigma}{\omega}=\varepsilon_0\tilde\varepsilon_r.$
*   复相位速度 $\tilde v=\frac{c}{\sqrt{\mu_r\tilde\varepsilon_r}}.$
*   复折射率 $\tilde n=\frac{c}{\tilde v}=\sqrt{\mu_r\tilde\varepsilon_r}=\frac{c}{\omega}\tilde k.$

并且， $\tilde n$ 又可表示为 $\tilde n=n(1+i\kappa)$ （ $\kappa$ 是**衰减系数**，决定光波在金属中传播时振幅的衰减特性）

还有刚提到的波矢量的大小 $\tilde k$ ，在金属当中是复数， $\tilde k=k\tilde n=kn(1+i\kappa).$

  

这时，金属中平面波的复数表示就呼之欲出（沿 $x$ 轴传播）

$\vec E=\vec Ae^{i(\tilde kx-\omega t)}=\vec Ae^{-kn\kappa x}e^{i(knx-\omega t)}$

有所不同的是 $\vec Ae^{-kn\kappa x}$ 表示振幅！这说明了**随着深度增加**，**振幅按指数变化衰减**.那么，同样考虑入射波的振幅下降到界面处振幅的 $\frac{1}{e}$ 时的深度，即**穿透深度** $x_0$ ，则有 $x_0=\frac{\lambda}{2\pi}\frac{1}{n\kappa}.$

对于金属良导体，（ $\varepsilon\leqslant\frac{\sigma}{\omega}$ ）有 $n\kappa\approx\sqrt{\frac{\mu_r\sigma}{2\omega\varepsilon_0}}.$

将其代入就得到 $\color{red}{x_0=\sqrt{\frac{2}{\omega\mu\sigma}}}.$

  

**金属表面的反射**

这时，折射角也要表示成复数形式，即 $\sin\tilde\theta_2=\frac{1}{\tilde n}\sin\theta_1.$

进而，菲涅耳公式改写为

*   $\tilde r_s=-\frac{\sin(\theta_1-\tilde\theta_2)}{\sin(\theta_1+\tilde\theta_2)}=|\tilde r_s|e^{i\delta_s}$
*   $\tilde r_p=-\frac{\tan(\theta_1-\tilde\theta_2)}{\tan(\theta_1+\tilde\theta_2)}=|\tilde r_s|e^{i\delta_p}$

相应的反射比改写为

*   $\rho_s=|\tilde r_s|^2=\frac{(n-\cos\theta_1)^2+n^2\kappa^2}{(n+\cos\theta_1)^2+n^2\kappa^2}$
*   $\rho_p=|\tilde r_p|^2=\frac{\Big(n-\frac{1}{\cos\theta_1}\Big)^2+n^2\kappa^2}{\Big(n+\frac{1}{\cos\theta_1}\Big)^2+n^2\kappa^2}$

特别地，对正入射时有 $\rho=\Big|\frac{\tilde n-1}{\tilde n+1}\Big|^2=\frac{n^2(1+\kappa^2)+1-2n}{n^2(1+\kappa^2)+1+2n}.$

综上可得出一些结论

当 $\sigma=0$ 时 $\kappa\rightarrow 0$ ；而当 $\sigma$ 很大时， $\kappa$ 很大，因而 $\rho$ 很大，这意味着光洁的金属表面几乎把入射光全部反射.即这种性质与导电性相关.

*   在金属内部，自由电子吸收光能转化为焦耳热，表现出非透明的性质.

金属表面的反射情况与波长相关，以及对不同的金属材料，具体情况也不一样.

*   实验表明（对于铜和银），在入射角 $\theta_1=90°$ 时， $\rho_s=\rho_p=1$ （正入射时反射比也很高）；且在入射角从零增大的过程中 $\rho_p$ 会出现最小值，但不是零，意味着**金属表面反射不会发生全偏振**现象.

由菲涅耳公式，如果入射光为线偏振光，反射光一般是椭圆偏振光.（取决于 $n$ 和 $\kappa$ ）（关于偏振，本文后半部分会讲到）

4\. 光的吸收、色散、散射
--------------

介质对光的吸收、色散和散射都是分子尺度上的光与物质的相互作用，并称为**分子光学**（molecular optics）

*   **光的吸收**（absorption）是指光强随传播距离而减少的现象，被吸收的光能转化为介质的热能或内能.应注意，除真空外，没有介质对光波或电磁波是绝对透明的.
*   **光的色散**（dispersion）是指介质中的光速与光波的频率有关.
*   **光的散射**（scattering）是指由于物质中存在的微笑粒子对光束的作用，使光波偏离原来的传播方向而四散开来的现象.

4.1 光的吸收
--------

对于一般光源产生的光强不太强的光，一般认为光与物质的相互作用是**线性**的，适用**朗伯**（Lambert）**定律**，即 $\color{red}{I=I_0e^{-\alpha l}}$

其中

*   $I$ 指透过介质厚度 $x=l$ 处的光强.
*   $I_0$ 指透过介质厚度 $x=0$ 处的光强.
*   $\alpha$ 是介质的吸收系数，与光强无关.

但要注意，若对于**激光**这种强光束，物质对光的吸收是**非线性**的，**不适用**朗伯定律.

  

对于透明溶剂的溶液，一般考虑**溶质对光的吸收**，当**溶液浓度不太大**时，吸收系数 $\alpha=\beta C$ ，即与溶液浓度成正比，此时 $\color{red}{I= I_0e^{-\beta Cl}}$ .这就是**比尔**（Beer）**定律**.

但要注意，当溶液**浓度过大**或**溶剂分子影响**到溶质分子对光的吸收时，比尔定律不适用.

  

另外，大多数物质在可见区的**吸收**有**波长选择性**，不同波长可能相差很大.

大气层对可见光和波长在 $300nm$ 以上的紫外光是透明的，而对红外光的某些波段和波长小于 $300nm$ 的紫外光表现为选择吸收.其中**红外波段**的主要吸收气体是**水蒸气**；波长小于 $300nm$ 的**紫外光**的吸收气体是**臭氧**.

因此光学元件对材料的选择都要考虑其波长选择性，**可见光**波段可选用**玻璃**，**紫外**波段可选用**石英**，**红外**波段可选用**萤石**等晶体材料.

  

还要知道，一般固体和液体会在某一较大波长范围内吸收较强，称这个吸收范围为**吸收带**.这样，根据介质对不同波长区域的吸收情况，把波长范围分为介质的**吸收区**和**透明区**；

而对于稀薄的气体，吸收带很窄，约 $10^{-3}nm$ 量级，这是因为这种情况下，入射波的频率与介质中的原子、分子的固有振动频率一致而引起共振，才强烈吸收，称这种现象为**共振吸收**.

值得一提的就是，大量实验标明，物质**吸收带**位置的**波长**值与其**发射**光谱带的位置**一致**，利用此性质可利用物质的**光谱**分析物质中**元素**成分.

4.2 光的色散
--------

介质的折射率 $n$ 随波长 $\lambda$ 的变化的快慢用介质的色散率 $\nu$ 来描述. $\nu=\frac{dn}{d\lambda}.$ 但这种变化率在物质的吸收区和透明区是非常不同的.

**正常色散**

正常色散发生在物质的**透明区**内，表现为**折射率随光波长增大而减小**.即 $\frac{dn}{d\lambda}<0.$

1836年，柯西（A.L.Cauchy）通过实验总结出经验公式 $\color{red}{n=A+\frac{B}{\lambda^2}+\frac{C}{\lambda^4}.}$ 其中 $A,B,C$ 是与物质有关的常数，叫做柯西常数.

  

**反常色散**

而在物质的**吸收区**内，**折射率随波长的增大而增大**. $\frac{dn}{d\lambda}>0.$

> **实验表明，反常色散与物质的吸收区相对应，正常色散与物质的透明区相对应.**

  

对于色散现象的解释，这里简单提一下经典色散理论

经典色散理论将**洛仑兹的经典电子论**和**麦克斯韦的电磁场理论**相结合，导出**电磁场频率**与**介电常数**的关系，从而得到**光波频率**与**折射率**的关系.

  

具体而言，**经典电子论**认为组成物质的原子由原子核和外层束缚电子以线性弹力所维系，这样原子可看作阻尼振荡的电偶极子，那么它就有本征频率 $\omega_0$ ，即发射或吸收频率为 $\omega_0$ 的电磁波.

另一方面，**经典电磁场理论**认为介质中单色电磁波的波速 $v=\frac{c}{\sqrt\varepsilon}.$ （在 $\mu\approx 1$ 的情况下）即 $n=\sqrt\varepsilon.$ 这些已经在前述内容讲过了.这里的介电常数 $\varepsilon$ 联系着介质的极化强度矢量 $\vec P$ 与电场强度适量 $\vec E$ ： $\vec P(t)=\varepsilon_0\chi\vec E(t)，\varepsilon=1+\chi$ .其中 $\chi$ 是介质的电极化率.

  

*   综上，在外来电磁场作用下，束缚电子做受迫振动.从求解电子受迫振动方程入手，依次导出束缚电子的偶极矩 $p$ ，极化强度矢量 $\vec P$ ，电极化率 $\chi(\omega)$ ，折射率 $n(\omega)$ .这样就得到了介质的色散关系.

4.3 光的散射
--------

光的散射也会使通过物质的**光强减弱**，因此研究光强减弱现象应同时考虑**吸收**和**散射**.

还应注意，**散射**是介质的**不均匀性**导致的，而对于**均匀介质**，**不发生散射**，因为散射的本质是光与物质相互作用的结果，是光波摄入介质中激发介质中电子做受迫振荡从而发出次级电磁波，但均匀介质中，这些次级波相互叠加，最终使光波沿折射和反射定律的方向传播，而其他方向完全干涉相消.但非均匀介质却不能完全抵消，从而造成散射光.

散射的效果要考虑诸多因素，现简单分析一些情况

  

**瑞利散射**（Rayleigh）

这是指**散射粒子**的线度远**小于波长**的情况，微粒的线度在 $\frac{\lambda}{10}$ 以下.这种散射有如下特点：

*   散射光强与入射频率的四次方成正比（与波长四次方成反比），即 $\color{red}{I(\omega)\propto\omega^4\propto\frac{1}{\lambda^4}}.$
*   散射光强随观察方向改变， $\color{red}{I(\theta)=I_0(1+\cos^2\theta)}$ .其中 $I(\theta)$ 是与入射光方向成 $\theta$ 角方向上的散射光强， $I_0$ 是 $\theta=\frac{\pi}{2}$ 方向上的散射光强.
*   散射光具有偏振性，与 $\theta$ 角有关（ $\theta$ 沿用上一条）

  

**自然光**入射**各向同性媒质中：**

*   在**垂直于入射方向**上的散射光是**线偏振光**；
*   在**入射方向**及其**逆方向**上散射光仍是**自然光**；
*   在**其他方向**上散射光是**部分偏振光**，偏振程度与 $\theta$ 有关.

**自然光**入射**各向异性媒质中**，散射光在**与入射光垂直**方向上是**部分偏振光**.

  

**米氏散射**（G.Mie）

当粒子线度大于 $10\lambda$ 时，这种**较大微粒**散射称为**米氏散射**.此时散射**光强几乎与波长无关**.

值得一提的是，**瑞利散射**和**米氏散射**中，**散射**光频率与**入射**光**频率相同**.

> 现在就可以根据这些散射理论解释一些现象：  
> 瑞利散射表明，散射光当中，短波长光的光强较大，那么大气散射太阳光中的蓝光和紫光，就造成了我们观察到的**天空呈蔚蓝色**.  
> 在清晨和傍晚，蓝光和紫光被大气强烈散射掉，在这个角度下，看到的**旭日**和**夕阳**则是**红色**的.  
> 而对于大气中的**云团**、**雾气**，**浪花**呈现**白色**则是由于散射粒子的线度较大，发生了米氏散射.

  

**拉曼散射**（C.V.Raman）

在**纯净**的**液体**和**晶体**内的散射，法线**散射**光中出现与**入射**光**频率不同**的部分.这种散射称为拉曼散射.其根本原因是光的散射过程中，分子的状态发生了改变，入射光与分子交换能量，就导致了散射光频发生变化.

拉曼散射的主要特征有：

*   在与入射光频率 $\omega_0$ 相同的散射蒲县两侧，对称分布着频率为 $\omega_0\pm\omega_1,\omega_0\pm\omega_2,\cdots$ 这些强度较弱的散射谱线.（其中长波一侧的谱线称为**斯托克斯线**，另一侧称为**反斯托克斯线**）
*   频率差 $\omega_1,\omega_2,\cdots$ 与散射物质中的分子固有振动频率一致，与入射光频率无关.

**5\. 光波的叠加**
-------------

*   波的叠加服从**叠加原理**：两个或多个波在相遇点产生的合振动是各个波单独在该点产生振动的矢量和.
*   另外，光的传播是独立的，即两个光波相遇后又分开，每个光波仍保持原有的特性，按原来方向继续前进.

这些性质都源于波动微分方程的线性性.但值得一提的是， 在超强光作用下或在某些非线性介质中，波叠加原理不成立，由此展开的是非线性波动光学.

对于具体的叠加情形，分为一下几个方面来讨论

5.1 两个频率相同，振动方向相同的单色波叠加
-----------------------

设有两个**频率相同**，**振动方向相同**的**单色**光波，分别发自光源 $S_1,S_2$ .他们在空间中的 $P$ 点处相遇， $P$ 到 $S_1,S_2$ 的距离分别为 $r_1,r_2$ .那么两光波在 $P$ 点处产生的振动可分别写做 $E_1=a_1\cos(kr_1-\omega t)，E2=a_2\cos(kr_2\omega t)$ .其中 $a_1,a_2$ 分别是两光波的振幅.

现设 $\alpha_1=kr_1，\alpha_2=kr_2$ ，则 $E=E_1+E_2=a_1\cos(\alpha_1-\omega t)+ a_2\cos(\alpha_2-\omega t).$

利用三角公式可进一步化简为 $\color{blue}{E=A\cos(\alpha-\omega t)}.$

其中 $A^2=a_1^2+a_2^2+2a_1a_2\cos(\alpha_2-\alpha_1)$ 以及 $\tan\alpha=\frac{a_1\sin\alpha_1+a_2\sin\alpha_2}{a_1\cos\alpha_1+a_2\cos\alpha_2}.$

*   说明 $P$ 点的合振动依然是**简谐振动**，振动**频率**与**方向**与两单色光**相同**.

进一步地，若 $a_1=a_2=a$ ，记 $I_0=a^2$ 表示单个光波在 $P$ 点的强度， $\delta=\alpha_2-\alpha_2$ 表示两个光波在 $P$ 点的相位差.那么 $P$ 点处的合振动的光强化为 $\color{red}{A^2=I=4I_0\cos^2\frac{\delta}{2}}.$

**说明点** $P$ **处的光强** $I$ **取决于相位差** $\delta$ **.**

$\color{red}{那么一串有趣的性质就来了}$

*   当 $\delta=2m\pi\ \ \ \ \ (m=0,\pm1,\pm2,\cdots)$ 时，光强有**最大值** $4I_0$ .
*   当 $\delta=(2m+1)\pi\ \ \ \ \ (m=0,\pm1,\pm2,\cdots)$ 时， $I=0$ ，光强有**最小值** $0$ .

若相位差 $\delta$ 介于二者之间，又可写成 $\delta=k(r_2-r_1)=\frac{2\pi}{\lambda_n}(r_2-r_1).$ 其中 $\lambda_n$ 是该单色波在介质中的波长，若其在真空中波长为 $\lambda$ ，又有 $n=\frac{\lambda}{\lambda_n}$ ，那么 $\delta=\frac{2\pi}{\lambda}n(r_2-r_1)$ .

定义 $n(r_2-r_1)$ 为**光程差，**记作 $\Delta$ .

既然上式给出了**相位差** $\delta$ 与**光程差** $\Delta$ 的关系，那么 $\color{red}{反过来说}$

*   当 $\Delta=m\lambda\ \ \ \ \ (m=0,\pm1,\pm2,\cdots)$ 时，光强有**最大值** $4I_0$ .（**光程差**是**波长**的**整数倍**）
*   当 $\Delta=\Big(m+\frac{1}{2}\Big)\lambda\ \ \ \ \ (m=0,\pm1,\pm2,\cdots)$ 时，光强有**最小值** $0$ .（**光程差**是**波长**的**半整数倍**）

  

最后不得不讲一种**特殊**的情况，就是两个频率相同，振动方向相同但**传播方向相反**的单色波.这样叠加而成的播称为**驻波**.

以垂直入射到分界面的单色波与其反射波叠加为例，分界面是 $z=0$ 平面.

$E_1=a\cos(kz+\omega t)，E_2=a\cos(kz-\omega t+\delta)$

那么 $E=E_1+E_2=2a\cos\Big(kz+\frac{\delta}{2}\Big)\cos\Big(\omega t-\frac{\delta}{2}\Big).$

可看做这是随时间的振动，且是频率为 $\omega$ 的简谐振动.其振幅随 $z$ 变化，即 $A=\Big|2a\cos\Big(kz+\frac{\delta}{2}\Big)\Big|$ .这样，振幅极大值、极小值随位置 $z$ 的值而改变，不随时间而变.

现定义振幅最大值的位置为**波腹**，振幅为零的位置为**波节**.

*   那么波腹的位置要满足条件 $kz+\frac{\delta}{2}=n\pi\ \ \ \ \ (n=1,2,3\cdots).$
*   波节的位置要满足条件 $kz+\frac{\delta}{2}=\Big(n-\frac{1}{2}\Big)\pi\ \ \ \ \ (n=1,2,3\cdots).$
*   一个很明显的结论就是**相邻**波节**或**波腹的**距离**为 $\frac{\lambda}{2}$ ，**相邻**波节**和**波腹的**距离**为 $\frac{\lambda}{4}$ .

应注意，若反射比不等于 $1$ ，那么入射波与反射波的振幅不相等.

5.2 两个频率相同，振动方向相垂直的单色波叠加
------------------------

这显然就形成了各种不同偏振态的光.

所谓偏振（polarization），就是指横波的振动矢量对某一方向的偏向性.

现设两光波分别为 $E_x=a_1\cos(kz_1-\omega t)，E_y=a_2\cos(kz_2-\omega t)$ ，这是由沿着 $z$ 轴排布的**两光源** $S_1,S_2$ 发出的，如下图所示.

![](https://pic4.zhimg.com/v2-5147af23deb531a560dd111cbb54663b_b.jpg)  
两振动方向相垂直的光波叠加

那么其合振动为 $\vec E=\vec x_0E_x+\vec y_0E_y=\vec x_0a_1\cos(kz_1-\omega t)+\vec y_0 a_2\cos(kz_2-\omega t).$

综合上式，消去参数 $t$ ，所得的就是和振动矢量末端的轨迹方程：

$\color{red}{\frac{E_x^2}{a_1^2}+\frac{E_y^2}{a_2^2}}=2\frac{E_xE_y}{a_1a_2}\cos(\alpha2-\alpha_1)=\color{red}{\sin^2(\alpha_2-\alpha_1)}.$ 其中 $\alpha_1=kz_1，\alpha_2=kz_2.$

这是个椭圆方程式，其外接矩形的边长分别为 $2a_1$ 和 $2a_2$ .

椭圆长轴与 $x$ 的夹角 $\psi$ 为 $\tan2\psi=\frac{2a_1a_2}{a_1^2-a_2^2}\cos\delta$ .其中 $\color{red}{\delta=\alpha_2-\alpha_1}$ ，是两光波的相位差.

$\color{red}{那么又一串有趣的性质就来了}$

*   当 $\delta=2n\pi\ \ \ (n=0,1,2,\cdots)$ 时，轨迹方程化为 $E_y=\frac{a_2}{a_1}E_x$ ，这是一条经过坐标原点，斜率为 $\frac{a_2}{a_1}$ 的直线，意味着这个合成波是**线偏振光**.
*   当 $\delta=(2n+1)\pi\ \ \ (n=0,1,2,\cdots)$ 时，轨迹方程化为 $E_y=-\frac{a_2}{a_1}E_x$ ，与刚才类似，这也是**线偏振光**.
*   当 $\delta=(2n+1)\frac{\pi}{2}\ \ \ (n=0,1,2,\cdots)$ 时，轨迹方程化为 $\frac{E_x^2}{a_1^2}+\frac{E_y^2}{a_2^2}=1.$ 这是个正椭圆方程（长短轴都在 $x$ 或 $y$ 轴上）.这是**椭圆偏振光**.进一步地，如果 $a_1=a_2=a$ ，那么这就是**圆偏振光**.
*   当 $\delta$ 取其他值时，就是一般的椭圆偏振光，长轴方位由 $\psi$ 决定，这个已经说过了.

另外，椭圆或圆偏振光还有**右旋**和**左旋**之分，用来区别：面对光的传播方向看去，合矢量沿**顺时针方向**旋转（右旋）和**逆时针方向**旋转（左旋）.这一点由相位差 $\delta$ 确定，当 $\color{red}{\sin\delta<0}$ 时为 $\color{red}{右旋}$ ；当 $\color{red}{\sin\delta>0}$ 时为 $\color{red}{左旋}$ .

  

> 最后，对椭圆偏振光再做进一步的介绍  
> 对于一般的椭圆偏振光（延续上述情况），还有一种考察方式就是以该椭圆的长轴和短轴进行重新建立坐标系，以长轴为x轴，短轴为y轴.  
> 在此坐标系下，椭圆偏振光的两个分量表示为 $E_{x’}=A_1\cos(\alpha-\omega t)，E_{y’}=A_2\cos\Big(\alpha-\omega t\pm\frac{\pi}{2}\Big).$  
> 经过计算可得到一个结论，就是 $A_1^2+A_2^2=a_1^2+a_2^2$ ，说明无论在什么坐标系下，两个项垂直的分震动的振幅平方和 $A_1^2+A_2^2$ 是**常数**.  
> 下面再引入两个定义  
> 椭圆度 $\varepsilon$ ， $\tan\varepsilon=\frac{A_2}{A_1}$ .（其中 $|\varepsilon|\leqslant\frac{\pi}{4}$ ）  
> 振幅比角 $\beta$ ， $\tan\beta=\frac{a_2}{a_1}.$ （其中 $0\leqslant\beta\leqslant\frac{\pi}{2}$ ）  
> 那么椭圆偏振光的旋向又有了一个判据， $\varepsilon<0$ 时右旋， $\varepsilon>0$ 时左旋.  
> 综合上式可以求得 $\begin{cases}\sin2\varepsilon=\sin2\beta\sin\delta\\\tan2\psi=\tan2\beta\cos\delta\end{cases}$  
> **引入这些的动机先不解释，后续会用到.**

5.3 两个不同频率的单色波叠加
----------------

对于 $E_1=a\cos(k_1z-\omega_1t)，E_2=a\cos(k_2z-\omega_2t)$ 用叠加原理合成为

$E=E_1+E_2=2a\cos(k_mz-\omega_mt)\cos(\bar kz-\bar\omega t)$

其中 $\bar\omega=\frac{(\omega_1+\omega_2)}{2},\bar k=\frac{(k_1+k_2)}{2}；$ $\omega_m=\frac{(\omega_1-\omega_2)}{2},k_m=\frac{(k_1-k_2)}{2}.$

若令 $\color{red}{A=2a\cos(k_mz-\omega_mt)}$ ，则 $\color{red}{E=A\cos(\bar kz-\bar\omega t)}.$

*   上述诸式说明合成波可看作**频率为 $\bar\omega$** ，而 $\color{red}{振幅随时间变化}$ 的波.

若 $\omega_1\approx\omega_2$ ，则 $\omega_m$ 很小，振幅变化就会很慢.

*   从光强角度考察， $I=A^2=2a^2[1+\cos2(k_mz-\omega_mt)]$ .说明合成波的强度在 $0\sim4a^2$ 之间变化，这种强度随时间变化的现象叫做**拍**.由上式，**拍频**为 $2\omega_m$ .即两单色光波**频率之差**.

  

*   这种叠加有一个很**特殊**的一点就是$\color{red}{振幅随时间变化}$.这意味着我们对速度的定义也要更细致一些：
*   之前我们讨论关于（单个）光波传播时，讨论的速度都是其**等相面的传播速度**，这是**相速度**.但在这里，考虑到振幅随时间变化，那么也要对**等幅面的传播速度**进行定义，这就是**群速度**.

易知合成波的相速度就是 $v=\frac{\bar\omega}{\bar k}.$

而对于群速度， $v_g=\frac{\omega_m}{k_m}=\frac{\Delta\omega}{\Delta k}.$ 当 $\Delta\omega$ 很小时，化为 $v_g=\frac{d\omega}{dk}=\frac{d(kv)}{dk}=v+k\frac{dv}{dk}$

代入 $k=\frac{2\pi}{\lambda}$ 就有 $v_g= v-\lambda\frac{dv}{d\lambda}.$

进而定义群折射率 $n_g=\frac{c}{v_g}=\frac{n}{1+\frac{\lambda}{n}\frac{dn}{d\lambda}}.$

结合之前讲过的色散现象，在色散物质中 $v_g\ne v.$

进一步讲，

*   正常色散时，群速度小于相速度；
*   反常色散时，群速度大于相速度；
*   对于不发生色散的介质， $\frac{dv}{d\lambda}=0$ ，群速度等于相速度.

  

依前述，复杂波的**群速度**可认为是**振幅最大点**的移动速度，而波动所携带的能量与振幅平方成正比，因此**群速度是光能（信号）的传播速度**！实验中测量的光脉冲速度是群速度而不是相速度.

值得一提的是，相速度只能表示频率与振幅不变的正弦波，这种波不仅不存在，且无法传递信号.若要传递信号，必须对振幅或频率进行调制（使其随时间变化）.

在传递信号时，只有真空中或物质正常色散的情况才有意义，这是因为吸收效果弱，即使在远距离传播也不会显著衰减，才好传播信号.
> 作者：Tyalmath
> 链接：undefined