---
title: Linear algebra
math: true
tags: Linear algebra
categories: Math
---
  线性代数是数学的一个分支，它的研究对象是向量，向量空间（或称线性空间），线性变换和有限维的线性方程组。向量空间是现代数学的一个重要课题；因而，线性代数被广泛地应用于抽象代数和泛函分析中；通过解析几何，线性代数得以被具体表示。线性代数的理论已被泛化为算子理论。由于科学研究中的非线性模型通常可以被近似为线性模型，使得线性代数被广泛地应用于自然科学和社会科学中。
***
[toc]
***
# 行列式
***
## 行列式的定义
* $\color{yellow}{定义：逆序数}$
  * 定义
    对n个不同的正整数的一个排列，若某个数字的右边有r个比它小的数字，则称该数字在此排列中有r个逆序.一个排列中所有数字的逆序之和称为该排列的逆序数，排列$j_1j_2j_3...j_n$的逆序数记为$\tau(j_1j_2j_3...j_n)$
  * 按自然数大小顺序由小到大的排列称为自然排列或标准排列
* $\color{yellow}{定义：奇偶排列}$
  * 定义
    逆序数等于奇数的排列称为奇排列，逆序数等于偶数的排列称为偶排列，标准排列是偶排列
  * $\color{yellow}{对换}$
    把一个排列中某两个不同数字位置对换而其余数字不动，就得到一个新的排列.进行一次这样的操作称为一次对换.
* $\color{yellow}{引理}$
  * 表述
    对换改变排列的奇偶性，经过一次对换后，奇排列变为偶排列，偶排列变为奇排列.
* $\color{yellow}{定理}$
  * 表述
    n个不同的正整数的任意排列必然可以经过有限次对换变成标准排列，并且对换次数的奇偶性与该排列的奇偶性一致.
  * 推论
    标准排列经过奇数次对换后必然得到奇排列，经过偶数次变换必然经过偶排列.
* $\color{yellow}{定义：n阶行列式}$
  * 定义
    由$n^2$个数排成n行n列的表，并且在两边各画一道竖线的记号
    $$\left|
    \begin{array}{c}
      a_{11} & a_{12} &... & a_{1n} \\
      a_{21} & a_{22} &... & a_{2n} \\
      ...    & ...    &... & ...    \\
      a_{n1} & a_{n2} &... & a_{nn}
    \end{array}
    \right|$$   

  * n阶行列式的表示
    n阶行列式按行展开可以表示为
    $$\begin{aligned}
     \sum_{j_1j_2...j_n}(-1)^{\tau(j_1j_2...j_n)}a_{1j_1}a_{2j_2}...a_{nj_n}
    \end{aligned}$$
    按列展开这里略去，形式雷同.
* $\color{yellow}{特殊的行列式}$
  * 上三角行列式
    其特点是主对角线以下的元素全部为0，上三角行列式的值等于其主对角线上各个元素的乘积.
    $$\begin{aligned}
     sum = \prod_{i=1}^{n}a_{ii}
    \end{aligned}$$
  * 下三角行列式
    其特点是主对角线以上的元素全部为0，下三角行列式的**绝对值**等于其主对角线上各个元素的乘积，正负号与其排列的逆序数有关.  
     $$\begin{aligned}
     sum = (-1)^{\tau(n(n-1)...(2)(1))}\prod_{i=1}^{n}a_{ii} = (-1)^{\frac{n(n-1)}{2}}\prod_{i=1}^{n}a_{ii}
    \end{aligned}$$
***
## 行列式的性质
* $\color{yellow}{性质一}$
  * 行列式的行和列顺次互换，其值不变(行列式转置后，其值不变)
    $$\left|
    \begin{array}{c}
      a_{11} & a_{12} &... & a_{1n} \\
      a_{21} & a_{22} &... & a_{2n} \\
      ...    & ...    &... & ...    \\
      a_{n1} & a_{n2} &... & a_{nn}
    \end{array}\right|
        =
    \left|
    \begin{array}{c}
      a_{11} & a_{21} &... & a_{n1} \\
      a_{12} & a_{22} &... & a_{n2} \\
      ...    & ...    &... & ...    \\
      a_{1n} & a_{2n} &... & a_{nn}
    \end{array}
    \right|$$
 
  * 上式中的两个行列式互称为转置矩阵.其中一个行列式的n行恰好顺次为另一个行列式的n个列.行列式$\lvert A \rvert$的转置行列式称为$\lvert A^T \rvert$
  * 性质一表明行列式中的行和列的地位是一致的，对称的，因此对行成立的性质对列也成立
