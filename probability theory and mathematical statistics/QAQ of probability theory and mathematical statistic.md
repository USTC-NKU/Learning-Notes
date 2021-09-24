---
title: QAQ of probability theory and mathematical statistic
math: true
tags: Summary of PTMS
categories: Probability Theory and Mathematical Statistics
---
[toc]
本文将综合总结概率论、数理统计、时间序列、回归分析、多元统计等内容的核心概念

* * *

**1、概率空间的定义？（+++++）** 三元体$(\Omega, \mathcal{F}, P)$构成一个概率空间。其中：

*   (1) 样本空间$\Omega$：是样本点$w$的全体
*   (2) 事件域$\mathcal{F}$：$\Omega$中某些满足下列条件的子集的全体构成的**集类**（$sigma$\-代数/$sigma$\-域）：

*   (a) $\Omega\in\mathcal{F}, \emptyset\in\mathcal{F}$；
*   (b) 封闭性：若$A\in\mathcal{F}$，则$\bar{A}\in\mathcal{F}$；
*   (c) 可数次运算下封闭：若$A_1,...,A_n,...\in\mathcal{F}$，则$\bigcup_{n=1}^\infty A_n\in\mathcal{F}$

  

*   (3) 概率P：定义在$\mathcal{F}$上的实值**函数**：$A(\in\mathcal{F})\rightarrow P(A)$，并满足下列条件（概率公理，概率是定义在$sigma$\-代数上的规范化测度）：

*   (a) 非负性：对任一$A\in\mathcal{F}$，$P(A)\geq 0$
*   (b) 规范性：$P(\Omega)=1, P(\emptyset)=0$
*   (c) 可列可加性：若$A_1,...,A_n,...$是两两互不相容的事件，则$P(\sum_{n=1}^\infty A_n)=\sum_{n=1}^\infty P(A_n)$

**2、由概率的定义能推出哪些概率的运算性质？（+++）**

*   (1) $P(\bar{A})=1-P(A)$
*   (2) $B\subset A, P(A-B)=P(A)-P(B)$
*   (3) 多退少补：$P(A_1\bigcup A_2\bigcup ...\bigcup A_n)=\sum_{i=1}^n P(A_i)-\sum P(A_iA_j)+...+(-1)^{n-1}P(A_1A_2...A_n)$
*   (4) 次可加：$P(\bigcup_{i=1}^\infty A_i)\leq\sum_{i=1}^\infty P(A_i)$
*   (5) 概率测度的连续性：$P(A)=\lim\limits_{n\rightarrow\infty} P(A_n)$

**3、什么是样本空间？什么是样本点？（++）** 样本点是随机试验的每一基本结果，样本空间是样本点的全体

**4、古典概型的定义和基本假设是什么？（+）** 古典概型定义：$p(A)=\frac{m}{n}$，其中m为事件A包含的样本点数，n为样本空间的样本点数。其基本假设是（1）样本空间有限（2）事件等可能

**5、什么是完备事件组？（+）** 事件列满足（1）$A_i$两两不相容且$P(A_i)>0$（2）$\sum_{i=1}^\infty A_i=\Omega$

**6、写出乘法公式/链式法则/全概率公式/贝叶斯公式（++）**

*   乘法公式：$P(AB)=P(A|B)P(B)$
*   链式法则：$P(A_1A_2...A_n)=P(A_1)P(A_2|A_1)P(A_3|A_2A_1)...P(A_n|A_{n-1}...A_1)$
*   全概率公式：$P(B)=\sum_{i=1}^\infty P(A_i)P(B|A_ i)$
*   贝叶斯公式：$P(A_i|B)=\frac{P(A_i)P(B|A_ i)}{\sum_{k=1}^\infty P(A_k)P(B|A_k)}$

**7、n个事件相互独立需要多少个条件？（+）** $2^n-n-1$ （两两独立，三三独立...）

**8、什么是随机变量？（++++）** 一句话版：随机变量是样本点的函数 完整定义：设$\xi(w)$是定义在概率空间$\{\Omega,\mathcal{F},P\}$上的实值函数，且对$R$上的任一波雷尔集$B$，有$\xi^{-1}(B)=\{w:\xi(w)\in B\}\in\mathcal{F}$，就称$\xi(w)$为随机变量，而称$\{P(\xi(w)\in B)\},B\in\mathcal{B}$为随机变量的概率分布。

**9、随机变量与普通变量的区别？（+）** 随机变量具有概率性（本质是定义在样本空间上取值为实数的函数）

**10、叙述泊松定理？泊松定理适用的条件？（+）** 泊松定理：$n\rightarrow\infty$有$np_n\rightarrow\lambda$则$\lim\limits_{n\rightarrow\infty} b(k;n,p)=\frac{\lambda^k}{k!}e^{-\lambda}$，n很大p很小时适用。

**11、分布函数的定义和性质？（+++）** 定义：$F(x)=P(\xi\leq x), -\infty< x< \infty$；性质：单调不减，右连续，极限负端0正端1

**12、密度函数的定义和性质？（+++）** 定义：非负可积函数$P(x)$使得分布函数$F(x)$满足：$F(x)=\int^x_{-\infty} p(y)dy, -\infty< x< \infty$；性质：非负性，规范性（全空间积分为1）

