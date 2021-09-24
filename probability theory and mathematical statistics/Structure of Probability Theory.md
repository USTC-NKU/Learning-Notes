---
title: Structure of Probability Theory
math: true
tags: Structure of Probability Theory
categories: Probability Theory 
---
[toc]
概率论，是研究随机现象数量规律的数学分支.本文旨在构建概率论这门学科在本科阶段的基本框架. 

***
# 1事件极其概率
***

## 1.1 随机现象与统计规律性
略
## 1.2 基本定义

**1.2.1 样本空间与样本点**

*   样本点 ($w$)：随机事件的每一基本结果
*   样本空间 ($\Omega$)：样本点的全体

**1.2.2 古典概型与几何概型**

*   **古典概型**：$p(A)=\frac{m}{n}$，其中m为事件A包含的样本点数，n为样本空间的样本点数。  
    
*   古典概型的推广$P(A)=\sum_{i,w_i\in A}P(w_i)$，概率满足：  
    

*   非负性：$P(A)\ge 0$
*   规范性：$P(\Omega)=1$
*   可列可加性：若$A_i\bigcap A_j=\emptyset$，则$P(\sum_{i=1}^\infty A_i)=\sum_{i=1}^\infty P(A_i)$

  

*   **几何概型**：事件$A_g=\{任取一个样本点，落在区域g\subset\Omega\}$，则概率定义为$P(A_g)=\frac{g的测度}{\Omega的测度}$。  
    

## 1.3 概率的公理化定义

**1.3.1 事件**

*   记号：$\emptyset$：不可能事件；$\Omega$：必然事件
*   事件的关系：$A\subseteq B$：A发生意味着B发生；$A\bigcap B$：AB同时发生；$A\bigcup B$：A或B发生；$\bar{A}$：A的对立事件；$A/B$：A发生B不发生

**1.3.2 概率空间**

*   三要素：样本空间($\Omega$)，事件域$\mathcal{F}$，概率$P$
*   概率

*   (1) $P(\emptyset)=0, P(\Omega)=1$
*   (2) 可数可加性：$P(\sum A_i)=\sum P(A_i)$
*   (3) 概率运算

*   $P(\bar{A})=1-P(A)$
*   $B\subset A$则$P(A-B)=P(A)P(B)$
*   $P(A\bigcup B)=P(A)+P(B)-P(AB)$
*   $P(A/B)=P(A)-P(AB)$

  

*   (4) 多还少补性：$P(A_1\bigcup A_2\bigcup ...\bigcup A_n)=\sum_{i=1}^n P(A_i)-\sum P(A_iA_j)+...+(-1)^{n-1}P(A_1A_2...A_n)$
*   (5) 次可加性：$P(\bigcup_{i=1}^\infty A_i)\leq\sum_{i=1}^\infty P(A_i)$

**1.3.3 概率测度的连续性**

*   【定理1.1】若$A_1,A_2,...$是一列单调增加的事件序列，具有极限$A$，那么$P(A)=\lim\limits_{n\rightarrow\infty} P(A_n)$

## 1.4 条件概率与事件的独立性

**1.4.1 条件概率**

*   【定义1.2 条件概率】在事件B发生的条件下A发生的概率：$P(A|B)=\frac{P(AB)}{P{B}}$
*   链式法则：$P(A_1A_2...A_n)=P(A_1)P(A_2|A_1)P(A_3|A_2A_1)...P(A_n|A_{n-1}...A_1)$

**1.4.2 全概率公式与贝叶斯公式**

*   【定义1.3 完备事件组】事件列$\{A_1,A_2,...,A_n\}$为$\Omega$的一个完备事件组若满足（1）$A_i$之间两两互不相容，$P(A_i)>0$；（2）$\sum_{i=1}^\infty A_i=\Omega$  
    
*   【定理1.2】全概率公式：若$\{A_1,A_2,...,A_n\}$为完备事件组，则对任意事件B有：$P(B)=\sum_{i=1}^\infty P(A_i)P(B|A_ i)$  
    
*   【定理1.3】贝叶斯公式：若$\{A_1,A_2,...,A_n\}$为完备事件组，则对任意事件B有：$P(A_i|B)=\frac{P(A_i)P(B|A_ i)}{\sum_{k=1}^\infty P(A_k)P(B|A_k)}$  
    

**1.4.3 事件的独立性**

*   两个事件独立的充要条件：$P(AB)=P(A)P(B)$
*   三个事件独立的充要条件：

$\begin{cases} P(AB)=P(A)P(B)\\ P(AC)=P(A)P(C)\\ P(BC)=P(B)P(C)\\ P(ABC)=P(A)P(B)P(C) \end{cases}\\$

*   n个事件独立的充要条件：对于一切可能的组合$1\leq i\le j\le k\le...\leq n$，有

$\begin{cases} P(A_iA_j)=P(A_i)P(A_j)\\ P(A_iA_jA_k)=P(A_i)P(A_j)P(A_k)\\ ...\\ P(A_iA_j...A_n)=P(A_i)P(A_j)...P(A_n) \end{cases}\\$

# 2随机变量与分布函数
---------------

## 2.1 离散型随机变量极其分布

**2.1.1 随机变量的概念**

