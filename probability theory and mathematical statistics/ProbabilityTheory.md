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
     正态分布曲线关于直线$x=\mu$对称，并在$x=\mu$取得最大值，另外，正态分布函数在$x\pm\sigma$处有拐点，曲线以x轴为渐近线
     $\mu=0,\sigma=1$时的正态分布曲线称为**标准正态分布**，其概率密度和分布函数分别用$\varphi(x),\Phi(x)$表示
     $$\begin{cases}
      \varphi(x)=\frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}} \\\\
      \Phi(-x) = 1 -\Phi(x) 
     \end{cases}$$
     对于一般地正态分布X~N $(\mu,\sigma^2)$，我们可以通过线性变换将之化为标准正态分布X~N (0,1)
     * **线性变换转换引理**
       若X~N $(\mu,\sigma^2)$,则取Z=$\frac{x-\mu}{\sigma}$ 就可将之转化为X~N (0,1)


### 随机变量的函数的分布
* 定理
  设随机变量X具有概率密度$f_X(x)$，$-\infty<x<\infty$，又设函数g(x)处处可导且函数严格单调，则Y=g(x)是连续型随机变量，其概率密度为
  $$\begin{aligned}
   f_Y(y)=\begin{cases}
   f_X[h(y)]h'(y)   ,\quad \alpha<x<\beta \\\\
   0  ,\quad else
   \end{cases}
  \end{aligned}$$
  其中$\alpha=\min(g(-\infty),g(\infty))$，$\beta=\max(g(-\infty),g(\infty))$，h(y)是g(x)的反函数
* 注意上述定理使用的条件要求函数是严格单调的，为此，若函数在所求指定区间内并非严格单调，则需要按照定义方式去解答，其步骤为
   * 1. 写出Y对X的反函数
   * 2. 写出Y的分布函数，将分布函数表征为X的分布函数
   * 3. 将写出的分布函数对Y求导数得到Y的概率密度函数
   * 4. 根据X的概率密度分布确定Y的概率密度函数表达式
   * 5. 注意一定要写出函数的定义域 


## 多维随机变量及其分布
### 二维随机变量
* 定义
  一般地，设E是一个随机试验，它的样本空间S={e}，设X=X{e}，Y=Y{e}是定义在S上的随机变量，由它们构成的向量(X,Y)叫做**二维随机变量**或**二维随机向量**
* 二维随机变量的性质不仅仅与每个变量本身有关，还与两个变量之间的关系有关
* 二维随机变量分布函数的定义
  设(X,Y)是二维随机变量，对于任意实数x,y，二元函数：
  $$\begin{aligned}
   F(x,y)=P(X\le x \cap Y\le y)=P(X\le x,Y\le y)
  \end{aligned}$$
  称为二维随机变量的**分布函数**，也叫做**联合函数**
  将二维随机变量(X,Y)看成平面上的随机点的坐标，那么分布函数的几何意义可以看成以点(x,y)为顶点而位于该点左下方的无穷矩形区域内的概率
* 分布函数的基本性质
  * 1. F(x,y)是变量x和y的不减函数，即对于任意固定的y，当$x_2>x_1$时$F(x_2,y)\ge F(x_1,y)$，当$y_2>y_1$时$F(x,y_2)\ge F(x,y_1)$
  * 2. $0\le F(x,y) \le 1$且
       * 对于任意固定的y，$F(-\infty,y)=0$
       * 对于任意固定的x，$F(x,-\infty)=0$
       * $F(-\infty,\infty)=0,F(\infty,\infty)=1$ 
  * 3. $F(x+0,y)=F(x,y),F(x,y+0)=F(x,y)$，即F(x,y)关于x右连续，关于y也右连续
  * 4. 对于任意$(x_1,y_1),(x_2,y_2),x_1<x_2,y_1<y_2$，下述不等式成立
  $$\begin{aligned}
   F(x_2,y_2)-F(x_1,y_2)-F(x_2,y_1)+F(x_1.y_1)\ge 0
  \end{aligned}$$ 