**13、数学期望的定义？（+）**

*   离散型：$E\xi=\sum_k x_k p_k$（需要$\sum_k x_k p_k$绝对收敛）
*   连续型：$E\xi=\int_{-\infty}^\infty xp(x)dx$（需要$\int_{-\infty}^\infty|x|p(x)dx<\infty$）
*   一般定义：$\int_{-\infty}^\infty xdF(x)$（需要$\int_{-\infty}^\infty |x|dF(x)<\infty$）

**14、为什么要引入方差？为什么方差是平方的形式？（+）** 方差为了描述随机变量$\xi$取值相对于其期望$E\xi$的离散程度，平方是使得离差$\xi-E\xi$正负抵消

**15、如何判断两个随机变量不相关？（+++）** $r(X,Y)=0$ 或 $Cov(X,Y)=0$ 或 $EXY=EXEY$

**16、什么是特征函数？特征函数的形式？（+）** 设$\xi$为实值随机变量，则$f(t)=Ee^{it\xi},-\infty< t< \infty$为$\xi$的特征函数

*   一般形式：$f(t)=\int_{-\infty}^{\infty} e^{itx}dF(x)$
*   离散形式：$f(t)=\sum_{n=1}^\infty p_n e^{itx_n},-\infty< x<\infty$
*   连续形式：$f(t)=\int_{-\infty}^{\infty} e^{itx}p(x)dx$

**17、为什么要引入特征函数？（+）** 均值、方差等数字特征不能完全确定随机变量的分布，而特征函数既能完全决定分布函数，又具有良好的性质。

**18、为什么特征函数能完全决定分布函数？特征函数与分布函数的关系？（+）** 逆转公式$F(x_2)-F(x_1)=\lim\limits_{T\rightarrow\infty}\frac{1}{2\pi}\int_{-T}^T \frac{e^{-itx_1}-e^{-itx_2}}{it}f(t)dt$推出唯一性定理，f绝对可积时有$p(x)=F'(x)=\frac{1}{2\pi}\int_{-\infty}^{\infty}e^{-itx} f(t)dt$直接决定了密度函数（密度积分得特征函数：傅里叶变换；特征函数积分得密度：逆傅里叶变换）

**19、特征函数与随机变量独立的关系？（+）** 若$\xi_1,...,\xi_n$独立，则$\eta=\xi_1+...+\xi_n$的特征函数为$f_\eta(t)=f_1(t)...f_n(t)$

**20、叙述依分布收敛（++++）** 设$\xi$是一随机变量，$\{\xi_n\}$是一列随机变量，如果$\xi_n$的分布函数弱收敛（每个连续点收敛）于$\xi$的分布函数，则称$\xi_n$依分布收敛与$\xi$

**21、叙述依概率收敛（++++）** 设$\xi$和$\xi_n, n\geq 1$，是定义在同一概率空间$(\Omega,\mathcal{F},P)$上的随机变量，如果对任意$\epsilon>0$，$\lim\limits_{n\rightarrow\infty} P(|\xi_n-\xi|\geq\epsilon)=0$或$\lim\limits_{n\rightarrow\infty} P(|\xi_n-\xi|<\epsilon)=1$，则称$\xi_n$依概率收敛于$\xi$，记作$\xi_n\stackrel{P}\longrightarrow\xi$

**22、依分布收敛\\依概率收敛有哪些性质？（++++）**

*   (1) 依概率

*   (a) 常数$a_n\rightarrow a, b_n\rightarrow b$，$X_n\stackrel{P}\longrightarrow X$，则$a_nX_n+b_n\stackrel{P}\longrightarrow aX+b$
*   (b) $X_n\stackrel{P}\longrightarrow X，Y_n\stackrel{P}\longrightarrow Y$，则：

*   $X_n\pm Y_n\stackrel{P}\longrightarrow X\pm Y$
*   $X_n Y_n\stackrel{P}\longrightarrow XY$
*   $\frac{X_n}{Y_n}\stackrel{P}\longrightarrow \frac{X}{Y}$ (Y≠0)

  

*   (c) $X_n\stackrel{P}\longrightarrow X$，f连续则$f(X_n)\stackrel{P}\longrightarrow f(X)$

*   (2) 依概率到依分布

*   (a) 对常数，$X_n\stackrel{P}\longrightarrow c \Leftrightarrow X_n \stackrel{d}\longrightarrow c$
*   (b) 若$X_n\stackrel{P}\longrightarrow X$，则$X_n\stackrel{d}\longrightarrow X$
*   (c) 若$X_n-Y_n\stackrel{P}\longrightarrow 0$，$X_n\stackrel{d}\longrightarrow X$，则$Y_n\stackrel{d}\longrightarrow X$
*   (d) 若$Y_n\stackrel{P}\longrightarrow c, X_n\stackrel{d}\longrightarrow X$则$X_nY_n\stackrel{d}\longrightarrow cX$

  

*   (3) 依分布收敛