*   【定义2.1 随机变量】设$\xi(w)$是定义在概率空间$\{\Omega,\mathcal{F},P\}$上的实值函数，且对$R$上的任一波雷尔集$B$，有

$\xi^{-1}(B)=\{w:\xi(w)\in B\}\in\mathcal{F} \\$

就称$\xi(w)$为随机变量，而称$\{P(\xi(w)\in B)\},B\in\mathcal{B}$为随机变量的概率分布。

**2.1.2 离散型随机变量**

*   【定义2.2 离散型随机变量】若随机变量$\xi$可能取的值至多可列个，则$\xi$为离散型随机变量。  
    
*   常见的离散型随机变量  
    

*   退化分布（单点分布）：$P(\xi=c)=1$
*   两点分布 & 伯努利分布：$p,q>0, p+q=1$

*   伯努利分布：$P(\xi=1)=p, P(\xi=0)=q$
*   两点分布：$P(\xi=x_1)=p, P(\xi=x_2)=q$

*   二项分布（n次伯努利实验）：$P(\xi=k)=C_n^k p^k q^{n-k}$

*   对称性：$b(k;n,p)=b(n-k;n,1-p)$
*   增减性：$k< (n+1)p$可能性随k递增，大于反之
*   递推公式：$\xi\sim B(n,p)$则$P(\xi=k+1)=\frac{P(n-k)}{q(k+1)}P(\xi=k)$
*   泊松定理：$n\rightarrow\infty$有$np_n\rightarrow\lambda$则$\lim\limits_{n\rightarrow\infty} b(k;n,p)=\frac{\lambda^k}{k!}e^{-\lambda}$

*   泊松分布：$\xi\sim P(\lambda): P(\xi=k)=\frac{\lambda^k}{k!}e^{-\lambda}$
*   几何分布：$P(\xi=k)=pq^{k-1},p+q=1,p,q>0$
*   超几何分布：$P(\xi=k)=\frac{C_M^kC_{N-M}^{n-k}}{C_N^n},n\leq N,M\leq N$

## 2.2 分布函数与连续型随机变量

**2.2.1 分布函数**

*   【定义2.3 分布函数】随机变量$\xi(w)$的分布函数：$F(x)=P(\xi\leq x), -\infty< x< \infty$
*   分布函数的性质

*   单调不减性：若$a< b$则$F(a)\leq F(b)$
*   $\lim\limits_{x\rightarrow-\infty}F(x)=0$, $\lim\limits_{x\rightarrow\infty}F(x)=1$
*   右连续型：$F(x+0)=F(x)$

**2.2.2 连续型随机变量与密度函数**

*   【定义2.4 连续型随机变量】随机变量$\xi$可取某区间一切值，且存在非负可积函数$P(x)$使得分布函数$F(x)$满足：$F(x)=\int^x_{-\infty} p(y)dy, -\infty< x< \infty\\$ 则$\xi$为连续型随机变量，$P(x)$为$\xi$的密度函数。  
    
*   密度函数的性质  
    

*   非负性：$p(x)\geq 0$
*   规范性：$\int_{-\infty}^{\infty}p(x)dx=1$

**2.2.3 常见的连续型随机变量**

*   均匀分布：$\xi\sim U(a,b)$

$p(x)=\begin{cases} \frac{1}{b-a}&amp;,a\leq x\leq b\\ 0&amp;, others \end{cases}, F(x)=\begin{cases} 0&amp;, x< a\\ \frac{x-a}{b-a}&amp;,a\leq x< b\\ 1&amp;, x\geq b \end{cases}\\$

*   正态分布：$\xi\sim N(a,\sigma^2)$

$p(x)=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{(x-a)^2}{2\sigma^2}},-\infty< x<\infty \\$$F(x)=\int_\infty^x\frac{1}{\sqrt{2\pi}}e^{-\frac{u^2}{2}du}, X\sim N(0,1) \\$

*   指数分布：$\xi\sim exp(\lambda),\lambda >0$

$p(x)=\begin{cases} \lambda e^{-\lambda x}&amp;,x\geq 0\\ 0&amp;, others \end{cases}, F(x)=\begin{cases} 1-e^{-\lambda x}&amp;, x\geq 0\\ 0&amp;, others \end{cases}\\$

*   $\Gamma$分布：$\xi\sim Ga(\alpha,\lambda),\alpha>0,\gamma>0$

$p(x)=\frac{\lambda^\alpha}{\Gamma(\alpha)}x^{\alpha-1}e^{-\lambda x}, x>0 \\$

*   $\beta$分布：$\xi\sim \beta(a,b), a>0,b>0$

$p(x)=\frac{\Gamma(a+b)}{\Gamma(a)\Gamma(b)}x^{a-1}(1-x)^{b-1}, 0< x< 1 \\$

*   柯西分布：

$p(x)=\frac{1}{\pi[1+(x-\theta)^2]},-\infty< x<\infty \\$

## 2.3 随机向量

**2.3.1 离散型随机向量**

*   【定义2.5 n维随机向量】$\xi_1(w),\xi_2(w),...,\xi_n(w)$定义在同一概率空间$(\Omega,\mathcal{F},P)$上，就称$\xi(w)=(\xi_1(w),\xi_2(w),...,\xi_n(w))$为n维随机向量。

**2.3.2 分布函数**