* 如果二维随机变量(X,Y)全部可能取到的数值是有限对或可列无限多对，则称(X,Y)是**离散型的随机变量**
* 设二维离散型随机变量(X,Y)所有可能取到的值为$(x_i,y_i)$，记$P(X=x_i,Y=y_i)=p_{ij}$，则由概率的定义有
  $$\begin{aligned}
   p_{ij}\ge 0, \quad \sum_{i=1}^{\infty}\sum_{j=1}^{\infty}p_{ij}=1
  \end{aligned}$$
* 对于二维随机变量(X,Y)的分布函数F(x,y)，如果存在非负可积函数f(x,y)使对于任意x,y有
  $$\begin{aligned}
   F(x,y)=\int_{-\infty}^{y}\int_{-\infty}^{x}f(u,v)dudv
  \end{aligned}$$
则称(X,Y)是**连续型二维随机变量**，函数f(x,y)称为二维随机变量的**概率密度**，也叫做**联合概率密度**
* 概率密度函数的性质
  * 1. $f(x,y)\ge 0$
  * 2. $\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}f(x,y)dxdy=1$
  * 3. 设G是xOy平面上的区域，点(X,Y)洛在G内的概率为
       $$\begin{aligned}
        P((X,Y)\in G)=\iint f(x,y)dxdy
       \end{aligned}$$
  * 4. 若f(x,y)在点(x,y)连续，则有
       $$\begin{aligned}
        \frac{\partial^2 F(x,y)}{\partial x\partial y}=f(x,y)
       \end{aligned}$$

### 边缘分布
* 二维随机变量(X,Y)作为一个整体，具有分布函数F(x,y).而X,Y都是随机变量，各自也存在分布函数，将他们分别记为$F_X(x)$,$F_Y(y)$ ，依次称为二维随机变量(X,Y)关于X和Y的**边缘分布函数**.边缘分布函数可以由二维随机变量(X,Y)的分布函数确定
  $$\begin{aligned}
   F_X(x)=P(X\le x)=P(X\le x,Y<\infty)=F(x,\infty)
  \end{aligned}$$
  $$\begin{aligned}
   F_Y(y)=F(\infty,y)
  \end{aligned}$$

* 对于离散型随机变量(以X为例，Y同理)
  $$\begin{aligned}
   F_X(x)=F(x,\infty)=\sum_{x_i\le x}\sum_{j=1}^{\infty}p_{ij}
  \end{aligned}$$
  $$\begin{aligned}
   P(X=x_i)=\sum_{j=1}^{\infty}p_{ij} \quad i=1,2\cdots
  \end{aligned}$$

  * 记符号
  $$\begin{aligned}
   p_{i\cdot}=\sum_{j=1}^{\infty}p_{ij}=P(X=x_i) \quad i=1,2\cdots
  \end{aligned}$$
  $$\begin{aligned}
   p_{\cdot j}=\sum_{i=1}^{\infty}p_{ij}=P(Y=y_j) \quad j=1,2\cdots
  \end{aligned}$$
  记号$p_{i\cdot}$后面的$\cdot$表示是由$p_{ij}$关于j求和后得到的，后者同理
  
  * 有了上面的公式和符号，我们引入**边缘分布律**的概念
  我们称$p_{i\cdot}$和$p_{\cdot j}$为(X,Y)关于X和Y的**边缘分布律**
  
* 对于连续型随机变量(X,Y)，设他的概率密度为f(x,y)
  $$\begin{aligned}
   F_X(x)=F(x,\infty)=\int_{-\infty}^x\Big[\int_{-\infty}^{\infty} f(x,y)dy\Big]dx
  \end{aligned}$$
  * 从上式容易看出随机变量X的概率密度为(Y同理)
    $$\begin{aligned}
     f_X(x)=\int_{-\infty}^{\infty}f(x,y)dy
    \end{aligned}$$
  * 分别称$f_X(x)$,$f_Y(y)$为(X,Y)关于X和关于Y的**边缘概率密度**

