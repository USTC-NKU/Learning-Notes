# Thermodynamic properties of homogeneous matter 均匀物质的热力学性质
---
**$$\begin{aligned}Organized\quad in\quad NKU \end{aligned}$$**
***
[toc]
---
## §2.1 内能、焓、自由能、吉布斯函数的全微分
* 根据物态方程、内能和熵，我们导出了热力学基本方程：
  $$\begin{aligned}
   \mathrm{dU} = T\mathrm{dS} - p\mathrm{dV}\tag{2.1.1}
  \end{aligned}$$
  热力学基本方程给出了两个平衡态的内能、熵和体积之间的微分关系，可以把热力学基本方程看作是U对S、V的全微分表达式，U是对S、V的函数，其全微分是：
  $$\begin{aligned}
   \mathrm{dU}=(\frac{\partial U}{\partial S})_V\mathrm{dS} + (\frac{\partial U}{\partial V})_S\mathrm{dV} \tag{2.1.2}
  \end{aligned}$$
  其中：
  $$\begin{aligned}
   (\frac{\partial U}{\partial S})_V = T,(\frac{\partial U}{\partial V})_S = -p \tag{2.1.3}
  \end{aligned}$$
  由于满足全微分，则混合偏导数是相等的，因此：
  $$\begin{aligned} \frac{\partial^2 U}{\partial V \partial S} = \frac{\partial^2 U}{\partial S \partial V} \end{aligned}$$
  因此：
    $$\begin{aligned}
   (\frac{\partial T}{\partial V})_S =  -(\frac{\partial P}{\partial S})_V \tag{2.1.4}
  \end{aligned}$$
* 我们对焓的公式两端求微分可以得到：
  $$\begin{aligned} \mathrm{dH} = \mathrm{dU} + \mathrm{d(pV)} 
  \\ = T\mathrm{dS} + V\mathrm{dp} \tag{2.1.4}
  \end{aligned}$$
  我们视H为S和p的函数，同样对其进行全微分：
  $$\begin{aligned}
   \mathrm{dH}=(\frac{\partial H}{\partial S})_p\mathrm{dS} + (\frac{\partial H}{\partial p})_S\mathrm{dp} \tag{2.1.5}
  \end{aligned}$$
  其中：
  $$\begin{aligned}
   (\frac{\partial H}{\partial S})_p = T,(\frac{\partial H}{\partial p})_S = V \tag{2.1.5}
  \end{aligned}$$
  因满足全微分，因此可以得到：
   $$\begin{aligned}
   (\frac{\partial T}{\partial p})_S =  (\frac{\partial V}{\partial S})_p \tag{2.1.6}
  \end{aligned}$$
* 对自由能函数F求微分可以得到：
  $$\begin{aligned} \mathrm{dF} = \mathrm{dU} - \mathrm{d(TS)} 
  \\ = -S\mathrm{dT} - p\mathrm{dV} \tag{2.1.7}
  \end{aligned}$$
  我们视F为T和V的函数，同样对其进行全微分：
  $$\begin{aligned}
   \mathrm{dF}=(\frac{\partial F}{\partial T})_V\mathrm{dT} + (\frac{\partial F}{\partial V})_T\mathrm{dV} 
  \end{aligned} $$
  其中：
  $$\begin{aligned}
   (\frac{\partial F}{\partial T})_V = -S,(\frac{\partial F}{\partial V})_T = -p 
  \end{aligned} \tag{2.1.8}$$
  因满足全微分，因此可以得到：
   $$\begin{aligned}
   (\frac{\partial S}{\partial V})_T =  (\frac{\partial p}{\partial T})_V \tag{2.1.9}
  \end{aligned}$$
