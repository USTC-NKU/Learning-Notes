# Rigid body mechanics 刚体力学
---
**$$\begin{aligned}Organized\quad in\quad NKU \end{aligned}$$**
***

[toc]
* * *

## **角动量守恒定理：**
------------

在平动中就讲了动量守恒，在所受合外力为0，或则内力远远大于合外力的时候物体的动量是保持守恒的。在刚体转动过程中也有这样子的性质，当刚体所受合外力的力矩为0的时候，也就是 $M=0$ 时， $L=J\omega$ 将会保持衡量，不会变化。（该定律不但适用于刚体，同样也适用于绕定轴转动的任意物体系统。 ）

  

$M=0$ 的几种情况：

（1）合外力 $F$ 投影下来的 $F_{\bot}$ 为0。

（2）$F_{\bot}$ 与转动半径 $r$ 的夹角为0°。

  

推导过程：上次就讲了 $M=J\alpha$ 、 $L=J\omega$ ，而 $\alpha=\frac{d\omega}{dt}$ 。所以 $M=\frac{dL}{dt}$ 。所以 $\int_{t_{1}}^{t_{2}}Mdt=L_{t2}-L_{t1}$ 。当 $M=0$ 时， $\Delta L=0$ 。所以角动量守恒。书上的原话就是：**在某一时间段内，作用在刚体上的外力的冲量矩等于刚体的角动量增量。**（力矩对时间的积分就是冲量矩，角动量变化量就是角动量的增量）

  

角动量守恒的常见情况：

（1）转动惯量改变
假设人是一个圆柱（理想化一下），双臂张开的转动惯量 $J_{1}$ 肯定大于双臂收拢的转动惯量 $J_{2}$ ，在没有外力的情况下，一定会有 $\omega_{1}<\omega_{2}$ 。

（2）平动物体撞上刚体

* * *

### **1.力矩对刚体所做功的功率**
-----------------

公式：$P=M\omega$

单位：W

推导过程：对于合外力在极小的 $\Delta t$ 时间内所做的功，一定可以表示为： $dW=F \cdot ds=F \cdot sin\varphi \cdot rd\theta$ （高中数学公式： $ds=r \cdot d\theta$ 。又是两个向量相乘，所以要带上 $sin\varphi$ ）

![](\pic/4.jpg)  

而又因为 $M=Fr \cdot sin\varphi$ ，所以 $dW=Md\theta$ 。所以 $P=\frac{dW}{dt}=M\frac{d\theta}{dt}=M\omega$

### 2.力矩对刚体所做的功
-----------

公式： $W=\int_{0}^{\theta}Md\theta$

单位：J

推导过程：上面讲功率已经推到了 $dW$ 。所以积分一下就可以了。

## 2.刚体转动的动能
---------

公式： $E_{k}=\frac{1}{2} J \omega^{2}$

单位：J

推导过程： $dW=Md\theta$ ，而 $M=J\alpha=J\frac{d\omega}{dt}$ 。所以两式联立，得 $dW=J\frac{d\omega}{dt} d\theta=J\frac{d\theta}{dt} d\omega=J\omega d\omega$ 。所以动能 $E_{k}=\int_{0}^{\omega}dW=J\int_{0}^{\omega}\omega d\omega=\frac{1}{2}J\omega^{2}$

常见几种模型的各个量是否守恒：

![](\pic/5.jpg)  

## 3.刚体的重力势能
---------

公式： $E_{p}=mgh_{c}$ （ $h_{c}$ 是刚体质心到零势面的高度）

单位：J


## 4.刚体的机械能守恒
----------

公式： $E=E_{p}+E_{k}$

应用：_如图，质量为m，长为l的均匀细棒绕过O点的转轴自水平位置以零角速度自由下摆。求细棒运动到与水平夹角为 $\theta$ 时的角速度；_

![](\pic/6.jpg)  

解：根据能量守恒，重力势能减小量是 $\Delta E_{p}=mg\cdot \frac{1}{2}l\cdot sin\theta$ 。动力势能增量是 $\Delta E_{k}=\frac{1}{2}J\omega^{2}$ 。而根据上次讲的，易知 $J=\frac{1}{3}ml^{2}$ 。所以： $\Delta E_{p}=\Delta E_{k}$ 。解方程： $mg\cdot \frac{1}{2}l\cdot sin\theta = \frac{1}{6}ml^{2}\omega^{2} \Rightarrow \omega^{2}=\frac{3g sin\theta}{l} \Rightarrow \omega=\sqrt{\frac{3g sin\theta}{l}}$

* * *

在前面研究公式的时候，我们就发现了许多平动与刚体转动公式之间的惊人的相似 。就好像被人刻意设计过一样。下面把两边的公式总结并且类比一下。

![](\pic/7.jpg)  
![](\pic/8.jpg)  
![](\pic/9.jpg)  