*   (a) 常数$a_n\rightarrow a, b_n\rightarrow b$，$X_n\stackrel{d}\longrightarrow X$，则$a_nX_n+b_n\stackrel{d}\longrightarrow aX+b$
*   (b) $X_n\stackrel{d}\longrightarrow X$，f连续则$f(X_n)\stackrel{d}\longrightarrow f(X)$

**23、叙述大数定律（+++++）**

*   伯努利大数定律：设$\{\xi_n\}$是一列独立同分布的随机变量，$P(\xi_n=1)=p,P(\xi_n=0)$，记$S_n=\sum_{i=1}^n \xi_i$，则$\frac{S_n}{n}\stackrel{P}\longrightarrow p$
*   辛钦大数定律：设$\{\xi_n\}$是定义在概率空间$(\Omega,\mathcal{F},P)$上的独立同分布的随机变量序列，$E|\xi_1|<\infty$，记$\mu=E\xi_1,S_n=\sum_{k=1}^n\xi_k$，则$\{\xi_n\}$服从弱大数定律，即$\frac{S_n}{n}\stackrel{P}\longrightarrow\mu$
*   切比雪夫大数定律：设$\{\xi_n\}$是定义在概率空间$(\Omega,\mathcal{F},P)$上的随机变量序列，$E\xi_n=\mu_n, Var\xi_n=\sigma_n^2$，如果$\sum_{k=1}^n\sigma^2_k/n^2\rightarrow 0$，则$\{\xi_n\}$服从弱大数定律，即$\frac{1}{n}\sum_{k=1}^n\xi_k-\frac{1}{n}\sum_{k=1}^n\mu_k\stackrel{P}\longrightarrow 0$

**24、对比几个大数定律不同使用条件（+++++）**

*   伯努利：独立二项分布，期望方差相同
*   辛钦：独立同分布
*   切比雪夫：独立，期望方差存在

**25、叙述中心极限定理（+++++）**

*   德莫夫-拉普拉斯中心极限定理：设$\Phi(x)$为标准正态分布的分布函数，对$-\infty< x<\infty$有：

$\lim\limits_{n\rightarrow\infty} P(\frac{S_n-np}{\sqrt{np(1-p)}}\leq x)=\Phi(x) \\$

*   林德贝格-勒维中心极限定理：设$\{\xi_n\}$是一列独立同分布的随机变量，记$S_n=\sum_{k=1}^n\xi_k$，$E\xi_1=\mu$，$Var\xi_1=\sigma^2$，则中心极限定理成立，即

$\frac{S_n-n\mu}{\sqrt{n}\sigma}\stackrel{d}\longrightarrow N(0,1) \\$

**26、不同中心极限定理适用的条件？（++++）** 德莫夫-拉普拉斯是二项分布，林德贝格-勒维是任意独立同分布随机变量

**27、概率论中有哪些重要的不等式？（++++）**

*   柯西-施瓦兹不等式：$|EXY|^2\leq EX^2 EY^2$（等价形式：$Cov(X,Y)\leq\sqrt{VarX VarY}$）
*   切比雪夫不等式：$P(|X-EX|\geq \epsilon)\leq\frac{VarX}{\epsilon^2}$
*   马尔科夫不等式：$f$在$[0,\infty)$非负单调不减，$P(|\xi|>x)\leq\frac{Ef(|\xi|)}{f(x)}$

**28、林德贝格-勒维中心极限定理的证明？（++++）** $\frac{S_n-n\mu}{\sqrt{n}\sigma}$的特征函数+泰勒展开，收敛到标准正态分布的特征函数

**29、如何应用中心极限定理生产正态分布随机数？（+）** 生成一系列$\{\xi_k\}^n_{k=1}\sim U(0,1)$，由均匀分布$E\xi_k=0.5, Var\xi_k=\frac{1}{12}$，则n稍大时$\eta=\frac{\sqrt{12}(\sum_{k=1}^n\xi_k-\frac{n}{2})}{\sqrt{n}}$可以看做服从正态分布的随机变量

**30、辛钦大数律的证明？（++++）** $\frac{S_n}{n}$的特征函数+泰勒展开，收敛到单点退化分布的特征函数

**31、大数律和中心极限定理的区别？（+++++）** 两个定律都是在说样本均值性质。随着n增大，大数定律：样本均值几乎必然等于均值。CLT：样本均值服从以总体均值为期望，总体方差为方差的正态分布。

**32、概率论和数理统计思想的区别？（++）** 概率论从总体（模型）预测样本，数理统计从样本推断总体（模型）

**33、有哪些分布具有可加性？（+++）** 正态分布的两个参数，二项分布的n，泊松分布的$\lambda$，Gamma分布的n，卡方分布的n

**34、样本的两重性指什么？（++）** 样本在抽样前是随机变量，抽样后是具体的数

**35、什么是简单随机样本？什么是抽样分布？（+）** 简单随机样本：相互独立，相同分布（抽出时是随机的）；统计量的概率分布叫抽样分布

**36、什么是统计量？统计量的特点？（+++）** 由样本算出的量，是样本的函数；两个特点：与样本有关与参数无关，也具有两重性

**37、数理统计中参数的含义？什么是参数空间？什么是样本分布族？（+）**

*   参数：样本分布中的未知常数
*   参数空间：参数的取值范围
*   样本分布族：$\mathcal{F}=\{f(x,\theta):\theta\}$（参数的每一个取值对应一个具体分布）