* 根据吉布斯G函数的定义做同样的操作可以得到：
    $$\begin{aligned}
   \mathrm{dG}=(\frac{\partial G}{\partial F})_{pV}\mathrm{dF} + (\frac{\partial G}{\partial {pV}})_F\mathrm{d(pV)} 
   \\ =-S\mathrm{dT} + V\mathrm{dp}
   \tag{2.1.10}
  \end{aligned}$$
    $$\begin{aligned}
   (\frac{\partial G}{\partial T})_p = -S,(\frac{\partial G}{\partial p})_T = V \tag{2.1.11}
  \end{aligned}$$
   $$\begin{aligned}
   (\frac{\partial S}{\partial p})_T =  -(\frac{\partial V}{\partial T})_p \tag{2.1.12}
  \end{aligned}$$
---
## §2.2 麦克斯韦关系的简单应用
---
### **麦克斯韦关系**
   $$\begin{aligned}
   (\frac{\partial T}{\partial V})_S =  -(\frac{\partial P}{\partial S})_V \tag{2.2.1}
  \end{aligned}$$
   $$\begin{aligned}
   (\frac{\partial T}{\partial p})_S =  (\frac{\partial V}{\partial S})_p \tag{2.2.2}
  \end{aligned}$$
   $$\begin{aligned}
   (\frac{\partial S}{\partial V})_T =  (\frac{\partial p}{\partial T})_V \tag{2.2.3}
  \end{aligned}$$
    $$\begin{aligned}
   (\frac{\partial S}{\partial p})_T =  -(\frac{\partial V}{\partial T})_p \tag{2.2.4}
  \end{aligned}$$

* 可以得到如下式子成立：
  $$\begin{aligned}
  C_V = (\frac{\partial U}{\partial T})_V = T(\frac{\partial S}{\partial T})_V \tag{2.2.5}
  \end{aligned}$$

  $$\begin{aligned}
  C_p = (\frac{\partial H}{\partial T})_p = T(\frac{\partial S}{\partial T})_p \tag{2.2.6}
  \end{aligned}$$

  结合麦克斯韦关系可以进一步得到：
  $$\begin{aligned}
    C_V = (\frac{\partial U}{\partial T})_V = T(\frac{\partial S}{\partial T})_V \tag{2.2.7}
  \end{aligned}$$
  $$\begin{aligned}
    C_p = (\frac{\partial H}{\partial T})_p = T(\frac{\partial S}{\partial T})_p \tag{2.2.8}
  \end{aligned}$$
* 此外可以证明：
  * 绝热压缩系数$\kappa_S$和等温压缩系数$\kappa_T$之比等于定容热熔和定压热容之比.
  绝热压缩系数$\kappa_S$的定义是：$\kappa_S = -\frac{1}{V}(\frac{\partial V}{\partial p})_S$
  等温压缩系数$\kappa_T$的定义是：$\kappa_T = -\frac{1}{V}(\frac{\partial V}{\partial p})_T$
  因此得到：
  $$\begin{aligned}
  \frac{\kappa_S}{\kappa_T} = \frac{-\frac{1}{V}(\frac{\partial V}{\partial p})_S}{-\frac{1}{V}(\frac{\partial V}{\partial p})_T} 
  \\ = \frac{\frac{\partial (V,S)}{\partial (p,S)}}{\frac{\partial (V,T)}{\partial (p,T)}} =  \frac{\frac{\partial (V,S)}{\partial (V,T)}}{\frac{\partial (p,S)}{\partial (p,T)}} 
  \\ = \frac{(\frac{\partial S}{\partial T})_V}{(\frac{\partial S}{\partial T})_p} \tag{2.2.14}
  \end{aligned}$$
  上式中第二行运用了雅可比行列式进行变换
  * $$\begin{aligned}
  C_p - C_V = -T\frac{(\frac{\partial p}{\partial T})^2_V}{(\frac{\partial P}{\partial v})_T} \tag{2.2.15}
  \end{aligned}$$
  证明：
  $$\begin{aligned}C_p = T(\frac{\partial S}{\partial T})_p
  = T\frac{\partial (S,p)}{\partial (T,p)}
  = T\frac{\frac{\partial (S,p)}{\partial (T,V)}}{\frac{\partial (T,p)}{\partial (T,V)}}
  \\ = T\frac{(\frac{\partial S}{\partial T})_V(\frac{\partial p}{\partial V})_T - (\frac{\partial S}{\partial V})_T(\frac{\partial p}{\partial T})_V }{(\frac{\partial p}{\partial V})_T}
  \\ = C_V -T\frac{(\frac{\partial p}{\partial T})^2_V}{(\frac{\partial p}{\partial V})_V} 
  \end{aligned}$$

  根据上述全微分及它们的微分表达式，结合麦克斯韦关系，可以推导出以 $p，T，V$ 之中任意两个热力学量为独立变量的微分表达式，如下：