*   【定义2.6 (联合)分布函数】对任意$(x_1,x_2,...,x_n)\in R^n$，称n元函数$F(x_1,x_2,...,x_n)=P(\xi_1(w)\leq x_1,...,\xi_n(w)\leq x_n)$为随机向量$\xi(w)=(\xi_1(w),\xi_2(w),...,\xi_n(w))$的（联合）分布函数。  
    
*   分布函数的性质  
    

*   对每个变量单调不减
*   对每个变量右连续
*   $F(x,-\infty)=0,F(-\infty,y)=0,F(\infty,\infty)=1$
*   对任意$a_1< b_1,a_2< b_2, F(b_1,b_2)-F(a_1,b_2)-F(b_1,a_2)+F(a_1,a_2)\geq 0$

*   密度函数$p$  
    

*   $F(x_1,...,x_n)=\int^{x_1}_{-\infty}...\int^{x_n}_{-\infty}p(y_1,...,y_n)dy_1...dy_n$

*   密度函数的性质  
    

*   非负性：$p(x_1,...,x_n)\geq 0$
*   规范性：$\int^{\infty}_{-\infty}...\int^{\infty}_{-\infty}p(y_1,...,y_n)dy_1...dy_n=1$

*   边际分布函数  
    

*   $F_\xi(x)=F(x,\infty)=\int^x_{-\infty}p_\xi(u)du$
*   $F_\eta(y)=F(\infty,y)=\int^y_{-\infty}p_\eta(v)dv$

*   边际密度函数  
    

*   $p_\xi(u)=\int^{\infty}_{-\infty}p(u,v)dv=F'_\xi(x)$
*   $p_\eta(v)=\int^{\infty}_{-\infty}p(u,v)du=F'_\eta(y)$

## 2.4 随机变量的独立性

*   【定义2.8 相互独立】  
    

*   离散型：$P(\xi=x_i,\eta=y_i)=P(\xi=x_i)P(\eta=y_i)$
*   连续型：$F(x,y)=F_\xi(x)F_\eta(y)$

*   【定理2.1】相互独立的充要条件：联合密度等于边际密度乘积$p(x,y)=p_\xi(x)P_\eta(y)$  
    
*   【推论2.1】若$\xi_1,...,\xi_n$相互独立，则其中的任意$r$个（$2\leq r< n$）个也相互独立

## 2.5 条件分布

**2.5.1 离散型的情形**

*   条件分布列：$P_{\eta|\xi}(y_j|x_i)=P(\eta=y_j|\xi=x_i)=\frac{P(\xi=x_i,\eta=y_i)}{P(\xi=x_i)}$  
    
*   条件分布函数：$P(\eta\leq y|\xi=x_i)=\sum_{j:y_j\leq y}P_{\eta|\xi}(y_j|x_i)$  
    

**2.5.2 连续的情形**

*   条件分布函数：$P(\eta\leq y|\xi=x)=\int_{-\infty}^y\frac{P(x,v)}{P_\xi(x)}dv=F_{\eta|\xi}(y|x)$  
    
*   条件密度函数：$P_{\eta|\xi}(y|x)=\frac{P(x,y)}{P_\xi(x)}$  
    

**2.5.3 一般情形**

*   条件分布列：$F_{\eta|\xi}(y|x)=\sum_{j:y_j\leq y}P_{\eta|\xi}(y_j|x)$  
    
*   条件密度函数：$F_{\eta|\xi}(y|x)=\int_{-\infty}^yP_{\eta|\xi}(v|x)dv$  
    

**2.5.4 给定随机变量下的条件概率**

*   设$X$为随机变量，$A$为随机事件，则（全概率公式的连续形式）：$P(A)=P(A,-\infty< X< \infty)=\int_{-\infty}^{\infty}P(A|X=x)P_X(x)dx$

## 2.6 随机变量的函数及其分布

**2.6.1 离散型随机变量的函数**

*   离散卷积公式：$P(\xi+\eta=r)=\sum_{k=0}^rP(\xi=k)P(\eta=r-k)$

**2.6.2 一维连续型随机变量的函数分布**

*   【定理2.2】 假设$f(x)$严格单调，其反函$f^{-1}(y)$有连续导函数，则$\eta=f(\xi)$也是连续型随机变量，密度函数为：

$g(y)=\begin{cases} P(f^{-1}(y))|(f^{-1}(y))'|,&amp; y\in f(x)的值域\\ 0,&amp; others \end{cases}\\$

*   【推论2.2】 假设$f(x)$在不重叠的区间$I_1,I_2,...$上逐段严格单调，且$I_i,i=1,2,...$之和为$(-\infty,\infty)$，在各段的反函数$h_1(y),h_2(y),...$有连续导数，则$\eta=f(\xi)$是连续型随机变量，其密度为：

$g(y)=\begin{cases} \sum P(h_i(y))|(h_i(y))'|,&amp; y\in 各h_i(y)的定义域\\ 0,&amp; others \end{cases}\\$

**2.6.3 随机向量函数的分布律**

*   卷积公式：$P_X,P_Y$为$X,Y$的密度函数，则$\eta$的密度为：  
    

*   $\eta=X+Y$

*   $X,Y$独立：$P_\eta(z)=\int_{-\infty}^{\infty}P_X(x)P_Y(z-x)dx$
*   $X,Y$不独立：$P_\eta(z)=\int_{-\infty}^{\infty}P(x,z-x)dx$