* $\color{yellow}{性质二}$
  * 互换行列式的两行(或两列)，行列式数值变号
* $\color{yellow}{性质三}$
  * 行列式中的某行(或某列)的各个元素含有公共因子K，则K可以提到行列式外
  * 用数K乘以该行列式，等于用数K乘以该行列式的某一行或某一列的各个元素
* $\color{yellow}{性质四}$
  * 若行列式中的某行(或某列)的元素均可以表示成两项之和，例如对第i行各个元素均有
    $$\begin{aligned}
     a_{ij} = b_{ij}+c_{ij}，\quad(j=1,2,...,n)
    \end{aligned}$$
    那么此行列式等于两个行列式的和，这两个行列式除第i行的元素分别为$b_{ij}$、$c_{ij}$外，其余元素均不变
  * 推广
    若某一行(或某一列)的元素可以表示为K个项之和，则原行列式等于这K个行列式的和
* $\color{yellow}{性质五}$
  * 满足以下条件之一的行列式的数值为0
    1. 行列式的某行或某列的元素全为0  
    2. 行列式中存在两行或两列完全相同
    3. 行列式的两行或两列的元素对应成比例
* $\color{yellow}{性质六}$
  * 若把行列式的某行(或某列)乘以K倍后加入到另一行(或另一列),行列式的数值不变
***
## 行列式的展开
* $\color{yellow}{余子式}$
  * 定义
    余子式 $M_{ij}$ 是把行列式$\lvert A \rvert$中元素 $a_{ij}$ 所在的行和列全部划去后所得到的n-1阶行列式. $M_{ij}$ 称为元素 $a_{ij}$ 在行列式 $\lvert A \rvert$ 中的余子式.
* $\color{yellow}{代数余子式}$   
  * 定义
    代数余子式 $A_{ij}$ = $(-1)^{i+j}M_{ij}$ ,称为元素 $a_{ij}$ 在行列式 $\lvert A \rvert$ 中的代数余子式.
  
* $\color{yellow}{定理1}$
  * n阶行列式(n≥2)等于它的任一行的各元与其代数余子式的乘积   
    $$\begin{aligned}
     \vert A \vert = \sum_{k=1}^{n}a_{ik}A_{ik}
    \end{aligned}$$  
  * 由于行与列的地位等价，所以以列写也成立吖
* $\color{yellow}{定理2}$
  * n阶行列式等于它的任一列的各元与其代数余子式的乘积
* $\color{yellow}{定理3}$  
  * n阶行列式的任一行的各元与另一行对应元的代数余子式的乘积之和为零
  $$\begin{aligned}
     \sum_{k=1}^{n}a_{jk}A_{ik} \equiv 0  \quad(i≠j)
    \end{aligned}$$  
  * 关于证明，小提一下：
    * 这里相当于将第j行的各个元素填充到第i行上面，然后行列式中就存在两行完全相同，根据前述性质可知行列式的数值为零 
* $\color{yellow}{定理4}$  
  * n阶行列式的任一列的各元与另一列对应元的代数余子式的乘积之和为零
* $\color{yellow}{范德蒙德行列式}$  
  * 内容
    $$\left|
    \begin{matrix}
      1 & 1 & 1 & ... & 1 \\
      x_1 & x_2 & x_3 &... & x_n \\
      x^2_1 & x^2_2 & x^2_3 &... & x^2_n \\ 
      ... \\
      x^{n-1}_1 & x^{n-1}_2 & x^{n-1}_3 &... & x^{n-1}_n \\
    \end{matrix}
    \right|
     = \prod_{1\leq j\leq i\leq n}(x_i - x_j)$$