其中

$C_V = T \left( \frac{\partial S}{\partial T} \right)_V， C_p = T \left( \frac{\partial S}{\partial T} \right)_p$

---
## §2.3 气体的节流过程和绝热膨胀过程
---
* **节流过程**
  ![](\Pic/节流过程.jpg)
  绝热的不导热材料包着系统，多孔塞两边各维持着较高的压强p1和较低的压强p2，于是气体从高压不断流向低压一端，并且达到**定常状态**，这个过程就叫做节流过程.测量表明，在节流过程前后，气体的温度发生了变化，这个效应称为**焦耳——汤姆孙效应**，简称**焦——汤效应**.
  * **热力学过程分析**
  通过多孔塞前，热力学参量为(p1,V1,U1);
  通过多孔塞后，热力学参量为(p2,V2,U2);
  在节流过程中外界对系统做功是：p1V1-p2V2,因为材料不导热，系统是绝热的，基于热力学第一定律可知：U2-U1 = p1V1 - p2V2
  即：
  $$\begin{aligned} H_1 = H_2 \tag{2.3.1} \end{aligned}$$
  ==这表明在节流过程前后，气体的焓不变==
  定义：
  $$\begin{aligned} \mu = (\frac{\partial T}{\partial p})_H \end{aligned}  \tag{2.3.2}$$
  表示在焓不变的条件下气体温度随压强的变化率，称为**焦汤系数**，取T、p为状态参量，状态函数焓可表示为H = H(T,p).偏导数之间满足下列关系：
  $$\begin{aligned}
  (\frac{\partial T}{\partial p})_H(\frac{\partial p}{\partial H})_T(\frac{\partial H}{\partial T})_p = -1
  \end{aligned} \tag{2.3.3}$$
  进一步可以得到：
    $$\begin{aligned} \mu = (\frac{\partial T}{\partial p})_H \end{aligned} = -\frac{(\frac{\partial H}{\partial p})_T}{(\frac{\partial H}{\partial T})_p}  $$
  并由前面可知有：
  $$\begin{aligned} C_p = T(\frac{\partial S}{\partial T})_p = (\frac{\partial H}{\partial T})_p \end{aligned}$$
  $$\begin{aligned}(\frac{\partial H}{\partial p})_T = T(\frac{\partial S}{\partial p})_T + V\end{aligned}$$
  根据麦氏关系又有：
  $$\begin{aligned} (\frac{\partial S}{\partial p})_T = -(\frac{\partial V}{\partial T})_p \end{aligned}$$
  再进一步可以得到：
    $$\begin{aligned} \mu = -\frac{(\frac{\partial H}{\partial p})_T}{(\frac{\partial H}{\partial T})_p}
   \end{aligned} = \frac{1}{C_p}[T(\frac{\partial V}{\partial T})_p -V] \tag{2.3.4}$$
   或者
   $$\begin{aligned}
    \mu = \frac{V}{C_p}(T\alpha -1) \tag{2.3.5}
   \end{aligned}$$
  * 对于理想气体而言，其体胀系数$\alpha = \frac{1}{T}$,因此焦汤系数为零，因此==理想气体在节流过程前后温度不变==,此外==节流过程是不可逆过程==
  对于实际气体，$\mu$取不同情况时的温度变化：
     1. $\mu = 0，\alpha T=1$,节流过程前后温度不变(理想气体)( \alpha T=1 称为反转曲线)
     2. $\mu < 0，\alpha T=1$,节流过程前后温度升高(制温区)
     3. $\mu > 0，\alpha T=1$,节流过程前后温度降低(制冷区)