*   $\eta=X-Y$

*   $X,Y$独立：$P_\eta(z)=\int_{-\infty}^{\infty}P_X(x)P_Y(z+x)dx$
*   $X,Y$不独立：$P_\eta(z)=\int_{-\infty}^{\infty}P(x,z+x)dx$

*   $\eta=X\times Y$

*   $X,Y$独立：$P_\eta(z)=\int_{-\infty}^{\infty}\frac{1}{|x|}P_X(x)P_Y(\frac{z}{x})dx$
*   $X,Y$不独立：$P_\eta(z)=\int_{-\infty}^{\infty}\frac{1}{|x|}P(x,\frac{z}{x})dx$

*   $\eta=\frac{X}{Y}$

*   $X,Y$独立：$P_\eta(z)=\int_{-\infty}^{\infty}|x|P_X(x)P_Y(zx)dx$
*   $X,Y$不独立：$P_\eta(z)=\int_{-\infty}^{\infty}|x|P(x,zx)dx$

*   次序统计量的分布: 设$\xi_1,\xi_2,...,\xi_n$独立同分布，分布函数都为$F(x)$，把$\xi_1,\xi_2,...,\xi_n$每取一组值$\xi_1(w),\xi_2(w),...,\xi_n(w)$按大小次序排列，所得随机变量$\xi_1^*\leq\xi_2^*\leq...\leq\xi_n^*$称为次序统计量。  
    

*   $\xi_n^*$的分布函数：$P(\xi_n^*\leq x)=(F(x))^n$
*   $\xi_1^*$的分布函数：$P(\xi_1^*\leq x)=1-(1-F(x))^n$
*   $(\xi_1^*,\xi_n^*)$联合分布函数：

$F(x,y)=P(\xi_1^*\leq x,\xi_n^*\leq y)=\begin{cases} (F(x))^n-(F(y)-F(x))^n, x< y\\ (F(y))^n, x\geq y \end{cases}\\$

**2.6.4 随机向量的变换**

*   【定理2.3】如果$m=n$，$f_j,j=1,2,...,n$有唯一的反函数组：$x_i=x_i(y_1,...,y_n),i=1,...,n$，且$J=\frac{\partial(x_1,...,x_n)}{\partial(y_1,...,y_n)}≠0$,则$(\eta_1,...,\eta_n)$是连续型随机向量，当$(y_1,...,y_n)\in(f_1,...,f_n)$值域，密度函数为$q(y_1,...,y_n)=p(x_1(y_1,...,y_n),...,x_n(y_1,...,y_n))|J|$，其他情况$q(y_1,...,y_n)=0$。  
    
*   【定理2.4】令$l\leq n_1< n_2<...< n_k=n$，$f_1$是$n_1$个变量的波雷尔可测函数，$f_k$是$n_k-n_{k-1}$个变量的波雷尔可测函数，若$X_1,...,X_n$是独立随机变量，那么$f_1(X_1,...,X_{n_1}),f_2(X_{n_1+1},...,X_{n_2}),...,f_k(X_{n_{k-1}+1},...,X_{n_k})$相互独立。特别，当$f_1,f_2,...,f_k$是单变量函数时，$f_1(X_1),f_2(X_2),...,f_k(X_k)$相互独立。  
    

# 3数字特征与特征函数
---------------

## 3.1 数学期望

**3.1.1-3.1.5 数学期望的定义与性质**

*   数学期望的定义

*   离散型：若$\sum_k x_k p_k$绝对收敛，则$E\xi=\sum_k x_k p_k$为$\xi$的数学期望
*   连续型：当$\int_{-\infty}^\infty|x|p(x)dx<\infty$时，称$E\xi=\int_{-\infty}^\infty xp(x)dx$为$\xi$的数学期望。
*   一般定义：设分布函数为$F(x)$，若$\int_{-\infty}^\infty xdF(x)<\infty$，称$\int_{-\infty}^\infty xdF(x)$为$\xi$的数学期望。

*   【定理3.1】随机变量函数的数学期望：设$\xi$为随机变量，$f(x)$为一元波雷尔函数，记$\eta=f(\xi)$，分布函数为$F_\xi(x),F_\eta(x)$，则$E_\eta=\int_{-\infty}^\infty xdF_\eta(x)=\int_{-\infty}^\infty f(x)dF_\xi(x)$

*   注：若$\xi$有密度函数$p(x)$则$Ef(\xi)=\int_{-\infty}^\infty f(x)p(x)dx$

*   数学期望的基本性质

*   常数的期望：$\xi=c$则$E\xi=Ec=c$
*   单调性

*   $a\leq\xi\leq b$则$E_\xi$存在，$a\leq E\xi\leq b$
*   若$|\xi|\leq\eta$且$E\eta$存在，则$E\xi$存在且$|E\xi|\leq E|\xi|\leq E\eta$

*   线性：$E(\sum_{i=1}^n c_i\xi_i+b)=\sum_{i=1}^n c_iE\xi_i+b$
*   独立可分离：若$\xi_1,...,\xi_n$相互独立，则$E(\xi_1...\xi_n)=E\xi_1...E\xi_n$
*   有界收敛定理：设对$\forall w \in\Omega$有$\lim\limits_{n\rightarrow\infty}\xi_n(w)=\xi(w)$且对一切$n\geq 1$，$|\xi_n|\leq M$，则$\lim\limits_{n\rightarrow\infty}E\xi_n=E\xi$