* $\color{yellow}{拉普拉斯定理}$
  * 定义
    在n阶行列式中，任意指定r个行与r个列，位于这些行列交点处的元素构成的r阶行列式M称为原行列式的一个r阶子式，划去某个r阶子式后剩下的n-r个行与列上的元素也构成一个子式N，我们称这一对子式M、N互为余子式
    此外，我们称带有正负号的余子式A为代数余子式.例如我们指定r行元素构成子式M，那么
    $$\begin{aligned}
     (-1)^{\sum_{k=1}^r i_k + \sum_{k=1}^{r}j_k}\cdot N
    \end{aligned}$$
    就是M的代数余子式
  * 拉普拉斯定理
    在n阶行列式中任意选定k个行(列)，则n阶行列式等于位于这K个行(列)中的一切k阶子式 $M_i$, (i=1,2,3...$C_n^k$)与其对应代数余子式 $A_i$乘积的和
    $$\begin{aligned}
     \vert A \vert = \sum_{i=1}^{C_n^k}M_iA_i
    \end{aligned}$$   
***
# 矩阵
***
## 矩阵的定义
* $\color{yellow}{定义1}$  
  * 由m$\times$n个数(实数或复数都可)排成的m行n列的数表称为m行n列矩阵，简称矩阵.
  * 当一个矩阵的行数和列数相等时，该矩阵称为方阵.
  $$\begin{pmatrix} a_{11} & a_{22} & \cdots &a_{1n} \\ a_{21} & a_{22} & \cdots & a_{2n} \\ \vdots & \vdots & \vdots &\vdots \\ a_{m1} & a_{m2} &\cdots &a_{mn}\end{pmatrix}$$
* $\color{yellow}{定义2}$
  * 如果矩阵A的每一个元素都是实数，则矩阵A是实矩阵；如果矩阵A中存在元素是复数，则矩阵A称为复矩阵  
* $\color{yellow}{定义3}$
  * 如果矩阵A与矩阵B有相同的行数和列数，则A与B称为**同型矩阵**   
* $\color{yellow}{几种矩阵}$  
  $$\begin{cases}
  k_{11}x_1+k_{12}x_2+\cdots+k_{1n}x_n=b_1 \\
  k_{21}x_1+k_{22}x_2+\cdots+k_{2n}x_n=b_2 \\
  \cdots \\
  k_{m1}x_1+k_{m2}x_2+\cdots+k_{mn}x_n=b_m \\
  \end{cases}$$
  * 由方程组中未知量的系数构成的矩阵称为**系数矩阵**
    $$A = \begin{pmatrix}
     k_{11} & k_{12} &\cdots &k_{1n} \\\\
     k_{21} & k_{22} &\cdots &k_{2n} \\\\
     \vdots & \vdots &       &\vdots \\\\
     k_{m1} & k_{m2} &\cdots &k_{mn} \\\\
    \end{pmatrix}$$
  * 有方程组右端中的常数项构成的矩阵为**常数列矩阵**
    $$b = \begin{pmatrix}
     b_1 \\\\ b_2 \\\\ \vdots \\\\ b_m
    \end{pmatrix}$$
  * 由系数和常数项构成的矩阵称为**增广矩阵**
  * 只有主对角线上存在元素而其余位置全为零的矩阵称为**对角矩阵**，显然对角矩阵是方阵
    $$diag(A) = \begin{pmatrix}
     \lambda_1 & 0 &\cdots & 0 \\\\
     0 & \lambda_2 &\cdots & 0 \\\\
     \vdots & \vdots &     &\vdots \\\\
     0 & 0 & \cdots &\lambda_n
    \end{pmatrix}$$
  * 特别地，主对角线上的元素全是1的对角阵称为**单位矩阵E**，所有元素全为0的矩阵称为**零矩阵**
  * 我们把1$\times$n矩阵称为n维行向量，同理定义n维列向量