* 绝热膨胀
  我们将过程近似地看作是准静态的，在准静态绝热过程中气体的熵保持不变，由：
  $$\begin{aligned}
   \mathrm{dS} = (\frac{\partial S}{\partial T})_p\mathrm{dp} + (\frac{\partial S}{\partial p})_T\mathrm{dT} = 0
  \end{aligned}$$
  可以得到：
  $$\begin{aligned}
   \mu = (\frac{\partial T}{\partial p})_S = -\frac{(\frac{\partial S}{\partial p})_T}{(\frac{\partial S}{\partial T})_p} = \frac{T}{C_p}(\frac{\partial V}{\partial T})_p 
   = \frac{VT\alpha}{C_p} \tag{2.3.8}
  \end{aligned}$$
  可以看出：
  在绝热状态下，随着体积膨胀压强降低，气体的温度必然下降，从能量转化的角度看，气体在绝热膨胀过程中减少其内能而对外做功，膨胀后的气体分子间的平均距离增大，吸引力减弱而使得分子间的相互作用能增大.内能减少而相互作用能增大，分子的平均动能必然减少，因而气体的温度下降.气体的绝热膨胀过程也被用来使气体降温并液化
---
## §2.4 基本热力学函数的确定
---

### 总结
----
##### （一）内能

###### 1\. 内能全微分

$dU = TdS - pdV = \left( \frac{\partial U}{\partial S} \right)_V dS + \left( \frac{\partial U}{\partial V} \right)_S dV$

###### 2\. 麦克斯韦关系（内能）

$\left( \frac{\partial T}{\partial V} \right)_S = - \left( \frac{\partial p}{\partial S} \right)_V$

##### （二）焓( $H = U + pV$ )

###### 1\. 焓全微分

$dH = TdS + Vdp = \left( \frac{\partial H}{\partial S} \right)_p dS + \left( \frac{\partial H}{\partial p} \right)_S dp$

###### 2\. 麦克斯韦关系（焓）

$\left( \frac{\partial T}{\partial p} \right)_S = \left( \frac{\partial V}{\partial S} \right)_p$

##### （三）自由能（ $F = U - TS$ ）

###### 1\. 自由能全微分

$dF = -SdT - pdV = \left( \frac{\partial F}{\partial T} \right)_V dT + \left( \frac{\partial F}{\partial V} \right)_T dV$

###### 2\. 麦克斯韦关系（自由能）

$\left( \frac{\partial S}{\partial V} \right)_T = \left( \frac{\partial p}{\partial T} \right)_V$

##### （四）吉布斯函数( $G = U - TS +pV$ )

###### 1\. 吉布斯函数全微分

$dG = -SdT + Vdp = \left( \frac{\partial G}{\partial T} \right)_p dT + \left( \frac{\partial G}{\partial p} \right)_T dp$

###### 2\. 麦克斯韦关系（吉布斯函数）

$\left( \frac{\partial S}{\partial p} \right)_T = - \left( \frac{\partial V}{\partial T} \right)_p$

------
------
##### 1\. 当以 $(T,V)$ 为独立变量时

① $dU=C_VdT+\left[T\left(\frac{\partial p}{\partial T}\right)_V-p\right]dV$

② $dH=\left[C_V+V\left(\frac{\partial p}{\partial T}\right)_V\right]dT+\left[T\left(\frac{\partial p}{\partial T}\right)_V+V\left(\frac{\partial p}{\partial V}\right)_T\right]dV$

③ $dF=-SdT-pdV$

④ $dG=\left[-S+V\left(\frac{\partial p}{\partial T}\right)_V\right]dT+V\left(\frac{\partial p}{\partial V}\right)_TdV$