* 二维正态分布
  $$\begin{aligned}
   f(x,y)=\frac{1}{2\pi\sigma_1\sigma_2\sqrt{1-\rho^2}}\exp\Big(\frac{-1}{2(1-\rho^2)}\Big[\frac{(x-\mu_1)^2}{\sigma^2_1}-2\rho\frac{(x-\mu_1)(x-\mu_2)}{\sigma_1\sigma_2}+\frac{(y-\mu_2)^2}{\sigma^2_2}\Big]\Big)
  \end{aligned}$$  

  其中$\mu_1,\mu_2,\sigma_1,\sigma_2,\rho$都是常数，这就是**二维正态分布**
  * 通过计算二维正态分布的边缘概率密度我们可以发现，二维正态分布的两个边缘概率密度都是一维正态分布，并且都不依赖于参数$\rho$，即对于给定的$\mu_1,\mu_2,\sigma_1,\sigma_2$，不同的$\rho$对应不同的二维正态分布，但他们的边缘分布都是相同的.此外，单单知道两个边缘分布一般是不能确定其联合分布的

### 条件分布
* 设(X,Y)是二维离散随机变量，其分布律为$P(X=x,Y=y)=p_{ij}$，其关于X和Y的边缘分布律分别为
  $$\begin{aligned}
   P(X=x_i)=p_{i\cdot}=\sum_{j=1}^\infty p_{ij}
  \end{aligned}$$
  $$\begin{aligned}
   P(Y=y_j)=p_{\cdot j}=\sum_{i=1}^\infty p_{ij}
  \end{aligned}$$
  * **条件分布律**
  设(X,Y)是二维离散型随机变量，对于固定的j，若$P(Y=y_j)>0$，则称
  $$\begin{aligned}
   P(X=x_i|Y=y_j)=\frac{P(X=x_i,Y=y_j)}{P(Y=y_j)}=\frac{p_{ij}}{p_{\cdot j}}
  \end{aligned}$$
  为在$Y=y_j$条件下随机变量X的**条件分布律**,类似地定义X固定下对Y的条件分布律
  * 性质
    1. $P(X=x_i|Y=y_j)\ge 0$
    2. $\sum_{i=1}^\infty P(X=x_i|Y=y_j)=\frac{1}{p_{\cdot j}}\sum_{i=1}^\infty p_{ij}=1$
* 对于连续型随机变量，由于对于任意的x,y，P{X=x},P{Y=y}=0恒成立，这时就不能直接使用上面公式计算条件概率
  * **条件概率密度**
  设二维随机变量(X,Y)的概率密度为f(x,y)，(X,Y)关于Y的边缘概率密度为$f_Y(y)$，对于固定的y，$f_Y(y)>0$，则
  $$\begin{aligned}
   f_{X|Y}(x|y)=\frac{f(x,y)}{f_Y(y)}
  \end{aligned}$$
  为在Y=y条件下X的**条件概率密度**
  * **条件分布函数**
  $$\begin{aligned}
   \int_{-\infty}^{x}f_{X|Y}(x|y)\mathrm{dx}=\int_{-\infty}^x\frac{f(x,y)}{f_Y(y)}\mathrm{dx}
  \end{aligned}$$
  为在Y=y的条件下X的**条件概率分布函数**，记为$P(X\le x|Y=y)$或$F_{X|Y}(x|y)$

### 相互独立的随机变量
* 定义
  设F(x,y)及$F_X(x),F_Y(y)$分别是二维随机变量(X,Y)的分布函数及边缘分布函数，若对于所有x,y有
  $$\begin{aligned}
   P(X\le x,Y\le y)&=P(X\le x)P(y\le y) \Leftrightarrow \\
   F(x,y)&=F_X(x)F_Y(y)
  \end{aligned}$$
  则称随机变量X和Y是**相互独立的**
  * 设(X,Y)是连续型随机变量，$f(x,y),f_X(x),f_Y(y)$分别为(X,Y)的概率密度和边缘概率密度，则X和Y相互独立的**充要条件**等价于
  $$\begin{aligned}
   f(x,y)=f_X(x)f_Y(y)
  \end{aligned}$$
  * 当(X,Y)是离散型随机变量时，X和Y相互独立的条件等价于
  $$\begin{aligned}
   P(X=x_i,Y=y_j)=P(X=x_i)P(Y=y_j)
  \end{aligned}$$
  * 二维正态随机变量(X,Y)相互独立的**充要条件**是参数$\rho=0$
