---
title: ProbabilityTheory
date: 2021-10-08 22:23:37
math: true
tags: ProbabilityTheory
categories: Probability Theory and Mathematical Statistics
---
   本章将以NKU的概统教材为顺序，梳理NKU版本教材下概统的知识点，知识点更新将随课程进度同步
***
[toc]
# 概率论与数理统计

## 概率论的基本概念

### 随机试验，样本空间，随机事件

**随机试验**：满足相同条件下可重复，能事先明确试验所有可能结果，在一次试验前无法确定哪一个结果出现的试验称为随机试验。

**样本空间**：将随机试验 $E$ 的所有可能结果组成的集合称为 $E$ 的样本空间。 $E$ 的每个结果称为样本点。

**随机事件**：称试验 $E$ 的样本空间 $S$ 的子集为 $E$ 的随机事件。

和事件，积事件，差时间，互斥事件与对立事件

交换律，结合律，分配律，德摩根律

### 频率与概率

**频率**：相同条件下，进行了 $n$ 次试验，事件 $A$ 发生的次数 $n_A$ 称为事件 $A$ 发生的频数，比值 $\frac{n_A}{n}$ 称为事件 $A$ 发生的频率，记为 $f_{n}(A)$ 。

**概率**：设 $E$ 是随机事件， $S$ 是它的样本空间。对于 $E$ 的每一个事件 $A$ 赋予一个实数，记为 $P(A)$ ，称为事件 $A$ 的概率，如果集合函数 $P(\cdot)$ 满足以下条件：

（1）非负性：对于每个事件 $A$ ，有 $P(A)\geq 0$ 。

（2）规范性：对于必然事件 $S$ ，有 $P(S)=1$ 。

（3）可列可加性：设 $A_1,A_2,\cdots$ 是两两不相容的事件，即对于 $A_{i}A_{j}=\emptyset ,i\neq j,i,j=1,2,\cdots$ ，有
$$
P(A_1\cup A_2\cup \cdots)=P(A_1)+P(A_2)+\cdots
$$

加法公式：对于任意两事件 $A,B$ 有

$$
P(A\cup B)=P(A)+P(B)-P(AB)
$$

### 古典概型

当随机试验满足样本空间内只有有限个元素，且每个基本事件发生的可能性相同，则称为**等可能概型**，又称**古典概型**。

超几何分布

### 条件概率

**条件概率**：设 $A,B$ 是两个事件，且 $P(A)>0$ ，称

$$
P(B|A)=\dfrac{P(AB)}{P(A)}
$$

为在事件 $A$ 发生的条件下事件 $B$ 发生的条件概率。

**乘法定理**：设 $P(A)>0$ ，则有 $P(AB)=P(B|A)P(A)$ 。

乘法定理可以推广到多个事件的积事件的情况。

**全概率公式**：设试验 $E$ 的样本空间为 $S$ ， $A$ 为 $E$ 的事件， $B_1,B_2,\cdots ,B_n$ 为 $S$ 的一个划分，且 $P(B_i)>0\quad (i=1,2,\cdots ,n)$ ，则
$$
P(A) = P(A|B_1)P(B_1)+P(A|B_2)P(B_2) + \cdots + P(A|B_n)P(B_n)
$$

**贝叶斯公式**：设试验 $E$ 的样本空间为 $S$ ， $A$ 为 $E$ 的事件， $B_1,B_2,\cdots ,B_n$ 为 $S$ 的一个划分，且 $P(A)>0,P(B_i)>0\quad (i=1,2,\cdots ,n)$ ，则
$$
P(B_i|A)=\dfrac{P(A|B_i)P(B_i)}{\displaystyle\sum_{j=1}^{n}{P(A|B_j)P(B_j)}},i=1,2,\cdots,n
$$

其中 $P(B_i)$ 称为先验概率， $P(B_i|A)$ 称为后验概率， $P(A|B_i)$ 称为似然概率。

### 独立性

独立：设 $A,B$ 是两事件，如果满足等式 $P(AB)=P(A)P(B)$ ，则称事件 $A,B$ 相互独立。简称 $A,B$ 独立。

设 $A,B$ 是两事件，且 $P(A)>0$ 。若 $A,B$ 相互独立，则 $P(B|A)=P(B)$ 。反之亦然。

若事件 $A$ 与 $B$ 相互独立，则下边各对事件也相互独立：

$$
A\text{与} \overline{B} \quad \overline{A}\text{与} {B} \quad \overline{A}\text{与} \overline{B}
$$