⑤ $dS=\frac{C_V}{T}dT+\left(\frac{\partial p}{\partial T}\right)_VdV$

##### 2\. 当以 $(T,p)$ 为独立变量时

① $dU=\left[C_p-p\left(\frac{\partial V}{\partial T}\right)_p\right]dT-\left[T\left(\frac{\partial V}{\partial T}\right)_p+p\left(\frac{\partial V}{\partial p}\right)_T\right]dp$

② $dH=C_pdT+\left[-T\left(\frac{\partial V}{\partial T}\right)_p+V\right]dp$

③ $dF=\left[-S-p\left(\frac{\partial V}{\partial T}\right)_p\right]dT-p\left(\frac{\partial V}{\partial p}\right)_Tdp$

④ $dG=-SdT+Vdp$

⑤ $dS=\frac{C_p}{T}dT-\left(\frac{\partial V}{\partial T}\right)_pdp$

##### 3\. 当以 $(p,V)$ 为独立变量时

① $dU=C_V\left(\frac{\partial T}{\partial p}\right)_Vdp+\left[C_p\left(\frac{\partial T}{\partial V}\right)_p-p\right]dV$

② $dH=\left[C_V\left(\frac{\partial T}{\partial p}\right)_V+V\right]dp+C_p\left(\frac{\partial T}{\partial V}\right)_pdV$

③ $dF=-S\left(\frac{\partial T}{\partial p}\right)_Vdp-\left[S\left(\frac{\partial T}{\partial V}\right)_p+p\right]dV$

④ $dG=\left[-S\left(\frac{\partial T}{\partial p}\right)_V+V\right]dp-S\left(\frac{\partial T}{\partial V}\right)_pdV$

⑤ $dS=\frac{C_V}{T}\left(\frac{\partial T}{\partial p}\right)_Vdp+\frac{C_p}{T}\left(\frac{\partial T}{\partial V}\right)_pdV$$

------

---
## §2.5 特性函数
---
* **特性函数**
  马修在1869年证明，如果是适当地选择独立变量(自然变量)，只要知道一个热力学函数，就可以通过求偏导数求得均匀系统的全部热力学函数，从而把均匀系统的性质完全确定下来.这个热力学函数即称作**特性函数**，表明它是表征均匀系统的特性的.
* **吉布斯-亥姆霍兹方程**
  1. 自由能函数F的亥姆霍兹方程：
  2. 吉布斯函数G的亥姆霍兹方程：
  3. 焓函数H的亥姆霍兹方程
  * 自由能函数F亥姆霍兹方程：
    根据：
    $$\begin{aligned} \mathrm{d}F = -S\mathrm{d}T -p\mathrm{d}V \end{aligned}\tag{2.5.1}$$
    $\Rightarrow$
    $$\begin{aligned} S = -\frac{\partial F}{\partial T}, 
    p = -\frac{\partial F}{\partial V}  \end{aligned}\tag{2.5.2}$$
    如果已知F(T,V)，求算F对T的偏导数即可得到熵函数S(T,V);求算F对V的偏导数就可以得到压强p(T,V),这就是物态方程.
    根据自由能函数定义：F = U-TS，有：
    $$\begin{aligned} U = F + TS = F -T\frac{\partial F}{\partial T} \end{aligned}\tag{2.5.3}$$
    上式给出内能U(T,V).这样，物态方程、内能和熵这三个热力学基本方程都可以通过F(T,V)求出.
    式$(2.5.3)$称为**吉布斯-亥姆霍兹方程**
  * 吉布斯函数G亥姆霍兹方程：
    根据：
    $$\begin{aligned} \mathrm{d}G = -S\mathrm{d}T + V\mathrm{d}p\end{aligned}\tag{2.5.4}$$
    $\Rightarrow$
    $$\begin{aligned} S = -\frac{\partial G}{\partial T},V = \frac{\partial G}{\partial p} \end{aligned}\tag{2.5.5}$$
    如果已知G(T,p),求算G对T的偏导就能得到熵函数(T,p);求算G对p的偏导就能得到体积V(T,p),这就是物态方程.
    根据吉布斯函数的定义：G = F + pV，有：
    $$\begin{aligned} U = G + TS -pV = G - T\frac{\partial G}{\partial T} - p\frac{\partial G}{\partial p}          \end{aligned}\tag{2.5.6}$$
    上式给出内能U(T,p).这样，物态方程、内能和熵这三个热力学基本方程都可以通过G(T,p)求出.
    式$(2.5.6)$称为**吉布斯-亥姆霍兹方程**
  * 焓函数H亥姆霍兹方程
    根据：
    $$\begin{aligned} H = U + pV = U + G -F = G + TS \end{aligned}$$  
    $\rightarrow$
    $$\begin{aligned} H = G -T\frac{\partial G}{\partial T} \end{aligned}\tag{2.5.7}$$
    上式也被称为**吉布斯-亥姆霍兹方程**