**3.1.6 条件期望**

*   【定义3.4 条件期望】$m(x)=E(\eta|\xi=x)$，则$m(\xi)$为已知$\xi$时$\eta$的条件期望，记作$E(\eta|\xi)$  
    
*   全期望公式：$E\eta=\sum_i p_i E(\eta|\xi=x_i)P(\xi=x_i)$  
    
*   条件期望的性质  
    

*   线性：$E(a_1\eta_1+a_2\eta_2|\xi=x)=a_1E(\eta_1|\xi=x)+a_2E(\eta_2|\xi=x)$
*   条件期望的运算：

*   $E(g(\eta)|\xi=x)=\int_{-\infty}^\infty g(y)dF_{\eta|\xi}(y|x)$
*   $E(g(\eta)|\xi=x)=\sum_j g(y_j)P_{\eta|\xi}(y_j|x)$
*   $E(g(\eta)|\xi=x)=\int_{-\infty}^\infty g(y)P_{\eta|\xi}(y|x)dy$

*   不等式：$\eta_1<\eta_2$则$E(\eta_1|\xi=x)\leq E(\eta_2|\xi=x)$
*   $E(h(\xi)\eta|\xi)=h(\xi)E(\eta|\xi)$
*   柯西-施瓦茨不等式：$|E(XY|Z)|\leq\sqrt{E(X^2|Z)}\sqrt{E(Y^2|Z)}$

## 3.2 方差、协方差与相关系数

**3.2.1 方差**

*   【定义3.5 方差\\标准差】$Var\xi=E(\xi-E\xi)^2, S\xi=\sqrt{Var\xi}$  
    
*   切比雪夫不等式：$P(|\xi-E\xi|\geq \epsilon)\leq\frac{Var\xi}{\epsilon^2}$  
    
*   方差的计算:  
    

*   一般情况：$Var\xi=\int_{-\infty}^{\infty}(x-E\xi)^2 dF_\xi(x)$
*   离散情况：$Var\xi=\sum_i(x_i-E\xi)^2P(\xi=x_i)$
*   连续情况：$Var\xi=\int_{-\infty}^{\infty}(x-E\xi)^2P_\xi(x)dx$
*   方差与期望：$Var\xi=E\xi^2-(E\xi)^2$

  

*   方差的性质：  
    

*   常数方差为零：$P(\xi=c)=1\Leftrightarrow Var\xi=0$
*   $Var(c\xi+b)=c^2Var\xi$
*   不等式：若$c≠E\xi$，则$Var\xi< E(\xi-c)^2$
*   方差求和式：$Var(\sum_{i=1}^n\xi_i)=\sum_{i=1}^n Var\xi_i+2\sum_{1\leq i< j\leq n}E(\xi_i-E\xi_i)(\xi_j-E\xi_j)$

*   两两独立时有：$Var(\sum_{i=1}^n\xi_i)=\sum_{i=1}^n Var\xi_i$

**3.2.2 协方差**

*   【定义3.6 协方差】设$\xi_i,\xi_j$的联合分布为$F_{ij}(x,y)$，若$E|(\xi_i-E\xi_i)(\xi_j-E\xi_j)|<\infty$，称$E(\xi_i-E\xi_i)(\xi_j-E\xi_j)=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}(x-E\xi_i)(y-E\xi_j)dF_{ij}(x,y)$为$\xi_i$和$\xi_j$的协方差，记作$Cov(\xi_i,\xi_j)$。  
    
*   协方差的性质：  
    

*   $Cov(\xi,\eta)=Cov(\eta,\xi)=E\xi\eta-E\xi E\eta$
*   $Cov(a\xi,b\eta)=abCov(\xi,\eta)$
*   $Cov(\sum_{i=1}^n\xi_i,\eta)=\sum_{i=1}^n Cov(\xi_i,\eta)$
*   $\vec{\xi}=(\xi_1,\xi_2,...,\xi_n)^T,c=[c_{ij}]_{n\times n}$，则$C\xi$的协方差阵为$CBC'$，其中$B$为$\vec{\xi}$的协方差阵。
*   $\vec{\xi}\sim N(\vec{\mu},B)$，$\vec{\mu}$为n维向量，$B_{n\times n}$对称正定，则$E\vec{\xi}=\vec{\mu}$，协方差阵为$B$。

**3.2.3 相关系数**

*   【定义3.7 相关系数】令$\xi^*=\frac{\xi-E\xi}{\sqrt{Var\xi}}$,$\eta^*=\frac{\eta-E\eta}{\sqrt{Var\eta}}$，称$r=Cov(\xi^*,\eta^*)=E\frac{(\xi-E\xi)}{\sqrt{Var\xi}}\frac{(\eta-E\eta)}{\sqrt{Var\eta}}$为$\xi$,$\eta$相关系数。  
    
*   柯西-施瓦茨不等式的三种形式  
    

*   $|E\xi\eta|^2\leq E\xi^2 E\eta^2$
*   $E|X-EX||Y-EY|\leq \sqrt{E(X-EX)^2E(Y-EY)^2}$
*   $Cov(X,Y)\leq\sqrt{VarX\times VarY}$

  