***
## 矩阵的运算
* $\color{yellow}{矩阵加减法与数乘}$
  * $\color{yellow}{定义1}$    
    如果同型矩阵A、B的每一个对应元素都相等，则矩阵A=B
  * $\color{yellow}{定义2}$
    两个同型矩阵 $A = (a_{ij})_{m\times n} $,$B = (b_{ij})_{m\times n} $ 的对应元素相加所得的同型矩阵C称为矩阵A与B的和
    显然非同型矩阵的加法是毫无意义的
  * $\color{yellow}{定义3}$
    若矩阵A、B对应位置的每个元素互为相反数，则称矩阵B是矩阵A的负矩阵
  * $\color{yellow}{定义4}$
    同型矩阵A、B的差记为A - B = A + (-B)，显然A=B的充要条件是A-B=0(这里的0指的是零矩阵而非数字零)
  * $\color{yellow}{定义5}$
    若$\lambda$是一个数，A = $(a_{ij})_{m\times n}$是一个矩阵，则同型矩阵$(\lambda a_{ij})_{m\times n}$ 称为数$\lambda$与矩阵A的乘积
    根据定义，矩阵的数乘显然是矩阵中的每一个元素都乘以这个数，这与行列式极为不同!
   
  * $\color{yellow}{矩阵线性运算的性质}$
    * 满足加法交换律
    * 满足加法结合律
    * 满足数乘分配律
    * 满足数乘结合律
* $\color{yellow}{矩阵的线性组合}$
  * 线性组合是**同型矩阵**中最基本的运算，给定n个矩阵$A_i$,经过线性运算得到的矩阵B称为矩阵$A_i$的线性组合.也即矩阵B可经矩阵$A_i$线性表出
    $$\begin{aligned}
     B = \sum_{i=1}^{n}\lambda_i A_i
    \end{aligned}$$
* $\color{yellow}{矩阵的乘法}$
  * $\color{yellow}{定义1：矩阵与列向量的乘积}$
    * 设A = $(a_{ij})_{m\times n}$ ，C = $(c_j)_{n\times 1}$ ，规定m$\times$n矩阵A与n维列向量的乘积AC是以 $d_i = \sum_{j=1}^{n}a_{ij}c_j$ 为分量的m维列向量
    $$AC = \begin{pmatrix}
     a_{11} & a_{12} & \cdots & a_{1n} \\\\
     a_{21} & a_{22} & \cdots & a_{2n} \\\\
     \vdots & \vdots &        & \vdots \\\\
     a_{m1} & a_{m2} & \cdots & a_{mn} \\\\
    \end{pmatrix}
    \begin{pmatrix}
     c_1 \\\\
     c_2 \\\\
     \vdots \\\\
     c_n
    \end{pmatrix} =
    \begin{pmatrix}
    a_{11}c_1+a_{12}c_2+\cdots +a_{1n}c_n \\\\
    a_{21}c_1+a_{22}c_2+\cdots +a_{2n}c_n \\\\
    \vdots \\\\
    a_{m1}c_1+a_{m2}c_2+\cdots +a_{mn}c_n \\\\
    \end{pmatrix}$$
    * 矩阵能与列向量相乘的条件是矩阵的列数与列向量的行数要相等
  * $\color{yellow}{定义2：矩阵与矩阵的乘积}$ 
    * 矩阵A,B之间的乘积是由A的第i个行向量与B的第j个列向量的对应分量乘积之和，矩阵A、B能够相乘的条件依然是A的列数等于B的行数，公式就不再打出
      **不同型矩阵的乘法无意义，同型的乘法一般也不满足交换律，即一般来说矩阵乘法中AB≠BA**
    * 矩阵乘法AB描述为A右乘B或者B左乘A
    * 若AB = 0(矩阵乘积中的0均为零矩阵，此后不再强调)，不能得到A=0或者B=0
    * **矩阵乘法不满足消去律**，即由AB=AC且A≠0不能推导出B=C
    * 当A是方阵时，k个A相乘称为A的k次幂，记为 $A^k$ ，并约定A的零次幂为单位矩阵E
    * 由于矩阵不满足乘法交换律，一般地，$(AB)^k \neq A^kB^k$, A、B皆为方阵并且k≥2 
  * $\color{yellow}{矩阵乘法的性质}$
    * 矩阵乘法符合结合律
    * 矩阵乘法符合分配律
    * 矩阵乘法满足与数的乘法结合律
* $\color{yellow}{n阶矩阵乘积的行列式}$
  * $\color{yellow}{定理}$
    若A与B皆为n阶方阵，那么以下公式成立
    $$\begin{aligned}
     \vert AB \vert = \vert A \vert  \vert B \vert
    \end{aligned}$$
    并且 $\vert AB \vert = \vert BA \vert$