* **表面系统的热力学函数**
  * 表面系统：表面系统是指液体和其他相的交界面.表面系统实际上是很薄的一层，在于分界面垂直的方向上表面的性质变化急剧.描述表面系统的状态参量有表面张力系数$\sigma$和表面积A(相当于流体的p和V)
  * 表面系统的物态方程是$\sigma$、A和T的关系：f($\sigma$,A,T) = 0，即$\sigma$ = $\sigma$(A,T)
  实验表明，表面张力系数只是温度T的函数，与表面积A无关，因此物态方程可以简化为：$\sigma$ = $\sigma$(T).
  当表面积有微量改变时，外界做的功为：
  $$\begin{aligned}\mathrm{d}W = \sigma\mathrm{d}A\end{aligned}$$
  表面系统自由能F的全微分为：
  $$\begin{aligned} \mathrm{d}F = -S\mathrm{d}T + \sigma\mathrm{d}A  \end{aligned}\tag{2.5.9}$$
  因此：
  $$\begin{aligned} S = -\frac{\partial F}{\partial T};\sigma = \frac{\partial F}{\partial A} \end{aligned}\tag{2.5.10}$$
  对上式右式积分可以得到：
  $$\begin{aligned} F = \sigma A \end{aligned}\tag{2.5.11}$$
  由于当表面积A区域零时，其自由能应当为零，因此上式不存在积分常数项.
  由此：
  $$\begin{aligned} S = -A\frac{\partial \sigma}{\partial T} \end{aligned}\tag{2.5.12}$$
  由自由能F的方程有F = U -TS有：
  $$\begin{aligned} U = A(\sigma - T\frac{\partial \sigma}{\partial T}) \end{aligned}\tag{2.5.13}$$
  上式即为表面系统的热力学函数

***
## §2.6 热辐射的热力学理论
***
* 热辐射特点：
  **1、任何物体，只要温度高于0K ，就会不停地向周围空间发出热辐射**
  **2、可以在真空和空气中传播**
  **3、伴随能量形式的转变**
  **4、具有强烈的方向性**
  **5、辐射能与温度和波长均有关**
  **6、发射辐射取决于温度的4次方**

* 平衡辐射
  1. 如果辐射体对电磁波的吸收和辐射达到平衡，热辐射的特性将只取决于温度而与辐射体的其他特性无关，称为平衡辐射.
  2. 平衡辐射包含各种频率、沿各个方向传播的电磁波.这些电磁波的振幅和相位是无规则的.热力学的一般论据表明，平衡辐射是空间均匀和各向同性的.它的内能密度与内能密度对频率的分布只于温度有关而与辐射体的其他性质无关.
  关于这一点，简易论证如下：
  设想有两个温度相等但内能密度不等的密闭空间，并且只允许某一范围内的电磁波在两空间内传播.由于内能密度并不相等，这样，能量将从内能密度高的一侧空间流向另一空间，能量输入将使得两空间存在温度差，获得能量的一侧温度升高，流失能量的一侧温度降低.于是，能量自发从低温区域流向高温区域，显然这违背了克劳修斯对热力学第二定律的表述，这是不可能的.因此，其内能密度及对频率的分布只能是温度的函数.