*   相关系数的性质  
    

*   $|r|\leq 1$
*   设随机变量$\xi,\eta$的方差有限，则以下条件等价：

*   （1）$Cov(\xi,\eta)=0$
*   （2）$\xi$与$\eta$不相关
*   （3）$E\xi\eta=E\xi E\eta$
*   （4）$Var(\xi+\eta)=Var\xi+Var\eta$

*   若$\xi,\eta$独立且方差有限，则$\xi$与$\eta$不相关
*   对二元正态随机向量，两个分量不相关与独立等价

## 3.3 特征函数

**3.3.1 定义**

*   【定义3.8 复随机变量】设$\xi,\eta$为随机变量，则$\zeta=\xi+i\eta$为复随机变量，期望为$E\zeta=E\xi+iE\eta$  
    
*   【定义3.9 特征函数】$f(t)=Ee^{it\xi},-\infty< t< \infty$为$\xi$的特征函数  
    

*   一般形式：$f(t)=\int_{-\infty}^{\infty} e^{itx}dF(x)$
*   离散形式：$f(t)=\sum_{n=1}^\infty p_n e^{itx_n},-\infty< x<\infty$
*   连续形式：$f(t)=\int_{-\infty}^{\infty} e^{itx}p(x)dx$

**3.3.2 性质**

*   【定理3.2】 $f(t)$为特征函数$\Leftrightarrow$ $f(t)$非负定，连续且$f(0)=1$ （这个定理包含了特征函数的三个性质）

*   $|f(t)|\leq f(0)=1, f(-t)=\overline{f(t)}$
*   $f(t)$在$R$上一致连续
*   $f(t)$非负定：对$\forall n, t_1,...,t_n\in R, \lambda_1,...,\lambda_n\in C$有$\sum_{k=1}^n\sum_{j=1}^n f(t_k-t_j)\lambda_k\bar{\lambda_j}\geq 0$

*   乘法公式：若$\xi_1,...\xi_n$相互独立，特征函数$f_1(t),...,f_n(t), \eta=\xi_1+...+\xi_n$，则$f_n(t)=f_1(t)...f_n(t)$
*   高阶矩与特征函数：$E\xi^n$存在$\rightarrow$$f(t)$n次可微$\rightarrow$$k\leq n$时$f^{(k)}(t)=i^k\int_{-\infty}^{\infty}x^k e^{itx}dF(x),f^{(k)}(0)=i^k E\xi^k$

*   常用公式：$f'(0)=iE\xi$

*   随机变量线性变换的特征函数：$\eta=a\xi+b\rightarrow f_n(t)=e^{ibt}f(at)$

**3.3.3 逆转公式与唯一性定理**

*   【定理3.3】逆转公式：分布函数$F(x)$的特征函数为$f(t)$，则$F(x_2)-F(x-1)=\lim\limits_{T\rightarrow\infty}\frac{1}{2\pi}\int_{-T}^T \frac{e^{-itx_1}-e^{-itx_2}}{it}f(t)dt$  
    
*   【定理3.4】唯一性定理：分布函数可以由特征函数唯一确定  
    

*   密度函数被特征函数唯一确定：$p(x)=F'(x)=\frac{1}{2\pi}\int_{-\infty}^{\infty}e^{-itx} f(t)dt$

*   【定理3.5】傅里叶变换：设$f(t)$是特征函数，$\int_{-\infty}^{\infty}|f(t)|dt<\infty$（绝对可积），则$F'(x)$存在且连续。  
    

**3.3.4 特征函数的可加性**

*   独立同分布随机变量的联合特征函数可分解为各自的乘积

**3.3.5 多元特征函数**

*   【定义3.10】随机向量$\vec{\xi}=(\xi_1,...,\xi_n)'$的分布函数为$F(x_1,...,x_n)$，称$f(t_1,...,t_n)=Ee^{i(t_1\xi_1+...+t_n\xi_n)}=\int_{-\infty}^{\infty}...\int_{-\infty}^{\infty}e^{i(t_1\xi_1+...+t_n\xi_n)}dF(x_1,...,x_n)$为它的特征函数。

# 4极限定理
----------

## 4.1 依分布收敛与中心极限定理

**4.1.1 分布函数收敛弱收敛**

*   【定义4.1 弱收敛】设$F$是一分布函数，$\{F_n\}$是一列分布函数，如果对$F$的每个连续点$x\in R$当$n\rightarrow\infty$时，都有$F_n(x)\rightarrow F(x)$，则称$F_n$弱收敛。  
    
*   【定义4.1 依分布收敛】设$\xi$是一随机变量，$\{\xi_n\}$是一列随机变量，如果$\xi_n$的分布函数弱收敛于$\xi$的分布函数，则称$\xi_n$依分布收敛与$\xi$，记作$\xi_n\stackrel{d}\longrightarrow\xi$。  
    
*   【定理4.3】Levy连续性定理：设$F$是一分布函数，$\{F_n\}$是一列分布函数，如果$F_n\stackrel{w}\longrightarrow F$，则相应的特征函数列$\{f_n(t)\}$关于$t$在任何有限区间内一致收敛于$F$的特征函数$f(t)$。  
    