**38、经验分布函数的性质有哪些？（++）** 是仅依赖于样本的函数，是统计量。单调，非降，左连续

**39、叙述格里汶科定理？这个定理说明了什么？（+）** 定理：$F(x)$为分布函数，记$D_n=sup_{-\infty< x<\infty}|F_n(x)-F(x)|$，则有$P(\lim\limits_{n\rightarrow\infty}D_n=0)=1$。说明n足够大，经验分布函数与理论分布函数只有很小的差别

**40、写出指数族的定义（+++）** 分布族$\mathcal{F}=\{f(x,\theta):\theta\in\Theta\}$，若密度函数可写为$f(x,\theta)=C(\theta)exp(\sum_{i=1}^k Q_i(\theta)T_i(x))h(x)$形式，则为指数分布族。其中$C,Q$为参数空间上的函数，$T,h$为样本空间上的函数

**41、什么是充分统计量？（++++）** 统计量$T(X)$已知，样本的条件分布于参数$\theta$无关

**42、什么是完全统计量？（+）** $T=T(X)$为充分统计量，若对任意满足$E_\theta[\psi(T(X)]=0$的$\psi(T(X))$有$P_\theta(\psi(T(X))=0)=1, \forall \theta\in\Theta$，则$T(X)$为完全统计量。

**43、叙述因子分解定理。这个定理说明了什么？（++）** 样本$X=(X_1,...,X_n)$的$f(x,\theta)$依赖$\theta$，$T=T(X)$为统计量，则$T$为充分统计量$\Leftrightarrow$$f(x,\theta)=g(t(x),\theta)h(x)$，说明样本可以仅通过充分统计量与参数发挥作用

**44、评价统计量优劣的指标有哪些？（++++）** 小样本：无偏性，有效性；大样本：相合性，渐进正态性；一般：均方误差

**45、点估计量和点估计值的区别？（++）** 点估计量是样本的函数$T(x_1,...,x_n)$，点估计值是将样本点带入函数$T$后得到的具体的值

**46、什么是相合估计？叙述弱相合估计、强相合估计、r阶矩相合估计（+）** 相合估计：$\forall n,\hat{g}_n(X)\stackrel{P}\longrightarrow g(\theta),(n\rightarrow\infty)$

*   $\lim\limits_{n\rightarrow\infty}P_\theta(|\hat{g}_n(X)-g(\theta)|\geq\epsilon)=0$：弱相合估计
*   $P_\theta(\lim\limits_{n\rightarrow\infty}\hat{g}_n(X)=g(\theta))=1$：强相合估计
*   $\lim\limits_{n\rightarrow\infty}E_\theta|\hat{g}_n(X)-g(\theta)|^r=0$：r阶矩相合估计（r=2均方相合）

**47、矩估计的基本思想？矩估计量的性质如何？（++）** 思想：将待估参数表示为总体分布某些矩的函数，并用样本矩估计总体矩。性质：小样本无偏，大样本相合且渐进正态

**48、什么是似然原理？什么是似然函数？什么是极大似然估计？（+++++）**

*   似然原理：随机试验最可能出现的结果中是该试验所有可能结果中概率最大的那一种
*   似然函数：样本$x$固定时，把概率函数$f(x,\theta)$看成$\theta$的函数。
*   极大似然估计：统计量$\hat{\theta}^*=\hat{\theta}^*(X)$，满足$L(\hat{\theta}^*,x)=sup_{\theta\in\Theta}L(\theta,x),x\in\mathcal{X}$（寻找某个参数使得能样本出现的概率最大）

**49、极大似然估计的特性？（++）** 不一定是无偏的；可以表示为充分统计量的函数；MLE不变性（$g(T(x))$是$g(\theta)$的MLE）

**50、叙述Rao-Blackwell定理，这个定理的意义何在？（+++）** 定理：设$T=T(\mathbf{X})$是一个充分统计量，而$\hat{g}(\mathbf{X})$是$g(\theta)$的一个无偏估计，则$h(T)=E(\hat{g}(\mathbf{X})|T)$是$g(\theta)$的无偏估计，并且$D_\theta(h(T))\le D_\theta(\hat{g}(\mathbf{X}))$对一切$\theta\in\Theta$成立，其中等号当且仅当$P_\theta(\hat{g}(\mathbf{X})=h(T))=1成立$。意义在于说明了对无偏估计在充分统计量的条件下求期望，可以改善这个无偏估计的方差

**51、叙述Lehmann-Scheff定理（+）** 设$X\sim\{f(x,\theta),\theta\in\Theta\}$，$g(\theta)$为参数空间$\Theta$上的可估函数，$T(\mathbf{X})$为$\theta$的一个充分完全统计量。若$\hat{g}(T(\textbf{X}))$是$g(\theta)$的一个无偏估计，则$\hat{g}(T(\textbf{X}))$是$g(\theta)$的唯一UMVUE。

**52、叙述UMVUE构造的过程？（+++）**

*   方法一：先找一个充分完备统计量$T(X)$，再找一个待估参数的无偏估计$\psi$，计算$E[\psi|T]$就得到UMVUE。
*   方法二：先找一个充分完备统计量$T(X)$，再找一个$T$的函数$g(T(X))$，使得它是待估参数的无偏估计，$g(T(X))$即为所求UMVUE。

**53、无偏估计的效率是如何定义的？什么是有效估计？（+）** 无偏估计$\hat{g}(X)$的效率：$e_{\hat{g}(\theta)}=\frac{(g'(\theta))^2/nI(\theta)}{D_\theta(\hat{g}(X))}$，$I(\theta)$为Fisher信息量

*   有效估计：$e_{\hat{g}(\theta)}=1$
*   渐进有效估计：$\lim\limits_{n\rightarrow\infty}e_{\hat{g}(\theta)}=1$

**54、C-R不等式及其使用的条件？为什么需要这个不等式？（+）** $Var_\theta(\hat{g})\geq\frac{g'(\theta)^2}{nI(\theta)}$，$I(\theta)$为Fisher信息量。该不等式仅适用于正则分布族。用于估计**无偏估计类**中估计量的方差下界，用途之一为判断UMVUE（达到下界一定是UMVUE，未达到不一定不是UMVUE）

**55、什么是Fisher信息量？Fisher信息量代表什么？（++）** Fisher信息量：$I(\theta)=E_\theta(\frac{\partial}{\partial\theta}log f(X,\theta))^2$，反映了总体分布的性质，$I(\theta)$越大，总体提供关于参数的信息越多，参数越容易估计

**56、区间估计和假设检验中$\alpha$含义相同吗？（++++）** 不相同。区间估计是找到一个随机区间，使得区间包含真实参数的概率等于一个固定的值$1-\alpha$，这个值为置信水平；假设检验是去判断某个假设是否真实，使得在原假设真实的情况下，犯错的概率等于一个固定的值$\alpha$，这个值为显著性水平

**57、区间估计和假设检验的思想/假设有什么不同？（+++++）** 区间估计：参数未知，没有对参数进行任何假设，只是计算一个随机区间；假设检验：对参数做出了自己的假设，需要利用统计量检验已知的参数是否靠谱

**58、枢轴量和检验统计量的区别？（+++++）** 枢轴量的表达式与待估参数$\mu$有关，枢轴量的分布与待估参数$\mu$无关（枢轴量是样本和待估参数的函数）；统计量只与样本有关（统计量是样本的函数）

**59、置信度与精度的区别？（++++）** 置信度：随机区间包含真实参数的概率；精度：随机区间的平均长度。给定样本量，则置信度与精度互相制约。

**60、什么是区间估计？（+++）** 设$X$为$f(x,\theta)$取出的样本，令$\hat{g}_1(X),\hat{g}_2(X)$为$\mathcal{X}$上$\Theta$的两个统计量，$\hat{g}_1(X)\leq\hat{g}_2(X)$，则称$[\hat{g}_1(X),\hat{g}_2(X)]$为$g(\theta)$的一个区间估计。

**61、置信水平和置信系数的区别？（++++）**

*   置信水平：$\theta$的区间估计$[\hat{g_1},\hat{g_2}]$包含$\theta$的概率$P_\theta(\hat{\theta_1}\leq\theta\leq\hat{\theta_2})$
*   置信系数：置信水平在参数空间$\Theta$的下确界$inf_{\theta\in\Theta}P_\theta(\hat{\theta_1}\leq\theta\leq\hat{\theta_2})$

**62、给出置信水平为$1-\alpha$的置信空间的定义（+++）** 对给定$0<\alpha<1, P_\theta(\hat{\theta_1}(X)\leq\theta\leq\hat{\theta_2}(X))\geq 1-\alpha,\theta\in\Theta$，则$[\hat{\theta_1}(X),\hat{\theta_2}(X)]$是$\theta$的置信水平为$1-\alpha$的置信空间。

**63、什么是拒绝域？（+++）** 拒绝域是样本的集合，由样本空间中一切使得假设被拒绝的样本构成

**64、两类错误的区别？（+++++）** 第一类错误；观察值落入拒绝域误将H0否定；第二类错误：观察值落入接受域误将H0接受

**65、什么是检验函数？（+++）** 检验函数：表示有了样本之后否定$H_0$的概率$$\\psi(x)=\\begincases}1, \\bar{x-a\_0|>A\\ 0, |\\barx}-a\_0\\leq A\\end{cases$$

**66、什么是势函数/功效函数？势函数与两类错误之间的关系？（+++）** 设$\psi(x)$是$H_0:\theta\in\Theta_0\leftrightarrow H_1:\theta\in\Theta_1$的一个检验函数，则$\beta_\psi(\theta)=P_\theta\{用检验\psi否定了H_0\}=E_\theta[\psi(X)],\theta\in\Theta$称为$\psi$的功效函数。

*   第一类错误：$\alpha(\theta)=P(\tilde{X}\in D|H_0为真)=P_\theta(\tilde{X}\in D)$

$\alpha(\theta)=\begin{cases}\beta_\psi(\theta),&amp;\theta\in\Theta_0\\ 0,&amp;\theta\in\Theta_1\end{cases}\\$

*   第二类错误：$\beta(\theta)=P(\tilde{X}\in\bar{D}|H_1为真)=P_\theta(\tilde{X}\in\bar{D})$

$\beta(\theta)=\begin{cases}0,&amp; \theta\in\Theta_0,\\ 1-\beta_\psi(\theta),&amp;\theta\in\Theta_1\end{cases}\\$

**67、什么是显著性水平为$\alpha$的检验？（++++）** 设$\psi$为$H_0:\theta\in\Theta_0\leftrightarrow H_1:\theta\in\Theta_1$的一个检验，$0\leq\alpha\leq 1$，若$\psi$犯**第一类错误**的概率不超过$\alpha$，称$\psi$为显著性水平为$\alpha$的检验。

**68、原假设与备择假设的地位是否相同？（++）** 不同：（1）控制第一类错误，不会轻易拒绝原假设 （2）检验统计量分布在原假设条件下已知

**69、显著性水平指什么？为什么需要这个量？什么是NP原则？（+++）** 显著性水平是第一类错误上界，由于不能同时最小化两类错误，因此通常控制第一类错误概率不超过α的前提下最小化第二类错误（NP原则）

**70、p值和α值的区别（+++++）** p值是手上样本出现的客观可能性，α值是心目中小概率的“度”

**71、一句话解释p值？（+++++）** p值是原假设为真时，比手头上样本结果更极端情况出现的概率

**72、p值和$\alpha$值与拒绝原假设的关系？（++）** p越小，原假设越容易被拒绝，$\alpha$反之

**73、什么是拟合优度检验？（+++）** 用样本去检验总体X是否服从分布F

**74、列联表检验可以干什么？（+）** 检验独立性和齐一性

**75、贝叶斯学派和经典统计学派在统计推断中的不同？（+）** 贝叶斯学派用到了总体信息、样本信息和先验信息，而经典统计学派只用到前两种。贝叶斯点估计方法通常用后验分布代替样本分布。

**76、平稳序列需要满足的条件？（++++）** （1）方差有限 （2）均值恒定 （3）自协方差只与时间差有关

**77、什么是白噪声？（++++）** （1）均值恒定 （2）协方差在t≠s时为零（比平稳序列多了一点）

**78、叙述数学期望的三大收敛定理（+）**

*   单调收敛定理：令$(X_n,n\geq 1)$是一列单调不减非负随机变量（$0\leq X_n\leq X_{n+1}\ a.s.$），若$X_n\rightarrow X\ a.s.$，则$\lim\limits_{n\rightarrow\infty}EX_n=EX$。
*   Fatou引理：令$(X_n,n\geq 1)$是一列单调非负随机变量，那么$\lim\limits_{n\rightarrow\infty}EX_n\geq E \lim\limits_{n\rightarrow\infty} X_n$
*   Lebesgue控制收敛定理：令$(X_n,n\geq 1)$是一列随机变量，设存在一个随机变量$Y$，$E|Y|<\infty, |X_n|\leq Y\ a.s.$，若$X_n\rightarrow X\ a.s.$或$X_n\stackrel{P}\longrightarrow X$，则$\lim\limits_{n\rightarrow\infty}EX_n=EX$。

**79、叙述随机变量的Fubini定理（+）** 设对$a\leq t\leq b$，$X(t)$是随机变量，若$\int_a^b E(|X(t)|)dt<\infty$或对所有$a\leq t\leq b$，$X(t)$都非负，则$E[\int_a^b X(t)dt]=\int_a^b E(X(t))dt$

**80、什么是随机过程？（++）** 设$(\Omega,A,P)$为概率空间，$T$为指标集，$\epsilon$为点集，称一随机变量$X(w,t): \Omega\rightarrow\epsilon,t\in T$为随机过程，记作$X=(X(t),t\in T)$，其中$t\in T$为时间参数空间。

**81、什么是样本曲线？（++）** 任给一个$w\in\Omega$，称$X(w,.): T\rightarrow\epsilon$为样本曲线（或随机过程的一次具体观测就是样本曲线）

**82、什么是宽平稳？什么是严平稳？二者的区别？（++++）** 宽：均值恒定，自协方差只与t-s有关；严：不同t同分布（即$(X(t_1+t),X(t_2+t),...,X(t_k+t))\stackrel{d}{=}(X(t_1),X(t_2),...,X(t_k))$）

**83、什么是平稳增量？什么是独立增量？什么是正态过程？（+）**

*   平稳增量：增量$X(t)-X(s)$的分布仅依赖于时间差$t-s$，而与$s$和$t$无关
*   独立增量：对$\forall k\geq 1,t_1< t_2<...< t_k$，增量$X(t_1),X(t_2)-X(t_1),...,X(t_k)-X(t_{k-1})$独立
*   正态过程：任意有限维分布为联合正态分布

**84、什么是泊松过程？（+++）** （1）连续时间，取值非负的随机过程（2）初值零：N(0)=0 （3）独立、平稳增量且$N(t)\sim P(\lambda t)$ （4）满足稀有性条件

**85、参数为$\lambda t$的泊松过程均值、方差、特征函数？（+）** $EN(t)=\lambda t, Var(N(t))=\lambda t, Ee^{ixN(t)}=e^{\lambda t(e^{ix}-1)}$

**86、泊松过程与其他分布有哪些关系？（++）** 间隔时间为$exp(\lambda)$，第n个事件发生时刻为$\Gamma(n, \lambda)$，到达时刻条件分布（给定N(t)）为$U(0,t)$

**87、为什么要引入非齐次泊松过程？（+）** 每一时刻发生的概率不同，参数不再是$\lambda t$而是$m(t)=\int_0^t \lambda(u)du$，不再具有平稳增量性

**88、什么是马尔科夫链？（++）** t时刻分布的条件概率只与t-1时刻的状态有关

**89、什么是布朗运动？（++）** 随机过程满足：（1）初值零：B(0)=0 （2）独立、平稳增量 （3）正态分布：$B(t)\sim N(0, \sigma^2 t)$

**90、布朗运动和泊松过程的异同？（+）** （1）初值都为0，独立平稳增量（2）布朗运动实值正态，泊松过程非负整数 （3）分布、数字特征不同

**91、均值遍历性是什么？（+++）** 设$X=(X_n,n\geq 0)$是离散时间平稳随机过程，$EX_n=\mu,r_X(k)=E(X_0X_k)$，则$X$均值遍历$\Leftrightarrow$$\frac{1}{n^2}\sum_{k=1}^n(n-k)(r_X(k)-\mu^2)\rightarrow 0 (n\rightarrow\infty)$（一句话：时间平均等于样本平均）

**92、中心化/标准化/归一化的区别？（++++）** 中心化只减去均值，不除以任何东西；标准化除以标准差；归一化除以极差（当然不一定减去均值，可以减去最小值）

**93、系统聚类的过程？（++）** （1）定义类之间的距离 （2）按照规则逐个合并 （3）画出谱系图

**94、对于p维多元正态分布满足：**

$X= \left(  \begin{matrix}  X^{(1)}\\X^{(2)}    \end{matrix}   \right) \sim N_p(\left(  \begin{matrix}  \mu_1\\\mu_2    \end{matrix}   \right),  \left(  \begin{matrix}    \Sigma_{11} &amp; \Sigma_{12} \\     \Sigma_{21} &amp; \Sigma_{22}   \end{matrix} \right))\\$

**其中$X_1$为r维，$X_2$为p-r维，回答以下问题：（++）**

*   已知$X_2=x_2$后$X_1$的分布？$N_{r}(\mu_{1.2}, \Sigma_{11.2})$
*   已知$X_2=x_2$后$X_1$的条件期望？$\mu_{1.2}=\mu_1+\Sigma_{12}\Sigma_{22}^{-1}(x_2-\mu_2)$
*   已知$X_2=x_2$后$X_1$的条件方差？$\Sigma_{11.2}=\Sigma_{11}-\Sigma_{12}\Sigma_{22}^{-1}\Sigma_{21}$
*   用$X_2=x_2$预测$X_1$的回归系数？$\beta=\Sigma_{12}\Sigma_{22}^{-1}$

**95、多元正态分布中$\mu$和$\Sigma$的极大似然估计是什么？（+）** $\hat{\mu}=\bar{X}, \hat{\Sigma}=\frac{1}{n}A$，其中A为样本离差阵

**96、主成分分析为什么要先标准化？（+++）** PCA寻找方差最大的方向，如果不标准化，则会逼近数值最大的那一个特征，而忽略数值比较小的特征。（标准化能公平评估每个特征的重要性）

**97、阐述主成分分析、因子分析和典型相关分析的区别？（+++）**

*   主成分分析：使用原始变量的线性组合（主成分）
*   因子分析：构造因子模型（公因子+特殊因子）
*   典型相关分析：研究两组变量间的相关关系（构造变量的线性组合）

**98、主成分、正交因子和典型相关变量的方差？（+）**

*   主成分方差：$D(Z)=\Lambda$（即$Var(Z_i)=\lambda_i$）
*   正交因子方差：$D(\epsilon)=diag(\sigma_1^2,...,\sigma_p^2), D(F)=I_m$（即$Var(F_i)=1$）
*   典型相关变量方差：$D(W_k)=D(V_k)=1$

**99、主成分之间、因子之间和典型变量之间的相关性？（+）**

*   主成分的相关性：$Cov(Z_i,Z_j)=0$
*   因子的相关性：$Cov(F_i,F_j)=0, Cov(F,\epsilon)=0$
*   典型变量的相关性：$Cov(V_i, V_j)=Cov(W_i, W_j)=Cov(V_i, W_j)=0, Cov(V_i, W_i)=\sqrt{\lambda_i}$

**100、相关分析和回归分析的区别？（+++）** 相关分析适用于所有统计关系（相关系数，正相关，负相关，不相关），回归分析仅对存在因果关系而言

**101、阐述一元线性回归的基本假设（+++++）** （1）线性 （2）解释变量变异性，方差常数 （3）随机干扰项条件零均值 （4）随机干扰项条件同方差，序列不相关 （5）随机干扰项服从零均值正态分布

**102、最小二乘估计量的性质？（+++）** （1）线性性（是$Y_i$的线性组合）（2）无偏性（3）有效性（所有线性无偏估计量中具有最小方差）

**103、线性回归中变量的显著性检验的目的？如何检验线性回归模型的拟合优度？（+）** 判断变量$X$是否对$Y$具有显著的线性影响；可以用可决系数$R^2=\frac{ESS}{TSS}$检验拟合情况

**104、多元线性回归和一元相比有什么更多的假设？（++）** 对于解释变量增加了$X_j$之间无完全多重共线性

**105、F检验的目的？用到的检验统计量及其服从的分布？（+++）** 检验响应变量和预测变量之间是否有关系（注意与t检验区分）；检验问题为：$H_0: \beta_1=\beta_2=...=\beta_p=0$，检验统计量：$F=\frac{(TSS-RSS)/p}{RSS/(n-p-1)}\sim F_{p,n-p-1}$

**106、最小二乘估计和最大似然估计等价的条件？（++）** 当模型估计值和真实值间的残差项服从均值是0的高斯分布时，二者等价

**107、什么是残差图？高杠杆点和离群点的区别？（+）** 残差图是$e_i=y_i-\hat{y}_i$与$x_i$的散点图。离群点是$y_i$异常，而高杠杆点是$x_i$异常（高杠杆点只由异常的自变量组成，与因变量没有关系）

**108、标准差与标准误的区别？（++）** 标准差是样本数据方差的平方根，它衡量的是样本数据的离散程度；标准误是样本均值的标准差，衡量的是样本均值的离散程度。（可以这么理解，标准差是一次抽样中个体分数间的离散程度，反映了**个体**分数对**样本均值**的代表性；标准误是多次抽样中样本均值间的离散程度，反映了**样本均值**对**总体均值**的代表性）

**109、线性回归如何计算残差标准误？（+）**

*   二元：$RSE=\sqrt{\frac{RSS}{n-2}}$
*   p元：$RSE=\sqrt{\frac{RSS}{n-p-1}}$

**110、线性模型如何防止过拟合？当需要对于自变量数目不同的模型进行选择的时候应该用哪些指标？（+++）** 防止过拟合的方法：变量子集选择，压缩估计，降维；对于变量数目不同的模型不能使用$R^2$或RSS，而应当使用如下指标（设$\hat{\sigma}^2=Var(\epsilon)$）：

*   $C_p=\frac{1}{n}(RSS+2p\hat{\sigma}^2)$
*   $AIC=\frac{1}{n\hat{\sigma}^2}(RSS+2p\hat{\sigma}^2)$
*   $BIC=\frac{1}{n}(RSS+log(n)p\hat{\sigma}^2)$
*   $R^2_{Adj}=1-\frac{RSS/(n-d-1)}{TSS/(n-1)}$

**111、时间序列中偏相关系数的定义？（+）** 偏相关系数$a_{n,n}$为$X_1$和$X_{n+1}$扣除$X_2,...,X_n$线性影响后的相关系数：$a_{n,n}=Corr[X_1-L(X_1|X_2,...,X_n), X_{n+1}-L(X_{n+1}|X_2,...,X_n)]$

**112、叙述最佳线性预测的定义？（+）** 随机变量$Y, X_j$零均值方差有限，若$\forall b\in R^n$有$E(Y-a^TX)^2\leq E(Y-b^TX)^2$则$a^TX$为对$Y$的最佳线性预测

**113、什么是白噪声的卡方检验？（+）** $H_0:\{X_t\}$为独立白噪声，$H_1:\{X_t\}$为相关序列。检验统计量$\hat{\chi}^2(m)=N(\hat{\rho}_1^2+...+\hat{\rho}_m^2)$，其中$\hat{\rho}_j^2$为样本自相关系数，$P(\hat{\chi}^2(m)>\chi_\alpha^2)=\alpha$，当$\hat{\chi}^2(m)>\chi_\alpha^2$时拒绝原假设。

**114、写出下列优化问题的目标函数（+++）**

*   岭回归

$\min_{\beta_0,\beta_1,...,\beta_p}\sum_{i=1}^n(y_i-\beta_0-\sum_{j=1}^p\beta_j x_{ij})^2+\lambda\sum_{j=1}^p\beta_j^2 \\$

*   LASSO回归

$\min_{\beta_0,\beta_1,...,\beta_p}\sum_{i=1}^n(y_i-\beta_0-\sum_{j=1}^p\beta_j x_{ij})^2+\lambda\sum_{j=1}^p|\beta_j| \\$

*   决策树（划分为J个区域）: $\min\sum_{j=1}^J\sum_{i\in R_j}(y_i-\hat{y}_{R_j})$  
    
*   决策树（带有剪枝）: $\min\sum_{j=1}^{|T|}\sum_{i\in R_j}(y_i-\hat{y}_{R_j})+\alpha |T|$  
    
*   k-means  
    

$\min_{C_1,...,C_K}(\sum_{k=1}^K\frac{1}{|C_k|}\sum_{i,i'\in C_k}\sum_{j=1}^p (x_{ij}-x_{i'j})^2) \\$

**115、最大间隔分类器、支持向量分类器、支持向量机的区别？（+）** 最大间隔分类器仅仅使得分割超平面的间隔最大，支持向量分类器允许错分（软间隔），支持向量机加入高次项并使用核技巧解决非线性问题