* n维随机变量的推广
  关于n维随机变量的分布函数、概率密度函数、边缘概率分布函数、边缘概率密度函数和相互独立性的定义可以参照二维随机变量的定义推广，为避免冗杂，此文不加描述，只提出重要的定理
  * **定理**
    设$(X_1,X_2,\cdots,X_m)$和$(Y_1,Y_2\cdots,Y_n)$相互独立，则$X_i$和$Y_j$相互独立，又若h,g是连续函数，则$h(X_1,X_2,\cdots,X_m)$和$g(Y_1,Y_2\cdots,Y_n)$相互独立

### 两个随机变量的函数的分布
* Z=X+Y分布
  * 设(X,Y)是二维连续型随机变量，它具有概率密度f(x,y)，则Z=X+Y为连续型随机变量，其概率密度为
    $$\begin{aligned}
     f_{X+Y}(z)=\int_{-\infty}^{\infty}f(z-y,y)\mathrm{dy}
    \end{aligned}$$
    $$\begin{aligned}
     f_{X+Y}(z)=\int_{-\infty}^{\infty}f(x,z-x)\mathrm{dx}
    \end{aligned}$$
  * 若此时X和Y还相互独立，设(X,Y)的边缘概率密度分别为$f_X(x),f_Y(y)$，则
    $$\begin{aligned}
     f_{X+Y}(z)=\int_{-\infty}^{\infty}f_X(z-y)f_Y(y)\mathrm{dy}
    \end{aligned}$$
    $$\begin{aligned}
     f_{X+Y}(z)=\int_{-\infty}^{\infty}f_X(x)f_Y(z-x)\mathrm{dx}
    \end{aligned}$$
    这两个公式称为$f_X(x),f_Y(y)$的**卷积公式**，记为$f_X*f_Y$
    $$\begin{aligned}
     f_X*f_Y &=\int_{-\infty}^{\infty}f_X(z-y)f_Y(y)\mathrm{dy} \\
     &=\int_{-\infty}^{\infty}f_X(x)f_Y(z-x)\mathrm{dx}
    \end{aligned}$$
  * **有限个相互独立的正态随机变量的线性组合仍然服从正态分布**
  * $\Gamma$分布
    设有n个相互独立的随机变量$X_i$，$X_i$服从参数为$\alpha_i,\beta$(>0)的$\Gamma$分布，则Z=$\sum_{i=1}^{n}X_i$服从参数为$\sum_{i=1}^{n}\alpha_i,\beta$的$\Gamma$分布，**这一性质称为$\Gamma$函数的可加性**
    $$f_{X_i}(x)=\begin{cases}
     \frac{1}{\beta^{\alpha_i}\Gamma(\alpha_i)}x^{\alpha_i -1}e^{\frac{-x}{\beta}}  \quad x>0\\
     0 \quad else
    \end{cases}$$
* Z=XY分布和Z=$\frac{Y}{X}$分布
  $$\begin{aligned}
   f_{\frac{Y}{X}}(z)=\int_{-\infty}^{\infty}|x|f(x,xz)\mathrm{dx}
  \end{aligned}$$
  $$\begin{aligned}
   f_{XY}(z)=\int_{-\infty}^{\infty}\frac{1}{|x|}f(x,\frac{z}{x})\mathrm{dx}
  \end{aligned}$$
  当X,Y相互独立时，参照上面拆解为两个边缘密度的积函数即可
* $M=\max(X,Y),N=\min(X,Y)$的分布
  * $X_i$为n个相互独立的变量  
  $$\begin{equation}
  F_{max}(z)=\prod_{i=1}^{n}F_{X_i}(z)
  \end{equation}$$

  $$\begin{equation}
  F_{min}(z)=1-\prod_{i=1}^{n}[1-F_{x_i}(z)]
  \end{equation}$$

