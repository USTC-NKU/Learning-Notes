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
## 2.2 麦克斯韦关系的简单应用
---
### ==**麦克斯韦关系**==
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
## 2.3 气体的节流过程和绝热膨胀过程
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
## 2.4 基本热力学函数的确定
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
## 2.5 特性函数
---
* **特性函数**
  马修在1869年证明，如果是适当地选择独立变量(自然变量)，只要知道一个热力学函数，就可以通过求偏导数求得均匀系统的全部热力学函数，从而把均匀系统的性质完全确定下来.这个热力学函数即称作**特性函数**，表明它是表征均匀系统的特性的.
* **吉布斯-亥姆霍兹方程**
  