一般的，设 $A_1,A_2,\cdots,A_n$ 是 $n$ 个事件，如果对于其中任意2个，任意3个，···，任意 $n$ 个事件的积事件的概率，都等于各事件概率之积，则称事件 $A_1,A_2,\cdots,A_n$ **相互独立**。

## 随机变量及其分布

### 随机变量
  * 设随机试验的样本空间S = {e}，X=X(e)是定义在样本空间S上的实值单值函数，则称X=X(e)为**随机变量**
  * 随机变量分为
    1. 离散型随机变量
    2. 非离散型随机变量，而非离散型随机变量又包括
       * 连续型随机变量
       * 其他类型                                                                                                               
### 离散型随机变量的分布律
  * $\color{yellow}{离散型随机变量的定义}$
    有些随机变量，它全部可能的取值是有限个或可列无限多个，这样的随机变量称为**离散型随机变量**
  * $\color{yellow}{离散型随机变量的表示}$
    $$\begin{aligned}
     P(X = x_k) = p_k，k = 1,2,3\cdots
    \end{aligned}$$ 
    上式称为离散型随机变量的分布律
    * $p_k$满足如下两个条件
      1. $0 \leq p_k$
      2. $\sum_{i=1}^{\infty}p_k = 1$
  * $\color{yellow}{离散型随机变量的分布律}$
    * $\color{yellow}{几何分布}$
      几何分布又称为**首次成功模型**
      $$\begin{aligned}
       P(X=k) = p(1-p)^{k-1} \quad k =1,2,3\cdots
      \end{aligned}$$
    * $\color{yellow}{(0-1)分布}$
      若随机变量的X值只能取0或1两个值，那么随机变量的分布律为
      $$\begin{aligned}
       P(X = k) = p^k(1-p)^{1-k} \quad k=0,1 \quad (0<p<1)
      \end{aligned}$$
    * $\color{yellow}{伯努利试验与二项分布}$
      若试验E只有两个结果$A,\bar{A}$，则称试验E为**伯努利试验**，将E独立重复地进行n次，则称这一串重复的独立试验为n重伯努利试验
      二项分布的分布律为
      $$\begin{aligned}
       P(X = k) = C_n^kp^{k}(1-p)^{1-k}=C_n^kp^{k}q^{1-k} \quad (q=1-p)
      \end{aligned}$$
      等式右侧恰好是二项式$(p+q)^n$的展开式中出现$p^k$的那一项，我们称**随机变量X服从参数为n,p的二项分布**，并记为X~$b(n,p)$
      当n=1时二项分布就退化为(0-1)分布
    * $\color{yellow}{泊松分布与泊松定理}$
      设随机变量X所有可能的取值为$0,1,2\cdots$，而各个取值的概率为
      $$\begin{aligned}
       P(X= k) = \frac{\lambda^k e^{-\lambda}}{k!} \quad (k=1,2\cdots)
      \end{aligned}$$ 
      其中$\lambda$是大于零的常数，则称**随机变量X服从参数为$\lambda$的泊松分布**，记为X~$\pi(\lambda)$
      由概率的公理化定义可知
      $$\begin{aligned}\sum_{k=1}^{\infty}P(X=k) = 1\end{aligned}$$
      因此
      $$\begin{aligned}
       \sum_{k=1}^{\infty}P(X = k) = \sum_{k=1}^{\infty}\frac{\lambda^k e^{-\lambda}}{k!} = e^{-\lambda}\sum_{k=1}^{\infty}\frac{\lambda^{k}}{k!} = 1 \Rightarrow  \sum_{k=1}^{\infty}\frac{\lambda^{k}}{k!} = e^{\lambda}
      \end{aligned}$$
      **泊松定理** 设$\lambda$为大于零的常数，n是任意正整数，设 $np_n = \lambda$，则对任一固定的非负整数k，有
      $$\begin{aligned}
       \lim_{n\to \infty}C_n^k p_n^k (1-p_n)^{1-k} = \frac{\lambda^k e^{-\lambda}}{k!}
      \end{aligned}$$
      这意味着当n很大而概率p很小时，可以用泊松分布近似计算二项分布
### 随机变量的分布函数

  * $\color{yellow}{随机变量的分布函数定义}$：设X是一个随机变量，x是任意函数，函数
    $$\begin{aligned}
     F(x) = P(X\leq x) \quad -\infin <x< \infin
    \end{aligned}$$
    称为X的**分布函数**
  * $\color{yellow}{重要公式}$
    $$\begin{aligned}
     P(x_1<X \leq x_2) = F(x_2) - F(x_1)
    \end{aligned}$$
    $$\begin{aligned}
     P(X>a) = 1 - F(a)
    \end{aligned}$$
    $$\begin{aligned}
     P(x_1<X < x_2) = F(x_2) - F(x_1) - P(X=x_2)
    \end{aligned}$$