## 随机变量的数字特征
### 数学期望
- **定义**
  设**离散型随机变量**X的分布律为
  $$\begin{equation}
  P(X=x_k)=p_k ,\quad k=1,2,\cdots
  \end{equation}$$
  若级数$\sum_{k=1}^{\infty}x_kp_k$绝对收敛，则称该级数的和为随机变量X的**数学期望**，记为E(X).即
  $$\begin{equation}
  E(X)=\sum_{k=1}^{\infty}x_kp_k
  \end{equation}$$
  设**连续型随机变量**X的概率密度为f(x)，若积分
  $$\begin{aligned}
  \int_{-\infty}^{\infty}xf(x)\mathrm{dx}
  \end{aligned}$$
  绝对收敛，则称该积分的值为随机变量X的**数学期望**，记为E(X),即
  $$\begin{equation}
  E(X)=\int_{-\infty}^{\infty}xf(x)\mathrm{dx}
  \end{equation}$$
- 数学期望简称**期望**，又称为**均值**
- 几种分布的数学期望表征式
  1. 均匀分布的数学期望为
     $$\begin{equation}
     E(x)=\int_{a}^{b}x\frac{1}{b-a}\mathrm{dx}=\frac{a+b}{2}
     \end{equation}$$
  2. 指数分布的数学期望为
     $$\begin{equation}
     \int_{0}^{\infty}x\frac{1}{\theta}e^{-(\frac{x}{\theta})}\mathrm{dx}=\theta
     \end{equation}$$
  3. 泊松分布的概率密度
     $$\begin{equation}
     E(X)=\sum_{k=1}^{\infty}k\frac{\lambda^{k}e^{-\lambda}}{k!}=\lambda
     \end{equation}$$
  4. 二项分布的数学期望为
     $$\begin{equation}
     E(X)=\sum_{k=0}^{\infty}kC_{n}^{k}p^k(1-p)^{n-k}=np
     \end{equation}$$
  5. 正态分布的数学期望为
     $$\begin{equation}
     E(X)=\int_{-\infty}^{\infty}x\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{(x-u)^2}{2\sigma^2}}\mathrm{dx}=u
     \end{equation}$$
- **定理**
   设Y是随机变量X的函数：Y=g(X),g是连续函数
   1. 若X是离散型随机变量，它的分布律为$P(X=x_k)=p_k$,若$\sum_{k=1}^{\infty}g(x_k)p_k$绝对收敛，则有
    $$\begin{equation}
    E(Y)=\sum_{k=1}^{\infty}g(x_k)p_k
    \end{equation}$$
   2. 如果X是连续型随机变量，它的概率密度为f(x)，若
      $$\begin{aligned}
       \int_{-\infty}^{\infty}g(x)f(x)\mathrm{dx}
      \end{aligned}$$ 
      绝对收敛，则有
      $$\begin{equation}
      E(Y)=\int_{-\infty}^{\infty}g(x)f(x)\mathrm{dx}
      \end{equation}$$
   定理表明在计算数学期望E(Y)时，我们不必算出Y的分布律或概率密度，只需要利用X的分布律或概率密度就可以了
   上述定理可以推广为多个随机变量的函数的情况 
   设Z是随机变量$x_i,i=1,2,\cdots,k$的函数$Z=g(x_i),i=1,2,\cdots,k$，g是连续函数，那么Z是一个一维随机变量.若多维随机变量的概率密度为$f(x_i),i=1,2,\cdots,k$,则有(利用Einstein求和省略)
   $$\begin{equation}
   E(Z)=(\int_{-\infty}^{\infty})\_ig(x_i)f(x_i)dx_i
   \end{equation}$$
   例如对于连续型二维随机变量(X,Y),假设满足绝对收敛
   $$\begin{equation}
   E(Z(X,Y))=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}g(x,y)f(x,y)\mathrm{dx}\mathrm{dy}
   \end{equation}$$
   例如对于离散型二维随机变量(X,Y)，假设满足绝对收敛
   $$\begin{equation}
   E(Z)=\sum_{j=1}^{\infty}\sum_{i=1}^{\infty}g(x_i,y_i)p_{ij}
   \end{equation}$$
