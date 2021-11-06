---
title: Electromagnetic theory of light
math: true
tags: Wave optics
categories: Physics
date: 2021-10-13 14:32
---

***
[toc]
***
# 光与电磁

***
## 基本理论
### § 电磁场理论回顾
* Maxwell归结出了Maxwell方程组，在光学应用中我们通常采用微分形式求解电磁场中某一点的场量
  * Maxwell方程组如下
    * $$\begin{equation}
      \nabla\cdot\vec{D} = \rho     
      \end{equation}$$
    * $$\begin{equation}
      \nabla\cdot\vec{B} = 0     
      \end{equation}$$ 
    * $$\begin{equation}
      \nabla\times\vec{E} = -\frac{\partial \vec{B}}{\partial t}     
      \end{equation}$$   
    * $$\begin{equation}
      \nabla\times\vec{H} = \vec{j} + \frac{\partial \vec{D}}{\partial t}    
      \end{equation}$$
    * $$\begin{equation}
      \nabla\cdot\vec{J} = -\frac{\partial \rho}{\partial t}    
      \end{equation}$$
    * 当然值得说明的是Maxwell方程组只包含$(1)-(4)$，$(5)$不属于方程组范畴，但考虑电磁场中经常使用，作者因此擅作主张将其加入
  * 本构关系   
    在各向同性媒介中有以下关系
    * $$\begin{equation}
      \vec{D} = \varepsilon\vec{E}
      \end{equation}$$
    * $$\begin{equation}
      \vec{B} = \mu\vec{H}
      \end{equation}$$
    * $$\begin{equation}
      \vec{J}v = \sigma\vec{E}
      \end{equation}$$
    * **真空中**  
      * $\varepsilon=\varepsilon_0=8.8542\times 10^{-12}\rm C^2/N\cdot m^2.$
      * $\mu=\mu_0=4\pi\times 10^{-7}\rm N\cdot s^2/C^2.$ 
  * 边界条件
    在两种介质交界处存在下列边界条件
    * 介质面处电位连续，电场强度切向分量相等
    * $$\begin{equation}            
      \vec{E}_{1t}=\vec{E}_{2t}
      \end{equation}$$   
    * 介质分界面处面电荷密度的关系
    * $$\begin{equation}
      \vec{D}_{1n}-\vec{D}_{2n} = \rho_s
      \end{equation}$$
    * 介质面处法通量连续，磁感应强度法向分量相等  
    * $$\begin{equation}
      \vec{B}_{1n} = \vec{B}_{2n}
      \end{equation}$$
    * 介质分界面处面电流密度的关系
    * $$\begin{equation}
      \vec{H}_{1t}-\vec{H}_{2t} = \vec{J_s}
      \end{equation}$$  
    * 介质分界面处不存在面电流  
    * $$\begin{equation}
      \vec{J}_{1n}-\vec{J}_{2n} = -\frac{\partial \rho_s}{\partial t}
      \end{equation}$$ 
  * 电磁场波动方程
    * $$\begin{equation}
      \nabla^2\vec{E}-\mu\varepsilon\frac{\partial^2 \vec{E}}{\partial t^2} = \mu\frac{\partial \vec{J}}{\partial t}+\frac{\nabla\rho}{\varepsilon}
      \end{equation}$$ 
    * $$\begin{equation}
      \nabla^2\vec{H} -\mu\varepsilon\frac{\partial^2 H}{\partial t^2} = -\nabla\times\vec{J}
      \end{equation}$$ 
  * 能量和能流密度方程
    * $$\begin{equation}
      W_e = \frac{1}{2}\varepsilon\vec{E}^2
      \end{equation}$$ 
    * $$\begin{equation}
      W_m = \frac{1}{2}\mu\vec{H}^2
      \end{equation}$$ 
    * $$\begin{equation}
      \vec S =\vec E \times \vec H = \vec E \times\vec B = \sqrt{\frac{\varepsilon}{\mu}}E^2\vec k_0 
      \end{equation}$$ 
  * 时谐电磁波
    * 以一定频率作正弦振荡的波称为时谐电磁波，或称为单色波；
    * 用复数形式表示为
      * $$\begin{equation}
        \vec{E}(x,t)=\vec{E}(x)e^{-i\omega t}
        \end{equation}$$   
      * $$\begin{equation}
        \vec{B}(x,t)=\vec{B}(x)e^{-i\omega t}
        \end{equation}$$    
  * 介质中电磁波传播律  
    * 当介质受到电磁波作用时，其极化率与磁化率不再是常数，原因在于束缚电荷受到电磁波的作用做受迫振动
      * $\chi_e=\chi_e(\omega)$
      * $\chi_M=\chi_M(\omega)$ 
    * 在线性介质中本构方程前两式子成立，此时电容率磁导率是频率的函数
    * 电容率$\varepsilon$与磁导率$\mu$随频率而变化的现象称为**介质的色散**  
    * 色散介质中$D(t)=\varepsilon E(t)$不再成立
  * 亥姆霍兹方程
    * $$\begin{equation}
      \nabla\times\vec E = i\omega\mu\vec{H}
      \end{equation}$$
    * $$\begin{equation}
      \nabla\times\vec H = -i\omega\varepsilon\vec E
      \end{equation}$$
    * $$\begin{equation}
      \nabla\cdot\vec E = \vec 0
      \end{equation}$$
    * $$\begin{equation}
      \nabla\cdot\vec H = \vec 0
      \end{equation}$$
    * **需要指出的是亥姆霍兹方程组中的四个方程只有前两个方程是独立的**  
    * $$\begin{equation}
      \nabla\times(\nabla\times\vec E) = \omega^2\mu\varepsilon\vec E = -\nabla^2\vec E
      \end{equation}$$
    * 根据波矢的定义
      * $$\begin{aligned}
       \vec k = \vec k_0 \frac{2\pi}{\lambda}
      \end{aligned}$$
      * 对上式右侧分式分子分母同时除以周期T可以得到
      $$\begin{aligned}
       \vec k = \vec k_0 \frac{\omega}{v}=\vec k_0\omega\sqrt{\mu\varepsilon}
      \end{aligned}$$  
      * 由此可以得到
        $$\begin{aligned}
         \nabla^2 \vec E + k^2\vec{E} = 0
        \end{aligned}$$ 
    * $$\begin{equation}
      \vec B = \frac{1}{i\omega}\nabla\times E = -\frac{i}{k}\sqrt{\mu\varepsilon}\nabla\times E
      \end{equation}$$ 
    * **亥姆霍兹方程**是**一定频率**下电磁波的基本方程，其解代表电磁波场强在空间中的分布，每一种可能的形式称为一种**波膜** 
  * $\nabla$算子的性质
    * $\nabla \rightarrow i\vec{k}$  
      * $\nabla \cdot \rightarrow i\vec{k}\cdot$
      * $\nabla \times \rightarrow i\vec{k}\times$
    * $\frac{\partial }{\partial t} \rightarrow -i\omega$   
  * 电磁波三矢量的关系
    * $$\begin{aligned}
     \vec E = \vec E_0e^{\vec{k}\cdot\vec r-\omega t}
    \end{aligned}$$
    * $$\begin{aligned}
       \vec B = \vec B_0e^{\vec{k}\cdot\vec r-\omega t}
    \end{aligned}$$  
    * 对两式求散度，容易得到$\vec{k}\cdot\vec{E}=\vec{0}$，$\vec{k}\cdot\vec{B}=\vec{0}$
  * 平面电磁波的等相面及相速度
    * 在某一时刻相位相同的点组成的面，称之为等相面（波阵面）
      * 平面电磁波的等相面为一平面，且垂直于传播方向
      * 相速度：相位移动的速度（等相面的法向速度）
        * $$kx-\omega t=const \Rightarrow V_p=\frac{dx}{dt}=\frac{\omega}{k}$$ 
      * 群速度：波包传递的速度，能量传递的速度   
        * $$v_g=\frac{d\omega}{dt}=\frac{d(kv)}{dt}$$
      * 正常色散时，群速度小于相速度；
        反常色散时，群速度大于相速度；
         对于不发生色散的介质,群速度等于相速度 