*   【定理4.4】逆极限定理：设$f_n(t)$是分布函数$F_n(x)$的特征函数，如果对于每个$t$，$f_n(t)\rightarrow f(t)$，且$f(t)$在$t=0$处连续，则$f(t)$一定是某个分布函数$F$的特征函数，且$F_n\stackrel{w}\longrightarrow F$。  
    

**4.1.3 中心极限定理**

*   【定义4.2 中心极限定理】设$\{\xi_n\}$是一列随机变量，如果存在常数$B_n> 0$与$A_n$使得

$\frac{1}{B_n}\sum_{k=1}^n \xi_k-A_n\stackrel{d}\longrightarrow N(0,1) \\$

*   【定理4.5】(de Moivre-Laplace)：设$\Phi(x)$为标准正态分布的分布函数，对$-\infty< x<\infty$有：

$\lim\limits_{n\rightarrow\infty} P(\frac{S_n-np}{\sqrt{np(1-p)}}\leq x)=\Phi(x) \\$

*   【定理4.6】(Lindeberg-Levy)：设$\{\xi_n\}$是一列独立同分布的随机变量，记$S_n=\sum_{k=1}^n\xi_k$，$E\xi_1=\mu$，$Var\xi_1=\sigma^2$，则中心极限定理成立，即

$\frac{S_n-n\mu}{\sqrt{n}\sigma}\stackrel{d}\longrightarrow N(0,1) \\$

*   【定理4.7】(Lindeberg-Feller)：设$\{\xi_k\}$为独立随机变量序列，则费勒条件：$\lim\limits_{n\rightarrow\infty}\frac{1}{\sum_{k=1}^n Var\xi_k} max_{1\leq k\leq n} Var\xi_k=0$与$\frac{\sum_{k=1}^n(\xi_k-E\xi_k)}{\sqrt{\sum_{k=1}^n Var\xi_k}}\stackrel{d}\longrightarrow N(0,1)$ 成立的充要条件是Lindeberg被满足：对任意$\tau>0$，

$\frac{1}{\sum_{k=1}^n Var\xi_k}\sum_{k=1}^n\int_{|x-E\xi_k|\geq\tau\sqrt{\sum Var\xi_k}}(x-E\xi_k)^2 dF_k(x)\rightarrow 0 \\$

*   【定理4.8】(Lyapunov)：若对独立随机变量序列$\{\xi_n\}$，存在常数$\delta>0$，使得当$n\rightarrow\infty$时有：

$\frac{1}{(\sum_{k=1}^n Var\xi_k)^{1+\delta/2}}\sum_{k=1}^n E|\xi_k-E\xi_k|^{2+\delta} \rightarrow 0 \\$

则中心极限定理成立。

## 4.2 依概率收敛与弱大数定律

**4.2.1 依概率收敛**

*   【定义4.3 依概率收敛】设$\xi$和$\xi_n, n\geq 1$，是定义在同一概率空间$(\Omega,\mathcal{F},P)$上的随机变量，如果对任意$\epsilon>0$，$\lim\limits_{n\rightarrow\infty} P(|\xi_n-\xi|\geq\epsilon)=0$或$\lim\limits_{n\rightarrow\infty} P(|\xi_n-\xi|<\epsilon)=1$，则称$\xi_n$依概率收敛于$\xi$，记作$\xi_n\stackrel{P}\longrightarrow\xi$  
    
*   【定理4.9】设$\xi$和$\xi_n,n\geq 1$是定义在概率空间$(\Omega,\mathcal{F},P)$上的随机变量：  
    

*   1.如果$\xi_n\stackrel{P}\longrightarrow\xi$，则$\xi_n\stackrel{d}\longrightarrow \xi$
*   2.如果$\xi_n\stackrel{d}\longrightarrow c$，c为常数，则$\xi_n\stackrel{P}\longrightarrow c$

*   依概率收敛的性质：若$X_n\stackrel{P}\longrightarrow X,Y_n\stackrel{P}\longrightarrow Y$，则有：

*   $X_n\pm Y_n\stackrel{P}\longrightarrow X\pm Y$
*   $X_n Y_n\stackrel{P}\longrightarrow XY$
*   $P(Y≠0)=1$则$\frac{X_n}{Y_n}\stackrel{P}\longrightarrow\frac{X}{Y}$
*   $X_n\stackrel{d}\longrightarrow \xi, Y_n\stackrel{P}\longrightarrow c$，则$X_n+Y_n\stackrel{d}\longrightarrow\xi+c, \frac{X_n}{Y_n}\stackrel{d}\longrightarrow \frac{\xi}{c}$

*   【定理4.10】马尔科夫不等式：设$\xi$是定义在概率空间$(\Omega,\mathcal{F},P)$上的随机变量，$f(x)$是$[0,\infty)$上的非负单调不减函数，则对任意$x>0$，  
    

$P(|\xi|> x)\leq \frac{Ef(|\xi|)}{f(x)} \\$

*   【定理4.11】$\xi_n\stackrel{P}\longrightarrow\xi$当且仅当

$E\frac{|\xi_n-\xi|^2}{1+|\xi_n-\xi|^2}\rightarrow 0 \\$

**4.2.2 弱大数定律**