- **数学期望的几个重要性质**
  以下假设随机变量的数学期望存在
  1. 设C是常数，则E(C)=C
  2. 设X是一个随机变量，C是常数，则E(CX)=CE(X)
  3. 设X，Y是两个随机变量，则E(X,Y)=E(X)+E(Y)，此结论可推广到任意有限个随机变量
  4. 设X,Y是相互独立的随机变量，则E(XY)=E(X)E(Y)，此结论可推广到任意有限个相互独立的随机变量

### 方差
- **定义**  
  设X是一个随机变量，若$E([X-E(X)]^2)$存在，则称$E([X-E(X)]^2)$为X的**方差**，记为D(X)或Var(X)，即
  $$\begin{equation}
  D(X)=E([X-E(X)]^2)
  \end{equation}$$
  方差是衡量随机变量X取值分散程度的一个尺度
  在应用上我们还引入**均方差**的概念，也称为**标准差**，记为$\sigma(X)$,$\sigma(x)=\sqrt{D(X)}$
- 方差实际上就是随机变量X的函数$g(X)=(X-E(X))^2$的数学期望
  对于离散型随机变量
  $$\begin{equation}
  D(X)=\sum_{k=1}^{\infty}[x_k-E(x)]^2p_k
  \end{equation}$$
  对于连续型随机变量
  $$\begin{equation}
  D(X)=\int_{-\infty}^{\infty}[X-E(X)]^2f(x)\mathrm{dx}
  \end{equation}$$
- 随机变量X的方差可按照如下公式计算
  $$\begin{equation}
  D(X)=E(X^2)-[E(X)]^2
  \end{equation}$$
  
- **几种常用的概率分布表**
  | 分布 | 参数 | 分布律或概率密度 | 数学期望 | 方差 |
  |:---: |:---: | :-------------: | :-----: |:---: |
  |(0-1)分布|0<p<1|P{X=k}=$p^k(1-p)^{1-k}$,k=0,1| p |p(1-p)|
  |二项分布|0<p<1|P{X=k}=$C_n^kp^k(1-p)^{n-k},k=0,1,2,\cdots,n$| np | np(1-p) |
  |帕斯卡分布|0<p<1|P{X=k}=$C_{k-1}^{r-1}p^r(1-p)^{k-r}.k=r,r+1,\cdots$| $\frac{r}{p}$ | $\frac{r(1-p)}{p^2}$ |
  |几何分布|0<p<1|P{X=k}=$(1-p)^{k-1}p,k=1,2,\cdots$| $\frac{1}{p}$ | $\frac{1-p}{p^2}$|
  |超几何分布|N,M,n,$(M\le N),(n\le N)$|P{X=k}=$\frac{C_M^kC_{N-M}^{n-k}}{C_N^k}$|$\frac{nM}{N}$|$\frac{nM}{N}(1-\frac{M}{N})(\frac{N-n}{N-1})$|
  |泊松分布|$\lambda>0$|P{X-k}=$\frac{\lambda^ke^{-\lambda}}{k!},k=0,1,\cdots$|$\lambda$|$\lambda$|
  |均匀分布|a<b|$$f(x)=\begin{cases}\frac{1}{b-a},a<x<b \\\\ 0 ,else\end{cases}$$|$\frac{a+b}{2}$|$\frac{(b-a)^2}{12}$|
  |正态分布|$\mu,\sigma>0$|$f(x)=\frac{1}{\sqrt{2\pi}\sigma}e^{\frac{(x-\mu)^2}{2\sigma^2}}$|$\mu$|$\sigma^2$|
  |$\Gamma$分布|$\alpha>0,\beta>0$|$$f(x)=\begin{cases} \frac{1}{\beta\Gamma(\alpha)}x^{\alpha-1}e^{-\frac{x}{\beta}},x>0 \\\\ 0,else \end{cases}$$|$\alpha\beta$|$\alpha\beta^2$|
  |指数分布|$\theta>0$|$$\begin{cases}\frac{1}{\theta}e^{-\frac{x}{\theta}},x>0 \\\\ 0,else \end{cases}$$|$\theta$|$\theta^2$|