***
## 逆矩阵与矩阵初等变换
* $\color{yellow}{逆矩阵}$
  * $\color{yellow}{可逆矩阵}$
    设A是一个n阶矩阵.若存在n阶矩阵B使得 AB = BA =E 成立，则称A是**可逆矩阵**，B是A的逆矩阵，当然A也是B的逆矩阵，由此可以得出**只有方阵才能够存在逆矩阵**，互为可逆矩阵交换顺序不产生任何影响
    * 可逆矩阵又称为**非奇异矩阵、满秩矩阵、非退化矩阵**
  * $\color{yellow}{定理1}$
    若A是可逆矩阵，则A的逆矩阵是唯一的.
    * 由于A的可逆矩阵是唯一的，我们用$A^{-1}$记为A的逆矩阵，即 $AA^{-1} = A^{-1}A = E$ 
  * $\color{yellow}{定理2}$
    矩阵A可逆的充分必要条件是矩阵A对应的行列式 $\lvert A \rvert$ 的数值 $\neq 0$ 
  * $\color{yellow}{伴随矩阵}$
    用矩阵A中各元素的代数余子式为元构成矩阵
    $$A^* = \begin{pmatrix}
    A_{11} & A_{21} & \cdots & A_{n1} \\\\
    A_{12} & A_{22} & \cdots & A_{n2} \\\\
    \vdots & \vdots &        & \vdots \\\\
    A_{1n} & A_{2n} & \cdots & A_{nn}
    \end{pmatrix}$$
    $A^*$称为n阶矩阵A的**伴随矩阵**
    * $AA^* = A^*A$
    * $AA^* = \vert A \vert E$
    * $A^* = A^{-1}\vert A \vert$
  * $\color{yellow}{定理3}$
    若A与B均为n阶可逆矩阵，则矩阵AB也为n阶可逆矩阵，并且 $(AB)^{-1} = B^{-1}A^{-1}$
    * $\color{yellow}{推论}$
      若 $A_1,A_2,A_3...,A_m$ 均为n阶可逆矩阵，则乘积 $A_1A_2A_3...A_m$ 也是一个n阶可逆矩阵并且 $(A_1A_2A_3...A_m)^{-1} = A^{-1}_m...A^{-1}_2A^{-1}_1$
  * $\color{yellow}{定理4}$
    设A是n阶可逆矩阵，那么对于任意的 $B = B_{n\times m}$，矩阵方程 $AX=B$ 有唯一解 $X=A^{-1}B$
  * $\color{yellow}{定理5：克拉默法则}$
    * n元线性方程组
      $$\begin{cases}
      k_{11}x_1+k_{12}x_2+\cdots+k_{1n}x_n=b_1 \\
      k_{21}x_1+k_{22}x_2+\cdots+k_{2n}x_n=b_2 \\
      \cdots \\
      k_{n1}x_1+k_{n2}x_2+\cdots+k_{nn}x_n=b_n \\
      \end{cases}$$
      当其系数矩阵的行列式数值不为零时($D = \vert A \vert \neq 0$)，线性方程组存在唯一解
      $$ x_j = \frac{1}{\vert A \vert}
      \begin{vmatrix}
       k_{11} & \cdots k_{1,j-1} & b_1 & k_{1,j+1} & \cdots & k_{1n} \\\\
       k_{21} & \cdots k_{2,j-1} & b_2 & k_{2,j+1} & \cdots & k_{2n} \\\\
       \vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\\\
       k_{n1} & \cdots k_{n,j-1} & b_n & k_{n,j+1} & \cdots & k_{nn} \\\\
      \end{vmatrix} = \frac{D_j}{D}$$
      $D_j$表示把系数矩阵A中的第j列对应替换为常数项列后得到的矩阵的行列式