* $\color{yellow}{分布函数的基本性质}$
  1. $F(x)$是一个不减函数(这是因为$F(x)$函数之间的运算表述的是在某一段区间内的概率，而概率具有非负性)
     $$\begin{aligned}
      F(x_2) - F(x_1) = P(x_1<X\leq x_2)≥0
     \end{aligned}$$
  2. $0\leq F(x)\leq 1$，且
     $$\begin{aligned}
      F(-\infin) = \lim_{x\to -\infty}F(x) = 0，F(\infty) = \lim_{x\to \infty}F(x) = 1
     \end{aligned}$$
  3. $F(x+0) = F(x)$，即F(x)是右连续的
  $\color{red}{具备上述三条性质的函数F(x)必定是某个随机变量的分布函数，上述三个条件是判断一个函数是否是分布函数的重要判据}$


### 连续型随机变量及其概率密度
 * 如果对于随机变量X的分布函数F(x)，存在非负可积函数f(x)，使对于任意实数x，有
   $$\begin{aligned}
    F(x) = \int_{-\infty}^xf(t)dt
   \end{aligned}$$
则X称为**连续型随机变量**，f(x)称为X的**概率密度函数**，简称**概率密度**
 * 概率密度函数f(x)具有以下性质
  1. f(x)≥0
  2. $\int_{-\infty}^{\infty}f(x)dx=1$
  3. 对于任意实数$x_1,x_2(x_1\leq x_2)$
     $$\begin{aligned}
      P(x_1< X\leq x_2) = F(x_2)-F(x_1)=\int_{x_1}^{x_2}f(x)dx
     \end{aligned}$$
  4. 若f(x)在点x处连续，则有$F'(x)=f(x)$
 * 需要指出的是，对于连续型随机变量，它取任一指定实数值a的概率均为零，即$P(X=a)\equiv 0$，**但这并不意味着事件{X=a}为不可能事件**，也就是说，不可能事件的概率一定为零，但概率为零不能说明事件是不可能事件    
 * 几种连续型随机变量的分布类型
   * **均匀分布**
     若连续型随机变量X具有概率密度
     $$f(x)=\begin{cases}
      \frac{1}{b-a}\quad,a<x<b \\\\
      0 \quad ,其他
     \end{cases}$$
     则称X在区间$(a,b)$上服从**均匀分布**，记为X~U$(a,b)$
     均匀分布的分布函数为
     $$F(x)=\begin{cases}
      0 \quad, x<a \\\\
      \frac{x-a}{b-a}  \quad,a\leq x<b \\\\
      1 \quad, x\geq b
     \end{cases}$$
   * **指数分布**
     若连续性随机变量X的概率密度为
     $$f(x)=\begin{cases}
      \frac{1}{\theta}e^{-\frac{x}{\theta}}\quad ,x>0 \\\\
      0 \quad ,其他
     \end{cases}$$
     其中$\theta>0$为常数，则称X服从参数为$\theta$的**指数分布**
     指数分布的分布函数为
     $$F(x)=\begin{cases}
      1 - e^{-\frac{x}{\theta}} \quad ,x>0 \\\\
      0 \quad,其他
     \end{cases}$$
     指数分布有一个重要的性质称为**无记忆性**
     $$\begin{aligned}
      P(X>s+t|X>s) = P(X>t)
     \end{aligned}$$
   * **正态分布**
     若连续型随机变量X的概率密度为
     $$\begin{aligned}
      f(x) = \frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{(x-\mu)^2}{2\sigma^2}} \quad ,-\infty<x<\infty
     \end{aligned}$$
     其中$\mu,\sigma(\sigma>0)$为常数，则称X服从参数为$\mu,\sigma$的**正态分布**或**高斯分布**，记为X~N$(\mu,\sigma^2)$ 
     正态分布曲线关于直线$x=\mu$对称，并在$x=\mu$取得最大值
     $\mu=0,\sigma=1$时的正态分布曲线称为**标准正态分布**，其概率密度和分布函数分别用$\varphi(x),\Phi(x)$表示
     $$\begin{cases}
      \varphi(x)=\frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}} \\\\
      \Phi(-x) = 1 -\Phi(x) 
     \end{cases}$$
     对于一般地正态分布X~N $(\mu,\sigma^2)$，我们可以通过线性变换将之化为标准正态分布X~N (0,1)
     * **线性变换转换引理**
       若X~N $(\mu,\sigma^2)$,则取Z=$\frac{x-\mu}{\sigma}$ 就可将之转化为X~N (0,1)