- **方差的重要性质**
  1. 设C是常数，则D(C)=0
  2. 设X是随机变量，C是常数，则$D(CX)=C^2D(X),\quad D(X+C)=D(X)$
  3. 设X,Y是两个随机变量，则有
     $$\begin{aligned}
      D(X\pm Y)=D(X)+D(Y)\pm 2E[(X-E(X))(Y-E(Y))]
     \end{aligned}$$
     特别地，当X,Y相互独立时
     $$\begin{aligned}
      D(X\pm Y)=D(X)+D(Y)
     \end{aligned}$$
     这一性质可以推广到任意有限多个互相独立的随机变量之和的情况
  4. D(X)=0的**充要条件**是X以概率1取常数E(X)，即
     $$\begin{aligned}
      P(X=E(x))=1
     \end{aligned}$$   
  5. 这一点不是方差的性质，但他很重要，故将此归入.
     n个相互独立的正态分布的线性组合仍然是正态分布，组合后得到的正态分布的期望与方差可完全由组成部分的期望和方差确定
     $$\begin{aligned}
      Z=C_1X_1+C_2X_2+\cdots+C_nX_n\quad 服从N(\sum_{i=1}^{n}C_iu_i,\sum_{i=1}^{n}C_i^2\sigma_i^2)
     \end{aligned}$$
  
- **切比雪夫不等式**
  设随机变量X具有数学期望$E(X)=\mu$,方差$D(X)=\sigma^2$，则对于任意整数$\varepsilon$，下面的不等式成立
  $$\begin{equation}
  P(|X-\mu|\ge \varepsilon)\le \frac{\sigma^2}{\varepsilon^2}
  \end{equation}$$
  这一不等式称为**切比雪夫不等式**，切比雪夫不等式也可以写成如下形式
  $$\begin{equation}
  P(|X-\mu|<\varepsilon)\ge 1-\frac{\sigma^2}{\varepsilon^2}
  \end{equation}$$

### 协方差与相关系数
- 在前面讲述方差的时候，我们说对于随机变量X,Y有
  $$\begin{equation}
  D(X\pm Y)=D(X)+D(Y)\pm 2E[(X-E(X))(Y-E(Y))]
  \end{equation}$$
  如果随机变量X,Y是相互独立的，则有
  $$\begin{aligned}
   E[(X-E(X))(Y-E(Y))]=0
  \end{aligned}$$
  **需要注意的是，若随机变量X,Y相互独立，则上式必定成立；但上式成立不足以说明随机变量X,Y相互独立.这意味这该条件对于变量的相互独立性，是充分不必要的**
- 定义
  量E{(X-E(X))(Y-E(Y))}称为随机变量X与Y的**协方差**，记为Cov(X,Y)，即
  $$\begin{equation}
  Cov(X,Y)=E[(X-E(X))(Y-E()Y)]
  \end{equation}$$
  而
  $$\begin{equation}
  \rho_{XY}=\frac{Cov(X,Y)}{\sqrt{D(X)}\sqrt{D(Y)}}
  \end{equation}$$
  称为随机变量X与Y的**相关系数**
  将协方差按照定义展开就可得到协方差计算公式
  $$\begin{equation}
  Cov(X,Y)=E(XY)-E(X)E(Y)
  \end{equation}$$
- **协方差的性质**
  1. $Cov(X,Y)=Cov(Y,X),\quad Cov(X,X)=D(X)$
  2. $Cov(aX,bY)=abCov(X,Y)$, a,b是常数
  3. $Cov(X_1+X_2,Y)=Cov(X_1,Y)+Cov(X_2,Y)$
