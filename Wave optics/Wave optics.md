---
title: Wave optics
math: true
tags: Wave optics
categories: Physics
---

***
[toc]
***
# 光波场
***
* 光是交变电磁场
* 光具有时间和空间两重周期性
* 定态光波的概念
  * 满足如下条件的波场为定态波场
    1. 波场空间中各点的扰动是同频率的简谐振动
    2. 波场中各点扰动的振幅只与空间位置有关而与时间无关
* 光是矢量波
  * 光波的传播方向可以用一个矢量表示，称为**波矢**
    $$\begin{aligned}
    \vec{k} = \frac{2\pi}{\lambda}\vec{s}
    \end{aligned}$$
    $\vec{s}$是传播方向上的单位矢量
  * 在真空和各向同性均匀介质中，电场矢量$\vec{E}$、磁感应矢量$\vec{B}$、波矢$\vec{k}$是两两正交的，且场矢量$\vec{E}$、磁感应矢量$\vec{B}$是同相位的.
  * 平面波和球面波的矢量表达式分别如下
    $$
    \left\{\begin{aligned}
    \vec{E}(\vec{r},t) = E_0(\vec{r})\cos (\vec{k}\cdot\vec{r} - \omega t + \varphi_0) 
    &\\
    \vec{B}(\vec{r},t) = B_0(\vec{r})\cos (\vec{k}\cdot\vec{r} - \omega t + \varphi_1)
    \end{aligned}
    \right.
    $$
    $$
    \left\{\begin{aligned}
    \vec{E}(\vec{r},t) = \frac{E_0}{\vec{r}}(\vec{r})\cos (\vec{k}\cdot\vec{r} - \omega t + \varphi_0) 
    &\\
    \vec{B}(\vec{r},t) = \frac{B_0}{\vec{r}}(\vec{r})\cos (\vec{k}\cdot\vec{r} - \omega t + \varphi_1)
    \end{aligned}
    \right.
    $$
* 光强
  * 电磁场具有能量，而且传输能量，电磁场的能量可以用**能流密度**描述
  * 能流密度：
    * 能流密度是指单位时间内通过垂直于传播方向单位面积的能量，能流密度是一个矢量，其方向表示电磁场能量传输的方向.这个矢量被称为**坡印廷矢量**
      $$\begin{aligned}
        \vec{S} = \vec{E}\times\vec{H}
      \end{aligned}$$
    * 根据能流密度与能量密度的关系(根据两者定义脑补模型即可，此处不再配图详尽推导)
      $$\begin{aligned}
       \vec{S} = w\vec{v} = \frac{\vec{v}}{2}(\epsilon E^2 + \mu H^2)
      \end{aligned}$$  
    * 由于光的频率很高而现有探测器的反应时间远比光的传播周期长，因此探测到的能流密度实际上都是在一段时间内的平均值.**光的强度是光波场平均能流密度的绝对值，也就是平均坡印廷矢量的绝对值**.
      $$\begin{aligned}
       I  = <\lvert \vec{S} \rvert> = <\lvert \vec{E}\times\vec{H} \rvert>
      \end{aligned}$$
    在各向同性的无源介质中，对上式计算可以得到
      $$\begin{aligned}
       I =  <\lvert \vec{E}\times\vec{H} \rvert>
       \\ =  <\lvert \vec{E}\times\frac{\vec{B}}{\mu} \rvert>
       \\ =  <\lvert \vec{E}\times\frac{\vec{k}}{\omega}\times\vec{E} \rvert>
       \\ = \frac{1}{T}\int_0^T \frac{k}{\omega \mu}E^2\mathrm{d}t
       \\ = \frac{E^2_0}{2}\sqrt{\frac{\epsilon}{\mu}}
       \\ =  \frac{nE^2_0}{2c\mu}
      \end{aligned}$$
    在不考虑量纲的情况下
    $$\begin{aligned}
     I \propto nE_0^2 \propto E_0^2
    \end{aligned}$$
    * 光的电场强度也称为光矢量
***
# 定态波场的数学描述
***
## 平面波
* 平面波具有以下特征
  1. 振幅是常数
  2. 空间相位是直角坐标的线性函数
     $$\begin{aligned}\varphi(\vec{P}) = \varphi_0 + \vec{k}\cdot\vec{r} = k_1x + k_2y + k_3z + \varphi_0\end{aligned}$$
  3. 波的余弦表达式为
     $$\begin{aligned}
      E(\vec{r},t) = E_0(\vec{r})\cos(\vec{k}\cdot\vec{r} - \omega t + \varphi_0)
     \end{aligned}$$
     由于$\vec{k}\cdot\vec{r}$ = const,从数学上解释可以发现该式表示一系列与波矢垂直的平面.
## 球面波
* 球面波具有以下特征
  1. 场点P处的振幅为
     $$\begin{aligned}
       A(\vec{P}) = \frac{a}{r}
     \end{aligned}$$
     某点出的振幅与到波源的距离成反比，振幅随位矢范数增大而衰减.
  2. 空间相位是球面对称的
     $$\begin{aligned}
      \varphi(\vec{P}) = kr + \varphi_0 = const
     \end{aligned}$$   
  3. 球面波方程
     $$\begin{aligned}
      E(\vec{r},t) = \frac{a}{\vec{\lvert r \rvert}}\cos(\vec{k}\cdot\vec{r} - \omega t + \varphi_0)
     \end{aligned}$$     
## 柱面波
* 柱面波具有以下特征
  1. 振幅表征
     $$\begin{aligned}
      A(\vec{P}) = \frac{a}{\sqrt{r}} \quad (r为圆柱面的半径)
     \end{aligned}$$
  2. 空间相位
     $$\begin{aligned}
      \varphi(\vec{P}) = kr + \varphi_0
     \end{aligned}$$
  3. 振动表达式
     $$\begin{aligned}
      E(\vec{r},t) = \frac{a}{\sqrt{\vec{\lvert r \rvert}}}\cos(\vec{k}\cdot\vec{r} - \omega t + \varphi_0)
     \end{aligned}$$       
***
# 傍轴条件与远场条件
***
## 傍轴近似
* 设想一发光点在坐标轴原点，接受屏垂直于Z轴且与物体所在的垂直距离为z，接受屏上存在一点P，与接受屏对与Z轴交点的距离为r，此时球面波的振幅为
  $$\begin{aligned}
   A(\vec{P}) = \frac{a}{\sqrt{z^2 + r^2}}
  \end{aligned}$$
  幂展开可以得到
  $$\begin{aligned}
   A(\vec{P}) = \frac{a}{z(1 + \frac{1}{2}(\frac{r}{z})^2 + ...)}
  \end{aligned}$$
  如果满足r << z，则高次展开可以忽略，因此
  $$\begin{aligned}
   A(\vec{P}) = \frac{a}{z}
  \end{aligned}$$
  满足r << z称为傍轴条件
## 远场近似      
* 在上面的模型中，球面波在接受屏幕上的相位为
  $$\begin{aligned}
   \varphi(\vec{P}) = k\sqrt{z^2 + r^2} 
   \\= kz(1 + \frac{1}{2}(\frac{r}{z})^2 + ...) 
   \\= k(z + \frac{1}{2}\frac{r^2}{z} + ...) 
  \end{aligned}$$
  如果满足
  $$\begin{aligned}
   z >> \frac{r^2}{\lambda}
  \end{aligned}$$
  则高次项可以忽略，因此
  $$\begin{aligned}
   \varphi(\vec{P}) = kz
  \end{aligned}$$
  上述条件称为远场条件，**满足远场条件必然满足傍轴条件**
***
# 光的叠加原理
***
* 成立条件
  **介质为线性介质且振动不是十分强烈**，振动很强烈时线性介质会变成非线性介质
* 叠加的具体过程已经在前面的机械波中有过推导，这里不再赘述.仅仅给出相关结论
  1. 不同频率的光是不相干的
  2. 频率相近的单色光叠加形成光学拍
  3. 不同频率的定态光波叠加得到非定态光
  4. 振动方向垂直的光非相干且总光强为两光强之和
* 根据省略的推导分析我们得出相干光产生的条件
  1. 相位差恒定
  2. 存在互相平行的振动分量
  3. 频率相同
***
# 光的偏振性
***
* 光波是电磁波，其电场强度、磁感应强度和波矢互相垂直，因此光波是横波.因可见光波段的电磁波不会引起大多数介质的磁化，因此只考虑其光矢量(即电矢量)
* 横波的振动方向与传播方向垂直，往往会表现出偏振特性.偏振，是**振动方向相对于传播方向的不对称性**，其表现为虽然在各个方向上存在振动但是不同方向上的振幅不同或者电矢量只在一个平面内有振动.
## 马吕斯定理
* 马吕斯定律指出，光线束在各向同性的均匀介质中传播时，始终保持着与波面的正交性，并且入射波面与出射波面对应点之间的光程均为定值
* 马吕斯定理指出通过偏振片后光强关系满足
  $$\begin{aligned}
   I = I_0 \cos^2 \alpha
  \end{aligned}$$
  $\alpha$是入射线偏振光的光振动方向和偏振片偏振化方向之间的夹角
  应当指出的是，**自然光通过起偏器后的光强变为原来的一半**，下面简要证明
  $$\begin{aligned}
   I = \int_0^{2\pi} (E_0\cos\theta)^2\mathrm{d}\theta 
   \\ = \frac{1}{2}E^2_0 = \frac{1}{2}I_0 
  \end{aligned}$$
## 偏振光的分类
1. **平面偏振光**(线偏振光)
   * 自然光经过起偏器后，由于只有平行于起偏器偏振化方向的电矢量才能通过，因此透射光只包含单一振动方向的电矢量，这种矢量始终在同一个平面内振动，投影上看来，电矢量只是一条直线，这样的光就是线偏振光(平面偏振光)
   * 任何一个平面偏振光，都可以分解为两个振动面互相正交的平面偏振光
   * 我们用**消光比**来描述偏振仪器的起偏效果，消光比表示为
     $$\begin{aligned}
      消光比 = \frac{最小透射光强}{最大透射光强} = \frac{I_{min}}{I_{max}}
     \end{aligned}$$
2. 圆偏振光
   * 在一个与光传播方向(波矢方向)垂直的平面内观察其电矢量，如果光的电矢量不是在一个固定的平面内振动，而是绕着传播方向匀速旋转，并且旋转过程中电矢量的大小不发生改变，这就是圆偏振光.
   * 根据光的叠加原理可知，圆偏振光可以分解为两个相互正交的平面偏振光，且这两个平面偏振光存在$\frac{\pi}{2}$的相位差.
   * 迎着光的传播方向观察，如果光矢量(电矢量)是顺时针旋转的，则称为**右旋圆偏振光**；如果电矢量是逆时针旋转的，则称为**左旋圆偏振光**
   * 同一个空间位置的圆偏振光可以表示为
     $$
     \begin{equation}
     \left\{\begin{aligned}
       E_x(z,t) = A\cos(\omega t)
       &\\
       E_y(z,t) = A\cos(\omega t ± \frac{\pi}{2})
     \end{aligned}
     \right.   
     \end{equation} 
     $$
3. 椭圆偏振光
   * 与圆偏振光的定义类似，但是矢量端点的轨迹不再是圆，而是椭圆.
   * 同样地，椭圆偏振光的电矢量也可以进行正交分解(同一位置省去了空间相位)
     $$
     \begin{equation}
     \left\{\begin{aligned}
       E_x(z,t) = A\cos(\omega t)
       &\\
       E_y(z,t) = A\cos(\omega t ± \Delta \varphi)
     \end{aligned}
     \right.   
     \end{equation} 
     $$ 
     下面到了小把戏时刻
     $$
     \begin{equation}
     \left\{\begin{aligned}
      \frac{E_x}{A_x} = \cos \omega t
     &\\
      \frac{1}{\sin \Delta \varphi}(\frac{E_y}{A_y}-\cos\omega t\cos\Delta\varphi) = \sin\omega t
     \end{aligned}
     \right.   
     \end{equation} 
     $$ 
     再进行一次小把戏就可以得到
     $$\begin{aligned}
      \frac{E^2_x}{A^2_x} + \frac{E^2_y}{A^2_y} - \frac{2E_x E_y}{A_x A_y}\cos\Delta\varphi = \sin^2\Delta\varphi
     \end{aligned}$$
     经过两次小把戏我们就得到了一个xoy平面内的椭圆方程！不过显然这个椭圆方程并不是标准方程，而是出现了偏心.椭圆的长轴或短轴对坐标轴的夹角满足
     $$\begin{aligned}
      \tan 2\alpha = \frac{2A_x A_y}{A^2_x-A^2_y}\cos\Delta\varphi
     \end{aligned}$$
4. 部分偏振光
   * 部分偏振光是相对于传播方向就不呈轴对称性而是有一个优越的振动方向.即这种偏振光的电矢量在不同的方向上有不同的大小，其中有两个相互垂直的方向上电矢量的振幅分别为最大和最小.自然光经过反射或折射一般变成部分偏振光，自然光经过散射一般也会变成部分偏振光.
   * 我们定义部分偏振光的**偏振度P**为
     $$\begin{aligned}
      P = \frac{I_{max} - I_{min}}{I_{max} + I_{min}}
     \end{aligned}$$
     应当指出的是自然光的偏振度为零，而平面偏振光的偏振度为1.
5. 总结综述
   * 从上面的讨论我们可以看出，平面偏振光、圆偏振光、椭圆偏振光的光矢量(电矢量)都可以看作是两个正交的分量叠加，分量的一般表达形式为：
     $$\begin{cases}
     E_x = A_x\cos(\omega t)
     \\
     E_y =A_y\cos(\omega t + \Delta \varphi)
     \end{cases}$$
   * 当$\Delta \varphi$ = 0 或 $\pi$ 时上述方程演变为平面偏振光的方程
   * 当$\Delta \varphi$ = $±\frac{\pi}{2}$ 且 $A_x = A_y$时，方程演变为圆偏振光
   * 其余情况下的方程均是椭圆偏振光方程，由此，椭圆偏振光是更一般的偏振态
***
# 光与物质的相互作用
***
## 光的吸收
* 线性吸收的实验定律
   * 实验表明在光强不是很大的情况下，在透明介质中，被吸收的光强与吸收体的厚度成正比.在各向同性的均匀介质中取一薄层，厚度为$\mathrm{d}x$，光射入薄层前的光强为I，从薄层射出后，强度为I + $\mathrm{d}I$, 则有
   $$\begin{aligned} \mathrm{d}I = -\alpha I \mathrm{d}x \end{aligned}$$
   解该常微分方程得
   $$\begin{aligned}
     I = I_0e^{-\alpha x}
   \end{aligned}$$
   系数$\alpha$是与介质有关得常数，称为吸收系数.上述实验定律称为**布格尔定律**或者**朗伯定律**
   在溶液中，上述定律依然成立，但是吸收系数与溶液的浓度成正比
   $$\begin{aligned}
     \alpha = AC
   \end{aligned}$$
   C为溶液的浓度，A是与溶液有关的常数，这一定律称为**比尔定律**
* 吸收系数$\alpha$与波长的关系
   * 实验表明同一种介质对不同的波长往往有不同程度的吸收.波长与吸收系数的关系大致有两类
     * 普遍吸收：吸收系数与波长无关，吸收后所有成分的光强都有相同的改变.值得注意的是对所有波段都普遍吸收的介质是不存在的
     * 选择吸收：吸收系数与波长有关，介质强烈吸收某些波长成分的光.这是由于介质中的原子能极差正好与入射光中某些波长的能量对应，因而强烈吸收这些成分.这种吸收也称为**共振吸收**，与吸收波长对应的光谱线称为共振线.
## 光的色散
* 色散规律
   * 实验表明，折射率随波长的增大而减小，而且在波长小的地方减小得快.根据实验数据可以得到**正常色散的柯西公式**
     $$\begin{aligned}
       n = A + \frac{B}{\lambda^2} + \frac{C}{\lambda^4}
     \end{aligned}$$ 
     **需要强调的是柯西公式是一个经验公式** 
## 光的散射
* 散射现象
  入射光与介质中的带电粒子相互作用，带电粒子在入射光的激发下做受迫振动，发出电磁波.这是有真实扰动源的光波，也称为次波.如果介质是均匀的，所发出的电磁波经过叠加后总有确定的方向，因此除了沿着入射光原来的方向有光继续传播之外其余方向均无光;而如果介质是不均匀的，则介质中发出的次波在其他方向上不能完全抵消，因此可以向任意方向传播，这就形成散射.**光在密度不均匀的介质中总能产生散射**
* 散射定律
   * 瑞利散射
     * 散射体尺寸小于入射波长
     * 散射光强与入射光波长的四次方成反比$I \propto \lambda^{-4}$
   * 德拜散射
     * 散射体尺寸大于光波波长
     * 散射光强对光波长依赖性不强，各个波长的散射光强差别不大
***
# 光的干涉
***
* 杨氏双缝干涉
   ![杨氏双缝干涉实验](\pic/杨氏双缝.jpg)
   根据光的叠加原理，干涉光在某一点的光强为
   $$\begin{aligned}
     I = A^2_1 + A^2_2 + 2A_1A_2\cos(\Delta \varphi) 
   \end{aligned}$$
   相位差$\Delta \varphi$ = $\Delta \varphi_0 + \frac{\Delta L}{\lambda}2\pi$，$\Delta L$是两光源对同一点的光程差，右式前项为两光源的初相位差.在杨氏双缝干涉实验中的两个光源是在同一个波阵面上，因此初相位为零.
   第一个光源到某点的距离为:
   $$\begin{aligned}
    r^2_1 = D^2 + (x-\frac{d}{2})^2 + y^2 
   \end{aligned}$$
   第二个光源到某点的距离为:
   $$\begin{aligned}
    r^2_2 = D^2 + (x+\frac{d}{2})^2 + y^2 
   \end{aligned}$$
   考虑傍轴条件和远场条件近似得到
   $$\begin{aligned}
    r_1 = D + \frac{(x-\frac{d}{2})^2 + y^2}{2D}
   \end{aligned}$$
  $$\begin{aligned}
    r_2 = D + \frac{(x+\frac{d}{2})^2 + y^2}{2D}
   \end{aligned}$$
   光程差为
   $$\begin{aligned}
    \Delta L = \frac{dx}{D}
   \end{aligned}$$
   因此亮条纹条件是
   $$\begin{aligned}
    \frac{dx}{D} = k\lambda ,k = 0,±1,±2...
   \end{aligned}$$
   暗纹条件是
    $$\begin{aligned}
    \frac{dx}{D} = (2k+1)\frac{\lambda}{2} ,k = 0,±1,±2...
   \end{aligned}$$
* 干涉条纹的可见度(反衬度)
  前面我们在偏振中定义了消光比，可见度(反衬度)在表达式上与之相同，可见度$\gamma$定义为
  $$\begin{aligned}
   \gamma = \frac{I_{max} - I_{min}}{I_{max} + I_{min}} = \frac{2A_1A_2}{A^2_1 + A^2_2}
  \end{aligned}$$
* 两列平行光的干涉
  前面的杨氏双缝干涉是同一个波阵面上的波源发出的相干光干涉叠加，其振幅和初相位均相同，这里我们讨论更为一般的情况.
  设两列同频率的单色光的振幅分别为$A_1$,$A_2$;初相位分别为$\varphi_1$,$\varphi_2$，两列波的波矢方向分别为($\alpha_i$,$\beta_i$,$\gamma_i$)，两列光在XOY平面上某一点的相位差为
  $$\begin{aligned}
   \Delta \varphi(x,y) = \vec{k}\cdot(\vec{r_1} - \vec{r_2}) + \varphi_1 - \varphi_2
   \\=k(\cos\alpha_1-\cos\alpha_2)x+k(\cos\beta_1 - \cos\beta_2)y + \varphi_1 - \varphi_2
  \end{aligned}$$ 
  在该点的光强为
  $$\begin{aligned}
   I(x,y) = A^2_1+A^2_2+2A_1A_2\cos(\Delta \varphi)
  \end{aligned}$$
  前面我们定义了干涉条纹的反衬度(可见度)$\gamma$，因此上式也可以写为
  $$\begin{aligned}
   I(x,y) = (A^2_1+A^2_2)(1 + \gamma \cos(\Delta \varphi))
  \end{aligned}$$
  由相位差确定的亮暗干涉条纹的条件为
   $$\begin{aligned}
    k(\cos\alpha_1-\cos\alpha_2)x+k(\cos\beta_1 - \cos\beta_2)y + \varphi_1 - \varphi_2 =
    \begin{cases}
      2k\pi
      \\(2k+1)\pi
    \end{cases}
  \end{aligned}$$ 
  上式方程显然是直线方程，因此亮暗条纹都是等间隔的平行直线，条纹间隔为
  $$\begin{aligned}
   \begin{cases}
   \Delta x = \frac{2\pi}{k(\cos\alpha_1 - \cos\alpha_2)} = \frac{\lambda}{\cos\alpha_1 - \cos\alpha_2}
   \\
   \Delta y =  \frac{2\pi}{k(\cos\beta_1 - \cos\beta_2)} = \frac{\lambda}{\cos\beta_1 - \cos\beta_2}
   \end{cases}
  \end{aligned}$$