*   【定义4.4 服从弱大数定律】设$\{\xi_n\}$是定义在概率空间$(\Omega,\mathcal{F},P)$上的随机变量序列，如果存在常数列$\{a_n\}$和$\{b_n\}$，使得$\frac{1}{a_n}\sum_{k=1}^n\xi_k-b_n\stackrel{P}\longrightarrow  0$，则称$\{\xi_n\}$服从弱大数定律。  
    
*   【定理4.12】伯努利大数定律：设$\{\xi_n\}$是一列独立同分布的随机变量，$P(\xi_n=1)=p,P(\xi_n=0)$，记$S_n=\sum_{i=1}^n \xi_i$，则$\frac{S_n}{n}\stackrel{P}\longrightarrow p$  
    
*   【定理4.13】切比雪夫大数定律：设$\{\xi_n\}$是定义在概率空间$(\Omega,\mathcal{F},P)$上的随机变量序列，$E\xi_n=\mu_n, Var\xi_n=\sigma_n^2$，如果$\sum_{k=1}^n\sigma^2_k/n^2\rightarrow 0$，则$\{\xi_n\}$服从弱大数定律，即  
    

$\frac{1}{n}\sum_{k=1}^n\xi_k-\frac{1}{n}\sum_{k=1}^n\mu_k\stackrel{P}\longrightarrow 0 \\$

*   【定理4.14】辛钦大数定律：设$\{\xi_n\}$是定义在概率空间$(\Omega,\mathcal{F},P)$上的独立同分布的随机变量序列，$E|\xi_1|<\infty$，记$\mu=E\xi_1,S_n=\sum_{k=1}^n\xi_k$，则$\{\xi_n\}$服从弱大数定律，即$\frac{S_n}{n}\stackrel{P}\longrightarrow\mu$  
    
*   【定义4.5 r阶平均收敛】随机变量$E|\xi|^r<\infty$，$E|\xi_n|^r<\infty$，若$E|\xi_n-\xi|^r\rightarrow 0$，则$\{\xi_n\}$r阶平均收敛于$\xi$  
    

## 4.3 以概率1收敛与强大数定律

**4.3.1 以概率1收敛**

*   【定义4.6 几乎必然收敛/柯西基本列】设$\xi$和$\xi_n,n\geq 1$是定义在概率空间$(\Omega,\mathcal{F},P)$上的随机变量  
    

*   如果存在$\Omega_0\in\mathcal{F}$，使得$P(\Omega_0)=1$，且对任意$w\in\Omega_0$，有$\xi_n(w)\rightarrow\xi(w)$，则称$\xi_n$以概率1收敛/几乎必然收敛，记作$\xi_n\rightarrow\xi\ a.s.$
*   如果存在$\Omega_0\in\mathcal{F}$，使得$P(\Omega_0)=1$，且对任意$w\in\Omega_0$，数列$\{\xi_n(w)\}$是柯西基本列，即$\xi_n(w)-\xi_m(w)\rightarrow 0(n>m\rightarrow\infty)$，则称$\xi_n$以概率1是柯西基本列。

  

*   【定理4.15】  
    

*   $\xi_n\rightarrow\xi\ a.s.$当且仅当对任意$\epsilon>0$，$\lim\limits_{n\rightarrow\infty}P(sup_{k\geq n}|\xi_k-\xi|\geq\epsilon)=0$或$\lim\limits_{n\rightarrow\infty}P(\bigcup_{k\geq n}|\xi_k-\xi|\geq\epsilon)=0$
*   $\{\xi_n\}$以概率1是柯西基本列当且仅当对任意$\epsilon>0$，$\lim\limits_{n\rightarrow\infty}P(sup_{k\geq 0}|\xi_{k+n}-\xi_k|\geq\epsilon)=0$或$\lim\limits_{n\rightarrow\infty}P(\bigcup_{k\geq 0}|\xi_{k+n}-\xi_k|\geq\epsilon)=0$

*   【推论4.4】如果对任意$\epsilon>0, \sum_{n=1}^\infty P(|\xi_n-\xi|\geq\epsilon)<\infty$，则$\xi_n\rightarrow\xi\ a.s.$  
    

**4.3.2 强大数定律**

*   【定义4.7 强大数定律】设$\{\xi_n\}$是定义在概率空间$(\Omega,\mathcal{F},P)$上的随机变量序列，如果存在常数列$\{a_n\}$和$\{b_n\}$，使得$\frac{1}{a_n}\sum_{k=1}^n\xi_k-b_n\rightarrow 0\ a.s.$，则称$\{\xi_n\}$服从强大数定律。  
    
*   【定理4.16】波雷尔强大数定律：设$\{\xi_n\}$是定义在概率空间$(\Omega,\mathcal{F},P)$上的独立同分布的随机变量，$P(\xi_n=1)=p,P(\xi_n=0)$，记$S_n=\sum_{i=1}^n \xi_i$，则$\frac{S_n}{n}\rightarrow p\ a.s.$  
    
*   【定理4.17】柯尔莫哥洛夫强大数定律：设$\{\xi_n\}$是定义在概率空间$(\Omega,\mathcal{F},P)$上的独立同分布的随机变量，$E|\xi_1|<\infty$，记$\mu=E\xi_1,S_n=\sum_{k=1}^n\xi_k$，则$\frac{S_n}{n}\rightarrow\mu\ a.s.$

* * *