- **相关系数的性质**
  考虑以X的线性函数a+bX来近似表示Y，我们以均方误差
  $$\begin{equation}
  e=E[(Y-(a+bX))^2]
  \end{equation}$$
  来衡量近似表达的好坏程度,e的值越小表示近似程度越好，最佳近似为
  $$\begin{equation}
  \min e=\min E[(Y-(a+bX))^2]=(1-\rho_{XY}^2)D(Y)
  \end{equation}$$
  由此我们可以得到下述定理
  1. $|\rho_{X,Y}\le 1|$
  2. $|\rho_{XY}=1|$的**充要条件**是存在常数a,b使得P{Y=a+bX}=1
- 根据上面的讲述，不难看出均方误差e是相关系数的严格单调递减函数.当相关系数大时，即均方误差小，表示X,Y的联系紧密，特别地，当相关系数为1时，定理2表明，X与Y之间以概率1存在着线性关系.**当相关系数为零时，称X与Y不相关**
- **当随机变量X，Y相互独立时，他们的协方差为零，因此相关系数为零，即X，Y不相关；但若X，Y不相关，X和Y却不一定相互独立.这是因为不相关是就随机变量X，Y的线性关系而言的，而相互独立是就一般关系而言的.但若X,Y服从二维正态分布时，X和Y不相关与X和Y相互独立是等价的**
  

### 矩、协方差矩阵
- 定义
  设X，Y是随机变量，若
  $$\begin{equation}
  E(X^k),\quad k=1,2,\cdots
  \end{equation}$$
  存在，称它为X的**k阶原点矩**，简称k阶矩
  若
  $$\begin{equation}
  E([X-E(x)]^k),\quad k=2,3,\cdots
  \end{equation}$$
  存在，称它为X的**k阶中心矩**
  若
  $$\begin{equation}
  E(X^kY^l),\quad k,l=1,2,\cdots
  \end{equation}$$
  存在，称它为X和Y的**k+l阶混合矩**
  若
  $$\begin{equation}
  E[(X-E(X))^k(Y-E(Y))^l],\quad k,l=1,2,\cdots
  \end{equation}$$
  存在，称它为X和Y的**k+l阶混合中心矩**
  显然，X的数学期望是一阶原点矩，方差是2阶中心距，协方差是X和Y的二阶混合中心矩
- **协方差矩阵**
  二维随机变量$(X_1,X_2)$有四个二阶中心矩，(我们设他们都存在),分别记为
  $$\begin{aligned}
   c_{11}=E[(X_1-E(X_1))^2] \\\\
   c_{12}=E[(X_1-E(X_1))(X_2-E(X_2))]\\\\
   c_{21}=E[(X_2-E(X_2))(X_1-E(X_1))]\\\\
   c_{22}=E[(X_2-E(X_2))^2]
  \end{aligned}$$
  将他们排成矩阵形式
  $$\begin{pmatrix}
  c_{11} & c_{12} \\\\
  c_{21} & c_{22} 
  \end{pmatrix}$$
  这个矩阵称为随机变量$(X_1,X_2)$的**协方差矩阵**
  设n维随机变量$(X_1,X_2,\cdots,X_n)$的二阶混合中心矩都存在
  $$\begin{aligned}
   c_{ij}=Cov(X_i,X_j)=E[(X_i-E(X_i))(X_j-E(X_j))],\quad i,j=1,2,\cdots,n
  \end{aligned}$$
  则称矩阵
  $$C=\begin{pmatrix}
  c_{11}&c_{12}&\cdots&c_{1n}\\\\
  c_{21}&c_{22}&\cdots&c_{2n}\\\\
  \vdots&\vdots& &\vdots \\\\
  c_{n1}&c_{n2}&\cdots&c_{nn}
  \end{pmatrix}$$
  为n维随机变量的**协方差矩阵**，由于$c_{ij}=c_{ji},i\neq j$,因此上述矩阵是一个对称矩阵




  $$\begin{equation}\end{equation}$$

  $$\begin{equation}\end{equation}$$
  $$\begin{equation}\end{equation}$$
    