* 平衡辐射的热力学函数之内能密度与温度的关系
  * 根据电磁理论关于**辐射压强p**与**辐射能量密度u**的关系：
    $$\begin{aligned} p = \frac{1}{3} u \end{aligned}\tag{2.6.1}$$
    论证如下：
     * 在黑体上取面元$\mathrm{d}s$，四周的辐射可以看成是来自$\mathrm{d}s$所在点为圆心，以任意可能值R为半径的半球面辐射到$\mathrm{d}s$上的，下面计算由半球面辐射到面元$\mathrm{d}s$上的辐射压力：
     ![辐射模型](/)
     在球面上取薄圆环$\mathrm{d}\varphi$,面元$\mathrm{d}s$可以表示为：
     $$\begin{aligned}\mathrm{d}\varphi = 2\pi R\sin\theta\cdot R\mathrm{d}\theta\end{aligned}\tag{(1)}$$
     若能量通过小面元$\mathrm{d}\varphi$辐射到$\mathrm{d}s$,那么,$\mathrm{d}s$所受到的总的辐射压力为：
     $$\begin{aligned} \mathrm{d}F = p_0 \mathrm{d}s\cos\theta\end{aligned}\tag{(2)}$$
     $p_0$为垂直辐射时的辐射压强
     为得到垂直辐射压强与辐射能量密度u的关系，
     我们做如下推导：
       * 取一黑体处于辐射平衡状态，在其表面任取一小面积元，那么黑体在$\mathrm{d}t$时间内接受 垂直辐射的能量为：（辐射能量以光速c辐射）
       $$\begin{aligned} \mathrm{d}u = u\cdot\mathrm{d}V = u\cdot c\mathrm{d}t\mathrm{d}s \end{aligned}\tag{(3)}$$
       若黑体与接触面理想光滑，那么当黑体接受辐射能量时，必然会因为受到辐射压力的作用而引起移动.设黑体移动的速率为v，则在$\mathrm{d}t$时间内黑体接受辐射的有效体积不再是c$\mathrm{d}t\mathrm{d}s$,黑体实际上接受的辐射能量为：
       $$\begin{aligned}\mathrm{d}u\prime = u\cdot (c-v)\mathrm{d}t\mathrm{d}s\end{aligned}\tag{(4)}$$
       基于能量守恒定律，该过程中损失的辐射能就等于黑体移动过程中辐射压力所做的功.垂直辐射时的辐射压强为$p_0$，因此：
       $$\begin{aligned} u - u\prime = uv\mathrm{d}t\mathrm{d}s =p_0 v\mathrm{d}s\mathrm{d}t \end{aligned}\tag{(5)}$$
       即：
       $$\begin{aligned} p_0 = u \end{aligned}\tag{(6)}$$
    至此，我们得到了垂直辐射压强和辐射能量密度的关系，带入((2))中有：
    $$\begin{aligned} \mathrm{d}F = u\cdot\mathrm{d}s\cos\theta \end{aligned}$$
    于是小面元上受到的垂直压力为：
    $$\begin{aligned} \mathrm{d}F_s = u\cdot\mathrm{d}s\cos\theta\cdot\cos\theta = u\cos^2\theta\mathrm{d}s \end{aligned}\tag{(7)}$$
    对于不同的$\theta$，面元面积不同.对此可以进行积分平均：
    $$\begin{aligned}
     \bar{\mathrm{d}F_s} = \frac{\int {\mathrm{d}F_s}{\mathrm{d}\varphi}}{\mathrm{d}\varphi}
     \\ = \frac{\int_0^\frac{\pi}{2} u \cos^2 \theta \mathrm{d}s\cdot 2\pi R^2\sin\theta\mathrm{d}\theta}{\int_0^\frac{\pi}{2}2\pi R^2\sin\theta\mathrm{d}\theta}
     \\=\frac{1}{3}u\mathrm{d}s
    \end{aligned}$$ 
    至此，我们得到了重要结论：
    **在一般情形中，辐射压强和辐射能量密度之间是三分之一的关系**
    
    阅读论文引用点击访问：[空腔辐射中辐射压强与辐射能量密度之间关系](https://kns.cnki.net/kcms/detail/detail.aspx?dbcode=CJFD&dbname=CJFD2005&filename=SLXK200503051&uniplatform=NZKPT&v=xDDRZThKQLzRR3nLVbaVIA1Hk%25mmd2FSeni9Mr%25mmd2BxC60M65Hx5BIY7roee81lNjRK93OqW)
    > [1]佟华.空腔辐射中辐射压强与辐射能量密度之间关系[J].吉林师范大学学报(自然科学版),2005(03):128-129.
    
    将空间的平衡辐射看作热力学系统.选取温度T和体积V为状态参量.由于辐射是均匀的，其内能密度只是温度的函数，表征为：
    $$\begin{aligned} U(T,V) = u(T)V \end{aligned}\tag{2.6.2}$$
    利用热力学偏导关系：
    $$\begin{aligned} (\frac{\partial U}{\partial V})_T = T(\frac{\partial S}{\partial V})_T - p \end{aligned}$$
    上式左侧即为内能密度.
    利用麦氏关系：
    $$\begin{aligned} (\frac{\partial S}{\partial V})_T = (\frac{\partial p}{\partial T})_V \end{aligned}$$
    由此：
    $$\begin{aligned} u = \frac{T}{3}(\frac{\partial u}{\partial T})_V - \frac{u}{3}\end{aligned}$$
    因为内能密度只是温度的函数，因此:
    $$\begin{aligned} (\frac{\partial u}{\partial T})_V = \frac{\mathrm{d}u}{\mathrm{d}T} \end{aligned}$$
    解微分方程即可得到：
    $$\begin{aligned}
     u = aT^4
    \end{aligned}\tag{2.6.3}$$
    于是我们在叙述热辐射特点中的第六点：发射辐射取决于温度的4次方得到证明.
* 平衡辐射的热力学函数之辐射熵函数
   * 根据熵定义及热力学第一定律有：
     $$\begin{aligned}
      \mathrm{d}S = \frac{\mathrm{d}U + p\mathrm{d}V}{T}
     \end{aligned}$$
     并入内能密度和辐射压强的关系有：
     $$\begin{aligned}
      \mathrm{d}S = \frac{1}{T}\mathrm{d}(aT^4V) + \frac{1}{3}aT^3\mathrm{d}V
     \\=4aT^2V\mathrm{d}T + \frac{4}{3}aT^3\mathrm{d}V
     \\=\frac{4}{3}a\mathrm{d}(VT^3)
     \end{aligned}$$
     积分得到：
     $$\begin{aligned}
      S = \frac{4}{3}aT^3V
     \end{aligned}\tag{2.6.4}$$
     式中不存在积分常量的原因是在$VT^3$为零时不存在辐射场.
     根据克劳修斯不等式以及可逆绝热分析我们知道在可逆绝热过程中熵变为零，这时有:
     $$\begin{aligned}
      T^3V = const
     \end{aligned}\tag{2.6.5}$$
* 平衡辐射的热力学函数之吉布斯函数
   * 根据吉布斯函数G的定义：G = F + pV以及前述关系可以得到：
     $$\begin{aligned}
      G = U - TS + pV
      \\= aT^4V - \frac{4}{3}aT^4V + \frac{1}{3}aT^4V\equiv 0
     \end{aligned}\tag{2.6.6}$$
     此后我们会说明平衡辐射下吉布斯函数为零是**平衡辐射光子数不守恒**的结果     
* 辐射通量密度$J_u$与辐射内能密度u的关系 
      

  
   