* 客串结束，下面进入正片
***
### § 各种波场
* 对于Maxwell方程组，当其满足如下条件时可以大幅简化(好耶)
  * 介质为无限大各向同性介质
  * 电磁场远离辐射源，不存在自由电荷和传导电流，这意味这$\vec{J}=\vec{0}$，$\rho=0$，具体方程的形式不在下面列出
* 当其满足如上条件时，电磁场波动方程可以大幅简化！(规整极了)
 
  * 众所周知光速c的定义为
    * $$\begin{equation}
       c=\frac{1}{\sqrt{\mu_0\varepsilon_0}}
      \end{equation}$$ 
  * 介质中的光速为
    * $$\begin{equation}
       v=\frac{c}{n}=\frac{1}{\sqrt{\mu\varepsilon}}
      \end{equation}$$     
  * $$\begin{equation}
      \nabla^2\vec{E}-\frac{1}{v^2}\frac{\partial^2 \vec{E}}{\partial t^2} = 0
      \end{equation}$$ 
  * $$\begin{equation}
      \nabla^2\vec{H} -\frac{1}{v^2}\frac{\partial^2 \vec{H}}{\partial t^2} = 0
      \end{equation}$$   
* 扯了半天废话，下面进入正题
  * **平面波 (plane waves)**
    * 平面波意味着波阵面是平面，平面波光的传播方向是一致的，不妨假设沿平行于Z轴传播，因此我们可以毫不费力地写出平面波的电磁波动方程组
     * $$\begin{equation} 
       \frac{\partial^2 \vec{E}}{\partial z^2} -\frac{1}{v^2}\frac{\partial^2 \vec{E}}{\partial t^2}=0
       \end{equation}$$  
     * $$\begin{equation}
      \frac{\partial^2 \vec{H}}{\partial z^2} -\frac{1}{v^2}\frac{\partial^2 \vec{H}}{\partial t^2}=0
      \end{equation}$$ 
     * $$\begin{equation}
      \frac{\partial^2 \vec{B}}{\partial z^2} -\frac{1}{v^2}\frac{\partial^2 \vec{B}}{\partial t^2}=0
      \end{equation}$$           
    * 此波动方程的通解为
      *   $\vec E =f\Big(\frac{z}{v}-t\Big)$
      *   $\vec H =f\Big(\frac{z}{v}-t\Big)$
      *   $\vec B =f\Big(\frac{z}{v}-t\Big)$
      * 这是波动方程的**通解**，它们表示以**速度** $v$ 沿 $z$ 轴**正方向**传播的**平面波**.可以进一步写出简谐振动形式的**特解**.
      *   ${\vec E=\vec A\cos\Big[\omega\Big(\frac{z}{v}-t\Big)\Big]}$
      *   ${\vec B=\vec A'\cos\Big[\omega\Big(\frac{z}{v}-t\Big)\Big]}$
    * 众所周知，一般情况下，对于光波场，其磁场强度、磁感应强度矢量对介质的极化作用一般不计，与物质发生相互作用时起主要作用的物理量是电场强度，这也是为什么我们称电矢量为光矢量的原因之一，因此现在及以后的讨论将围绕电场强度矢量展开
    * 平面光波场的电矢量方程的一般形式
      * $$\begin{equation}\vec E = \vec A\cos\Big[\vec{k}\cdot\vec r-\omega t\Big]\end{equation}$$
      * $$\begin{equation}\vec k\cdot\vec r = k\cos\alpha x+k\cos\beta y+k\cos\gamma z\end{equation}$$
      * 式(26)中的坐标是空间中某一点P的位置坐标，三个角度是波矢的方向余弦
    * 平面光波场电矢量的复数表示形式
      为了计算简化，我们引入复数表示形式
      * $$\begin{equation}\vec E =\vec Ae^{i(\vec{k}\cdot\vec r-\omega t)}\end{equation}$$ 
      需要提及的是复数表示展开为一般形式中出现的虚部部分并不会影响研究传播规律，这里只取实部部分即可
  * **球面波(Spherical Waves)**
    * 球面波电矢量方程一般形式
      * $$\begin{equation}E=\frac{A}{r}\cos\Big[\vec k\cdot\vec r-\omega t\Big]\end{equation}$$  
    * 球面波电矢量方程的复数形式
      * $$\begin{equation}E=\frac{A}{r}e^{i(\vec k\cdot \vec r-\omega t)}\end{equation}$$
    * 球面波与平面波不同，谈传播方向并无意义，因此不表示为矢量形式.
    * 球面波的振幅A表示距离波源单位长度处的振幅大小     
  * **柱面波(Cylindrical Waves)** 
    * 柱面波电矢量方程一般形式
      * $$\begin{equation}E=\frac{A}{\sqrt{r}}\cos\Big[\vec k\cdot\vec r-\omega t\Big]\end{equation}$$  
    * 柱面波电矢量方程的复数形式
      * $$\begin{equation}E=\frac{A}{\sqrt{r}}e^{i(\vec k\cdot \vec r-\omega t)}\end{equation}$$




***
## 电磁波的反射与折射
### § 反射折射基本规律
      1. 反射与折射波的频率与入射波相等
      2. 入射线、反射线与折射线在同一平面内
      3. 入射角等于反射角
      4. 折射满足折射定律
      5. 入射波、反射波、折射波的振幅满足菲涅尔公式
### § 绝缘介质界面边界条件
* 绝缘介质面上不存在自由电荷与传导电流密度，根据上述边界方程可知
  * 电场强度切向连续 
  * $$\begin{equation}\vec n\times(\vec E_2-E_1)=0\end{equation}$$
  * 磁场强度切向连续
  * $$\begin{equation}\vec n\times(\vec H_2-H_1)=0\end{equation}$$
  * 电位移矢量法向连续
  * $$\begin{equation}\vec n\cdot(\vec D_2-D_1)=0\end{equation}$$
  * 磁感应强度矢量法向连续
  * $$\begin{equation}\vec n\cdot(\vec B_2-B_1)=0\end{equation}$$
  
### § 反射与折射波
* 考虑两种介质分界面为无限大平面，一束电磁波入射于界面
  * $$\begin{aligned}
   \vec E = \vec E_0e^{\vec k \cdot \vec r -\omega t}
  \end{aligned}$$ 
* 在边界处激发新的波，在介质1中传播的称为反射波，在介质2中传播的称为折射波 
  * $$\begin{aligned}
   \vec E' = \vec E'_0e^{\vec k' \cdot \vec r -\omega t}
  \end{aligned}$$ 
  * $$\begin{aligned}
   \vec E'' = \vec E''_0e^{\vec k'' \cdot \vec r -\omega t}
  \end{aligned}$$   
* **注意在介质1中的总场强E是入射波与反射波的叠加，而介质2的场强即为折射波场强**  
### § 反射与折射定律
* 在分界面z=0上的任意时刻任意位置处均满足边界条件
  * $$\begin{aligned}
   \vec n\times(\vec E + \vec E' -\vec E'') = 0
  \end{aligned}$$ 
  * $k_x=k'_x=k''_x,k_y=k'_y=k''_y$
* 不失一般性，选择$k_y$=0，入射光，反射光与折射光在同一平面y=0内
  * $k\sin\theta=k'\sin\theta=k''\sin\theta''$
  * $k=k'=\frac{\omega}{v_1},k''=\frac{\omega}{v_2}$ 
  * $\frac{n_2}{n_1}=\frac{\sin\theta}{\sin\theta''}=\frac{\sqrt{\mu_2\varepsilon_2}}{\sqrt{\mu_1\varepsilon_1}}$
### § 两种独立的偏振波
      1. 平面电磁波反射、折射的振幅关系与偏振有关；
      2. 斜入射的平面电磁波有两种偏振方式：s偏振与p偏振；
      3. s偏振：E垂直于入射面，电场没有垂直于分界面的分量；
      4. p偏振：E平行于入射面，存在垂直于分界面的电场分量；
      5. 若入射波是s偏振，则反射、折射波也是s偏振； 
      6. 若入射波是p偏振，则反射、折射波也是p偏振；
      7. 这里的入射面指的是由入射光线和法线决定的平面，入射面与界面正交；
      8. 取法线为z轴，界面为x轴建立坐标系，我们规定s分量的正方向为y轴正方向
* $\vec p\times\vec s=\vec k$
### § s偏振振幅关系菲涅尔公式
* 对于s偏振($\theta=\theta'$，入射反射角，$\theta''$折射角)：
  * 根据电场、磁场强度切向连续
  * $\vec E + \vec E' = \vec E''$
  * $\vec H\cos\theta-\vec H'\cos\theta' = \vec H''\cos\theta''$
* 利用$\vec{H} =\sqrt{\frac{\varepsilon}{\mu}}\vec E$，取$\mu=\mu_0$，$\frac{\sin\theta}{\sin\theta''}=\sqrt{\frac{\varepsilon_2}{\varepsilon_1}}$
  * $$\begin{equation}\frac{E'}{E}=\frac{\sin(\theta''-\theta)}{\sin(\theta+\theta'')}\end{equation}$$
  * $$\begin{equation}\frac{E''}{E}=\frac{2\cos\theta\sin\theta''}{\sin(\theta+\theta'')}\end{equation}$$
### § p偏振振幅关系菲涅尔公式
* 对于p偏振
  * 根据电场、磁场强度切向连续 
  * $\vec{H}+\vec{H'}=\vec{H''}$
  * $\vec E\cos\theta-\vec E'\cos\theta' = \vec E''\cos\theta''$
* 利用$\vec{H} =\sqrt{\frac{\varepsilon}{\mu}}\vec E$，取$\mu=\mu_0$，$\frac{\sin\theta}{\sin\theta''}=\sqrt{\frac{\varepsilon_2}{\varepsilon_1}}$
  * $$\begin{equation}\frac{E'}{E}=\frac{\tan(\theta''-\theta)}{\tan(\theta+\theta'')}\end{equation}$$
  * $$\begin{equation}\frac{E''}{E}=\frac{2\cos\theta\sin\theta''}{\sin(\theta+\theta'')\cos(\theta-\theta'')}\end{equation}$$  
### § 布儒斯特(Brewster)定律与半波损失
* **布儒斯特定律**
  * 当$\theta+\theta''=\frac{\pi}{2}$，p偏振分量没有反射波，反射波完全变成s偏振光，此时的入射角称为**布儒斯特角**
* **半波损失**
  * 当$\varepsilon_2>\varepsilon_1$，$\sin\theta_1>\sin\theta_2$，对s偏振，$\frac{E'}{E}<0$，此时反射波与入射波电场反向，称为**半波损失**  
### § 全反射
* 当$\varepsilon_1>\varepsilon_2$，入射角$\sin\theta\geq\frac{n_2}{n_1}$会发生全反射
* 此时波矢$\vec k$含有虚部，波矢$\vec k$的虚部部分表征波透入的深度，透入深度与波长相仿，含有虚波矢$\vec k$的平面波仍然是亥姆霍兹方程的解
  * $$\begin{aligned}
   k''^2_x + k''^2_y+k''^2_z=k''^2 \\
   k''_x =k_x=k\sin\theta=k\frac{n_2}{n_1} \\
   k''_z =i\kappa \\
   \kappa=k\sqrt{\sin^2\theta-n^2_{21}} \\
   \vec E''=\vec E''_0E^{-\Kappa z}e^{i(k''_x x-\omega t)}
  \end{aligned}$$
 * 在s偏振中电磁能量全部被反射出去，在半周内，电磁能量透入第二介质，在界面附近薄层内储存起来，在另一半周内，该能量释放出来变为反射波能量。
 