* $\color{yellow}{矩阵的初等变换}$
  * $\color{yellow}{定义}$
    * 对矩阵的行(列)施行下列三种变换都称为**矩阵的初等行(列)变换**
      * 互换矩阵两行(列)的位置所得到的初等矩阵 $E_{ij}$
      * 用非零常数$\lambda$乘以矩阵的某行(列)所得到的初等矩阵 $E_{ii}(\lambda)$
      * 将矩阵某行(列)的$\lambda$倍加到矩阵的另一行(列)上所得到的初等矩阵 $E_{ij}(\lambda)$
        矩阵的初等行变换和初等列变换统称为**初等变换**
    * 对n阶单位矩阵E施行一次上述三种初等变换的一种后所得到的矩阵称为**初等矩阵**.初等矩阵共有三种，初等矩阵显然是方阵，并且三种初等矩阵是可逆矩阵，并且初等矩阵的逆矩阵仍然为初等矩阵.三种初等矩阵对应的逆矩阵分别为
    $$\begin{cases}
    (E_{ij})^{-1} = E_{ij} \\\\
    (E_{ii}(\lambda))^{-1} = E_{ii}(\frac{1}{\lambda}) \\\\
    (E_{ij}(\lambda))^{-1} = E_{ij}(-\lambda)
    \end{cases}$$
  * $\color{yellow}{引理}$
    对 $m\times n $ 矩阵A施行某一种初等行(列)变换，其结果等于对矩阵A左乘(右乘)一个相应的m阶(n阶)初等矩阵
  * $\color{yellow}{定理}$
    可逆矩阵必可以表示为若干个初等矩阵的乘积
    * 可以证明，若A是一个n阶可逆矩阵，则必可以经过一系列初等变换将A化为单位矩阵
      $$\begin{aligned}
       F_m...F_2F_1A = E_n
      \end{aligned}$$
      由此式可知
      $$\begin{aligned}
       F_m...F_2F_1E_n = A^{-1}
      \end{aligned}$$
      表明对矩阵A和单位矩阵进行完全相同的一系列初等变换，当矩阵A 被化为单位矩阵E后，单位矩阵就被化为了矩阵A对应的逆矩阵
* $\color{yellow}{转置矩阵与一些重要方阵}$
  * $\color{yellow}{转置矩阵}$
    设A是一个 $m\times n$ 矩阵，将A的行顺次改成列，所得到的 $n\times m$矩阵称为A的**转置矩阵**，记作 $A^T$ (形式上可以参见行列式的转置)
    * $\color{yellow}{转置矩阵的运算规律}$
      * $(A^T)^T = A$
      * $(A\pm B)^T$ = $A^T \pm B^T$
      * $(\lambda A)^T$ = $\lambda A^T$
      * $(AB)^T$ = $B^TA^T$
      * 若A是可逆矩阵，则 $(A^T)^{-1} = (A^{-1})^T$
  * $\color{yellow}{几个重要方阵}$
    * $\color{yellow}{对称矩阵}$
      若实矩阵A满足 $A^T = A$ ，则称A为对称矩阵，对称矩阵必然为方阵，对称矩阵以主对角线为轴，镜像位置上的元素相同
    * $\color{yellow}{反称矩阵}$
      若实矩阵A满足 $A^T = -A$ ，则称A为反称矩阵，反称矩阵必然为方阵.容易知道反称矩阵的主对角线上的元素均为0.镜像位置上的元素互为相反数.**奇数阶的反称矩阵的行列式必然为零**
    * $\color{yellow}{对角矩阵}$
      除主对角线上的元素外其余元素均为0的方阵称为对角阵
      * $\color{yellow}{对角阵的性质}$
        * 若A、B均为n阶对角阵，则 $A+B,\lambda A,AB$ 皆为对角矩阵，且AB=BA，并且A、B矩阵相乘得到的矩阵等于主对角线上对应位置的元素相乘形成的n阶矩阵
        * **对角矩阵相乘是可交换的** 
        * 对角矩阵可逆的充分必要条件是其主对角线上不存在为0的元素，对角矩阵的逆矩阵也是对角矩阵，并且其主对角线上各元素恰好是对应各元素的倒数
     * $\color{yellow}{正交矩阵}$
       若n阶实矩阵满足 $A^TA = E$,则A称为**正交矩阵**
       * 显然，正交矩阵是可逆矩阵，并且 $A^T = A^{-1}$,这也是n阶矩阵A为正交矩阵的充分必要条件
       * 若A为正交矩阵，则A的转置矩阵和逆矩阵均为正交矩阵
       * A为正交矩阵，则A的行列式的数值必为±1中的一个，即 $\vert A = 1 \vert$ 或 $\vert A = -1 \vert$
       * 有限多个同阶正交矩阵的乘积仍然是正交矩阵，但其和形成的矩阵一般不是正交矩阵
      * $\color{yellow}{共轭矩阵}$
      * $\color{yellow}{埃尔米特矩阵}$
    