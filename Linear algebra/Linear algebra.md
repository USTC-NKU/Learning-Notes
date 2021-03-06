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
    $A^*$称为n阶矩阵A的**伴随矩阵**，**注意伴随矩阵中各个代数余子式与原矩阵位置是镜像的**，这意味第一行第二列元素$a_{12}$的代数余子式在伴随矩阵中的位置为第二行第一列
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
        设n阶矩阵 $A=(a_{ij})$ 的元都是复数，则矩阵
        $$\begin{aligned}
         \bar{A} = (\bar{a}_{ij})
        \end{aligned}$$
        称为A的**共轭矩阵**，共轭矩阵中的每个元均是原矩阵对应元的共轭复数
        * 若A,B均为n阶复矩阵，则下列等式成立
          * $\overline{A+B} = \bar{A}+\bar{B}$
          * $\overline{AB} = \bar{A}\bar{B}$
          * $\overline{\gamma A} = \bar{\gamma}\bar{A}$ $\quad$ ($\gamma$为复数)
          * $\overline{A^T} = (\bar{A})^T$
        * 若A是可逆矩阵，则A的共轭矩阵也是可逆矩阵，并且 $\overline{A^{-1}} = (\bar{A})^{-1}$
      * $\color{yellow}{埃尔米特矩阵}$
        若矩阵A满足 $A^T = \bar{A}$，则A称为**埃尔米特矩阵**，由定义易知埃尔米特矩阵主对角线上的元必定为实数，埃尔米特矩阵的行列式必为实数
      * $\color{yellow}{酉矩阵}$
        若n阶矩阵A满足条件 $A^T = \overline{A^{-1}}$ ,则A称为**酉矩阵**
        $$\begin{aligned}
         A\bar{A}^T = A\overline{A^T} = AA^{-1} = E
        \end{aligned}$$
        根据上式我们可以确定酉矩阵中任一行列各元的模的平方和等于1，任一行列的元与另一行列对应元的共轭数乘乘积为零.当酉矩阵中的元全为实数时，酉矩阵就是正交矩阵
***
## 分块矩阵
  * $\color{yellow}{分块矩阵定义}$
    一般地，对于任意一个 $m\times n$ 的矩阵A，可以用若干条水平和竖直直线按某种需要将A划分为若干个子阵，被划分了的矩阵A称为**分块矩阵**
  * $\color{yellow}{分块矩阵的运算}$
    * 分块矩阵的加法
      分块矩阵A,B能够进行加法的条件如下
      1. A,B矩阵为同型矩阵
      2. A,B采取完全相同的划分方式
    * 分块矩阵的数乘
      数乘分块矩阵等于数乘分块矩阵的每一个子块
    * 分块矩阵的转置
      分块矩阵的转置由两部构成
        1. 先将矩阵A按照转置规则进行转置
        2. 再对每个子块按照转置规则进行转置
    * 分块矩阵的乘法
      分块矩阵A,B能够相乘的条件如下
        1. 矩阵A的列数等于矩阵B的行数
        2. 矩阵A关于列的划分与矩阵B关于行的划分一致
           此后进行的乘法与矩阵的乘法规则无异  
  * $\color{yellow}{准对角矩阵}$
    * 准对角矩阵的形式
      $$\begin{pmatrix}
       A_1 & \\\\
           & A_2 \\\\
           &     &\ddots \\\\
           &     &      &A_s
      \end{pmatrix}$$
      形同上式的n阶矩阵A称为**准对角矩阵**，准对角矩阵上的各个子块均为方阵，，其余部分均为零矩阵
    * 准对角矩阵的性质
      * 两个同型的准对焦矩阵的乘积仍为准对角矩阵(这一点与我们之前在讲述对角矩阵时两个对角矩阵相乘的结果一致) 
      * 准对角矩阵可逆的充分必要条件是其各个子块均为可逆矩阵.其可逆矩阵的结果等于各个子块分别取可逆矩阵(这一点与我们讲对角矩阵时也一致)
      * (whatever,准对角矩阵看作对角矩阵也没啥大毛病，只不过元素是矩阵罢了) 
***
# 线性方程组
***
## 向量组与矩阵的秩
* $\color{yellow}{向量组的秩}$
  * $\color{yellow}{向量组的线性相关与线性无关}$
    * **定义1：线性相关**
      设 $a_1,a_2,\cdots a_s$ 为一组向量，若其中至少有一个向量可经过组内其余s-1个向量线性表出，则称该向量组是线性相关向量组，即这些向量是**线性相关**的，不能表出称为**线性无关**
    * **致命结论集合**
      1. 任何含零向量的向量组一定是线性相关的
      2. 一个线性相关的向量组再添加若干同维向量后亦然线性相关(部分相关则全体相关)
      3. 一个线性无关的向量组，从中抽取若干个向量组成的子向量组也必然线性无关(全体无关则部分无关)
    * **定理1**
      向量组 $a_1,a_2,\cdots a_s$ 线性相关的充要条件是至少存在一组不全为零的数 $\lambda_j$ 使得下式成立
      $$\begin{aligned}
       \sum_{j=1}^s \lambda_j a_j = \vec{0}
      \end{aligned}$$
      * 推论
        1. 向量组 $a_1,a_2,\cdots,a_s$ 线性无关的充要条件是当且仅当所有的 $\lambda_j$ 都为零时上式才能成立
        2. 向量组 $a_1,a_2,\cdots,a_s$线性无关，而向量组 $a_1,a_2,\cdots,a_s,\beta$ 线性相关，则向量 $\beta$ 必然可以经过向量组 $a_1,a_2,\cdots,a_s$ 线性表出，且表示式唯一
    * **定理2**
      n阶行列式
      $$\begin{aligned}
       \vert A \vert = \det (a_{ij}) = 0
      \end{aligned}$$
      的充分充分必要条件是，它的n个行(列)向量**线性相关**
      * 推论
        1. n阶行列式 $\vert A \vert \neq 0$ 的充要条件是其n个行(列)向量**线性无关**
        2. 任何n+1个n维行向量必线性相关 
        3. 根据定理1可知，任何含有非零向量的n维向量的向量组必然有线性无关子组，根据推论2可知，其任何线性无关子组的数目不超过n
    * **定义2：极大线性无关组**
      若向量组的一个子组线性无关，则将向量组中的任何一个向量添加到这个线性无关子组中，得到的新向量子组都是线性相关的子组，则称该线性无关子组为向量组的**极大线性无关组**
      * 推定
        1. 若一个向量组本身就是线性无关，则该向量组的极大线性无关组就是向量组本身.
        2. 仅有零向量的向量组不存在极大线性无关组
        3. 一般地，一个向量组的极大线性无关组不是唯一的
    * **定理3**
      对于一个确定的向量组，它的一切极大线性无关组中所含的向量个数相同，这是向量组线性相关性的内在属性
    * **定义3：秩**
      一个向量组的极大线性无关组所含向量的个数称为该向量组的**秩**，只含有零向量的向量组的秩为0
      * 推论
        1. 秩为r的向量组中，任何r+1个向量必然线性相关(参见定理2.推论2的表述)  
* $\color{yellow}{矩阵的秩}$
  * **定义1：k阶子式**
    在矩阵A中，位于k个不同行和不同列相交处的元构成的k阶行列式称为矩阵A的一个**k阶子式**
  * **定理1**
    矩阵A的行(列)秩等于A中一切非零子式的最高阶数  
  * **定理2**
    矩阵的行秩等于列秩，他们都等于矩阵中非零子式的最高阶数
  * **定义2：矩阵的秩**
    矩阵A的行秩，称为矩阵A的秩，记为 $r_A$，$r_A$ = 矩阵的行秩 = 矩阵的列秩 = 矩阵中非零子式的最高阶数
  * **定理3**
    $r_{AB}\leq\min(r_A,r_B)$ ,即矩阵乘积的秩不超过每个乘积因子的秩
    * 推论
      1. 设A为n阶可逆矩阵，$P = P_{m\times n}$,$Q = Q_{n\times p }$ ,则$r_{AQ} = r_{Q}$,$r_{AP} = r_{P}$,即任何矩阵乘可逆矩阵后其秩不变
      2. 初等变换不改变矩阵的秩(这是因为初等矩阵也是可逆矩阵)
  * **定义3：阶梯形矩阵**
    满足下列条件的矩阵称为行阶梯形矩阵，简称阶梯形矩阵
      1. 非零行的标号小于零行
      2. 设矩阵有r个非零行，第i个(i>1)非零行的第一个非零元必在前一行非零首元的右下侧,举个栗子
        $$\begin{pmatrix}
        1&1&1&1&1&1 \\\\
        0&0&1&1&1&1 \\\\
        0&0&0&1&1&1 \\\\
        0&0&0&0&0&0 \\\\
        \end{pmatrix}$$
    **阶梯形矩阵的秩等于它所含非零行向量的个数** 
    一般地，秩为r的矩阵必可以经过一系列初等行列变换化为Jordan标准型
    $$\begin{pmatrix}
    E_r & 0 \\\\
    0 & 0
    \end{pmatrix}$$
    $E_r$ 为r阶单位矩阵
  * **定理4**
    设 $A=(a_{ij})_{m\times n}$ 且 $r_A > 0$ 的充分必要条件是存在可逆矩阵 $P=P_{m\times m}$ 和 $Q=Q_{n\times n}$ 使得
    $$\begin{aligned}
     A = P\begin{pmatrix}
     E_r & 0 \\\\
     0 & 0
     \end{pmatrix}Q
    \end{aligned}$$  
***
## 线性方程组的解法
* $\color{yellow}{非齐次线性方程组的解法}$
  $$\begin{cases}
  k_{11}x_1+k_{12}x_2+\cdots+k_{1n}x_n=b_1 \\
  k_{21}x_1+k_{22}x_2+\cdots+k_{2n}x_n=b_2 \\
  \cdots \\
  k_{n1}x_1+k_{n2}x_2+\cdots+k_{nn}x_n=b_n \\
  \end{cases}$$
  当常数项向量为零向量时为**齐次线性方程组**，存在不为零常数为**非齐次线性方程组**
  上述方程组可以表示为矩阵乘法的形式(参见最开始介绍矩阵时所提) $AX = b$，前述所涉及的概念均不再赘述
  * **定理1**
    非齐次线性方程组有解的充要条件是系数矩阵的秩与增广矩阵的秩相同，即 $r_A = r_B$
  * **定理2**
    当 $r_A = r_B = n$ 时，非齐次线性方程组只存在唯一解；当 $r_A = r_B < n$ 时，方程组有无穷多解
  * $\color{yellow}{矩阵消元法}$
    使用**初等行变换**将方程组的增广矩阵化为阶梯形矩阵，即可运用定理1判断方程是否有解以及解的情况
* $\color{yellow}{齐次线性方程组的解法}$
  其解法服从非齐次方程组的解法，其次方程组必然有解
  * 齐次方程组必有零解
  * 当 $r_A = r_B = n$ 时，齐次线性方程组只存在唯一解零解；当 $r_A = r_B < n$ 时，方程组有无穷多解
  * 齐次方程组有非零解的充要条件是系数矩阵的行列式为零(联系克莱默法则)
***
## 线性方程组的解的结构
* $\color{yellow}{齐次方程组的基础解系}$
  * 定义
    齐次线性方程组解集合的一个极大线性无关子组，称为该齐次线性方程组的一个基础解系
  * 定理
    当 $r_A<n$ 时，齐次线性方程组的基础解系含有n-r个解向量
* $\color{yellow}{非齐次方程组的基础解系}$  
  * 定义
    非齐次线性方程组对应的齐次方程称为非齐次线性方程的**导出组**
  * 定理
    把非齐次线性方程组的一个特解$X_0$加入到其导出组的每个解向量上就得到非齐次线性方程的全部解向量，表示为
    $$\begin{aligned}
     X = X_0 + \sum_{i=1}^{n-r}k_iX_i
    \end{aligned}$$
***
# 线性空间
***
## 线性空间的概念
* $\color{yellow}{线性空间的概念组}$
  * **定义：数域**
    1. 数域是指这样的集合：它至少包含两个不同的数，并且对加减乘除四则运算是封闭的，即所得运算的结果仍然是该集合中的元素.由数域的定义可知，任何数域必然包括全体有理数
    2. 常见的数域有：有理数域Q，实数域R，复数域C，以下用F泛指一般的数域
  * **定义：线性空间**
    * 设V是一个非空集合，它的元以字母 $\alpha,\beta,\gamma\cdots$ 表示.又F是一个数域，其中的数用 $\lambda,\mu$ 等表示.具备下述条件的集合V成为线性空间
      1. 集合V中定义加法运算规则，由该规则运算V中任意两元，所得的结果属于V中元素，并且结果是唯一确定的，该加法运算规则需满足下列运算律
         * 交换律： $\alpha$ + $\beta$ = $\beta$ + $\alpha$
         * 结合律： ($\alpha$ + $\beta$) + $\gamma$ = $\alpha$ + ($\beta$ + $\gamma$)
         * 存在零向量，使得 $\vec{0}$ + $\alpha$ = $\alpha$ 
         * 存在每个向量的负向量，使得 $\alpha$ + (-$\alpha$) = $\vec{0}$
      2. 数域F中的数与V中的元定义数乘运算规则，使得对于任意属于F中的数和任意属于V中的元，其乘积结果仍然是V中的元，并且结果唯一确定，该数乘运算满足以下运算律
         * 幺元律 1$\alpha$ = $\alpha$
         * $\lambda(\alpha+\beta)$ = $\lambda \alpha$ + $\lambda \beta$
         * $(\lambda + \mu)\alpha = \lambda \alpha + \mu \alpha$
         * $\lambda(\mu \alpha) = (\lambda \mu)\alpha$
    * 加法运算和数乘运算合称为**线性运算**，称集合V所定义的线性运算构成数域F上的**线性空间**，V的元称为向量
* $\color{yellow}{子空间}$
  * **定义：子空间**
    设V是F上的线性空间，L是V的一个非空子集.如果L关于V中的加法与数乘运算也构成F上的一个线性空间，则L称为V的子空间
  * **定理**
    若L是V的非空子集且关于V的线性运算是封闭的，即若$\alpha,\beta \in L,\lambda \in F,则\alpha + \beta \in L,\lambda \alpha \in L$，则L是V的子空间   
***    
## n维线性空间
* $\color{yellow}{n维线性空间的定义}$
  * **定义**
    如果线性空间V中存在由n个向量构成的极大线性无关子组，则V称为**n维线性空间**.V的极大线性无关子组称为V的**基或基底**.基所含向量的个数就称为空间V的维度
    * 零空间的维度定义为零
    * 既非零空间又非n维空间的线性空间称为**无穷维空间**
  * **定理1**
    设$[\alpha_1,\alpha_2,\cdots\alpha_n]$是n维线性空间V的一个基，则V中的任何向量均可由基的向量线性表出，且表出形式是唯一的
  * **定理2**
    设在基$[\alpha_1,\alpha_2,\cdots\alpha_n]$下，n维线性空间V中的向量$\alpha ,\beta$的坐标分别为
    $$\begin{aligned}
     X = (a_1,a_2\cdots,a_n) \\\\
     Y = (b_1,b_2\cdots,b_n)
    \end{aligned}$$
    则向量$\alpha+\beta$等于对应位坐标之和，向量数乘的结果等于数乘以每个坐标分量
* $\color{yellow}{基变换与坐标变换}$
  * **定理**
    设$[\varepsilon_1,\varepsilon_2,\cdots,\varepsilon_n]$和$[\eta_1,\eta_2,\cdots,\eta_n]$是n维线性空间V的两个基底，向量$\alpha$在这两个基底下的坐标分别为X,Y，M为基$[\varepsilon_1,\varepsilon_2,\cdots,\varepsilon_n]$到基$[\varepsilon_1,\varepsilon_2,\cdots,\varepsilon_n]$的过渡矩阵，若基变换为
    $$\begin{aligned}
      [\eta_1,\eta_2,\cdots,\eta_n] = [\varepsilon_1,\varepsilon_2,\cdots,\varepsilon_n]M
    \end{aligned}$$ 
    则坐标变换公式为
    $$\begin{aligned}
     X = MY 
    \end{aligned}$$   
***
# 线性变换
***
## 线性变换的定义
* $\color{yellow}{定义1：映射}$
  设X,Y是两个非空集合.如果有一个确定的法则f,使得X中的每一个元x在f之下有集合Y中唯一确定的元y与之对应，则称此法则f是X到Y的一个**映射**，记为
  $$\begin{aligned}
   f：X\rightarrow Y
  \end{aligned}$$
  若X中的元x通过映射f得到Y中对应元y，则记为
  $$\begin{aligned}
   f：x\rightarrow y
  \end{aligned}$$
  我们称y是在映射f下元x的象，记为y=f(x)，而x称为y在映射f下的原象
* $\color{yellow}{定义2：变换}$
  设V是线性空间.V到自身的映射T称为V的一个**变换**，即$T：V\rightarrow V$,这时向量$\alpha\in V$在变换T之下的象$\beta$记为$T\alpha$,即$\beta = T\alpha$
* $\color{yellow}{定义3：线性变换}$
  设F上线性空间V有一个变换T，若T满足下面条件
   1. 对任意 $\alpha ,\beta \in V, T(\alpha+\beta) = T\alpha + T\beta$
   2. 对任意 $\alpha \in V, a \in F,T(a\alpha) = aT\alpha$ 
  则称T是线性空间V上的一个**线性变换**
* $\color{yellow}{定理}$
  线性空间V上的变换T是线性变换的充要条件是对任意数及V中的任意向量恒有
  $$\begin{aligned}
   T(a\alpha + b\beta) = aT\alpha + bT\beta
  \end{aligned}$$
* $\color{yellow}{线性变换的性质}$
  * 性质1： 线性变换T把零向量变为零向量
  * 性质2： 线性变换把原向量组$[\alpha_i]$的线性组合变为$[T\alpha_i]$的线性组合
  * 性质3： 线性变换不改变向量组的相关性
  * 性质4： 设T是线性空间V的线性变换.令$TV=(T\alpha:\alpha \in V)$是V的全体向量的象集合，则TV是V的子空间.称TV为线性变换T下V的**象子空间**
***
## n维线性空间V中线性变换的矩阵
* $\color{yellow}{线性变换在一个基下的矩阵}$
  * **定理1**
    设$[\varepsilon_1,\varepsilon_2,\cdots,\varepsilon_n]$是线性空间V的一个基，T是V上的线性变换，则线性变换T被该基的象$T\varepsilon_1,\cdots,T\varepsilon_n$所确定
  * **定理2**
    对于每个n阶矩阵A，在n维线性空间中必存在唯一的线性变换T，使得T在V中给定的基下的矩阵恰为A
  * **赠品**
    随手附赠变换$T\alpha$与$\alpha$在同一基底下其坐标之间的关系(因为疲于写逻辑关系所以下面推导会找不到逻辑词，但推导是渐进的)
    * $\alpha = \sum_{i=1}^n\varepsilon_i x_i$，$T\alpha = \sum_{i=1}^n\varepsilon_i y_i$
    * $T\alpha = T(\sum_{i=1}^n\varepsilon_i x_i)$
    * $T\alpha = [T\varepsilon_1,\cdots,T\varepsilon_n](x_1,\cdots,x_n)^T = [T\varepsilon_1,\cdots,T\varepsilon_n]X$
    * $T\varepsilon_j = [\varepsilon_1,\cdots,\varepsilon_n](a_{1j},\cdots,a_{nj})^T$
    * $T\alpha = [\varepsilon_1,\cdots,\varepsilon_n]\begin{pmatrix}
     a_{11} & a{12} & \cdots & a_{1n} \\\\
     \vdots & \vdots &   &\vdots \\\\
     a_{n1} & a_{n2} & \cdots & a_{nn}
    \end{pmatrix}X = [\varepsilon_1,\cdots,\varepsilon_n]AX$
    * $T\alpha = [\varepsilon_1,\cdots,\varepsilon_n]Y$
    * **Y = AX**
* $\color{yellow}{线性变换在不同基下矩阵之间的关系}$
  * $\color{yellow}{定义：矩阵相似}$
    设A，B是n阶矩阵，若存在满秩矩阵M，使 $B =M^{-1}AM$ 成立，则称矩阵A、B相似，记为A~B 
    * **矩阵相似的性质**
      1. 自反性：A~A
      2. 对称性：A~B 则 B~A
      3. 传递性：A~B B~C 则 A~C
***
## 矩阵的对角化
***
* $\color{yellow}{矩阵的特征值与特征向量}$
  * **定义1：特征值和特征向量**
    设$A=(a_{ij})$是n阶矩阵，若数$\lambda$和n维非零向量X使等式
    $$\begin{aligned}
     AX=\lambda X 
    \end{aligned}$$
    成立，则称$\lambda$是矩阵A的**特征值(特征根)**，X是A对应于$\lambda$的特征向量
  * **定理1**
    设$A=(a_{ij})$为n阶矩阵，则$\lambda$是A的特征值的充要条件是行列式
    $$\begin{aligned}
     \vert \lambda E -A\vert = 0
    \end{aligned}$$  
    而A的对应于特征值$\lambda$的特征向量是齐次线性方程组$(\lambda E - A)X = 0$的非零解向量
  * **定义2：特征方程**
    设$A=(a_{ij})$为n阶矩阵，方程
    $$\begin{aligned}
     \vert \lambda E -A\vert = 0
    \end{aligned}$$  
    称为矩阵A的**特征方程**，左侧行列式按幂从高到低展开形成的多项式称为**特征多项式**.
    矩阵A的特征值就是矩阵A特征方程的根，并由数学理论可知A的特征方程共有n个复特征根
* $\color{yellow}{矩阵的特征值与特征向量的性质}$
  * **定理2**
    相似矩阵具有完全相同的特征值
    * 定理表明如果矩阵A与对角矩阵相似，则该对角矩阵的主对角线上的全体元素便是A的全部特征值
    * 具有完全相同的特征值不能表明矩阵相似，因此定理2的逆定理是不成立的
  * **定理3**
    分块矩阵A的特征值由其各个子块的全部特征值构成
  * **定理4**
    设$\lambda_1,\lambda_2,\cdots,\lambda_r$是矩阵A的r个互不相同的特征值，$X_1,X_2,\cdots,X_r$为对应的特征向量，则$X_1,X_2,\cdots,X_r$线性无关
  * **定理5**
    设$\lambda_1,\lambda_2,\cdots,\lambda_k$是矩阵A的k个互不相同的特征值，$X_{j1},X_{j2},\cdots,X_{jr_j}$为A对应于特征值$\lambda_j$的$r_j$个线性无关的特征向量，则其全部特征向量构成的向量组必线性无关
  * **定理6**
    设$\lambda_0$是n阶矩阵A的k重特征值，则A的对应于$\lambda_0$的特征子空间的维数不超过k    
* $\color{yellow}{矩阵的对角化}$
  * **定理1**
    n阶**复矩阵**A与对角矩阵相似的充要条件是A由n个线性无关的特征向量
  * **定理2**(充分条件)
    n阶**复矩阵**A的特征值都是单根，则A必相似于对角矩阵
  * **定理3**
   n阶**复矩阵**A相似于对角矩阵的充要条件是对于每个$k_i$重特征值$\lambda_i$，矩阵$\lambda_iE - A$的秩等于$n-k_i$  
***
# 欧几里得空间
***
## 欧几里得空间
* $\color{yellow}{向量的标准内积}$
  * **定义1：标准内积**
    设V是实线性空间.若果对于任意一对向量按照某种法则在R中有唯一确定的实数，且满足下述运算律
    1. $<a,b> = <b,a>$
    2. $<a+b,c>=<a,c>+<b,c>$
    3. $<ka,b>=k<a,b>$
    4. $当a\neq0,<a,a>\quad>0$
    则实数$<a,b>$称为向量a与b的**标准内积**.定义了内积的实线性空间称为**欧几里得空间**，简称欧氏空间
  * **欧氏空间V内积的基本性质**
    1. 对于任意$\alpha \in V$,有$<\alpha,0>=0$
    2. 设$\alpha$为V中任一向量，若对V中任何向量都有二者内积为零，则$\alpha$为零向量
    3. 对于任意的$\alpha_i,\beta_j \in V$以及$a_i,b_j \in R$,恒有
       $$\begin{aligned}
        <\sum_{i=1}^la_i\alpha_i,\sum_{j=1}^tb_j\beta_j> = \sum_{i=1}^l\sum_{j=1}^ta_ib_j<\alpha_i,\beta_j>
       \end{aligned}$$
  * **定义2：模**
    $$\begin{aligned}
     \vert a\vert = \sqrt{<a,a>}
    \end{aligned}$$
    模长为1的向量称为单位向量
* $\color{yellow}{标准正交基}$
  * **定义：正交组**
    欧氏空间V中的一组两两正交的非零向量，称为V的一个**正交组**.若这个正交组中的每个向量都是单位向量，则称为**标准正交组**
    * 由正交组中向量构成的基底称为**正交基**，同理定义标准正交基
  * **定理1**
    欧氏空间中的正交组必为线性无关组
  * **定理2**
    设$[\alpha_1,\alpha_2,\cdots,\alpha_m]$是欧氏空间V的一组线性无关的向量，则存在一个正交组$[\beta_1,beta_2,\cdots,\beta_m]$，其中$\beta_k$是$\alpha_1,\alpha_2,\cdots,\alpha_k$的线性组合(k=1,2,...，m) 
    * 施密特正交化方法
      按照下述公式可以得到正交基，对得到的正交基单位化就可以得到标准正交基
      $$\begin{cases}
       \beta_1 = \alpha_1 \\\\
       \beta_k = \alpha_k - \sum_{j=1}^{k-1}\frac{<\alpha_k,\beta_j>}{<\beta_j,\beta_j>}\beta_j  \quad(k=2,3,\cdots,m)
      \end{cases}$$
***
## 正交变换
* $\color{yellow}{定义：正交变换}$
  设T是欧式空间V中的线性变换，如果对于任意的$\alpha \in V$,都有$\vert T\alpha\vert =\vert\alpha\vert$，则称T为**正交变换**
* $\color{yellow}{定理1}$
  欧氏空间V中的线性变换T为正交变换的充要条件是，对任意的$\alpha,\beta\in V$，有$<T\alpha,T\beta>=<\alpha,\beta>$
  * 推论
    设T为欧氏空间的正交变换，$\alpha,\beta\in V$，则向量夹角$\hat{(\alpha,\beta)} = \hat{(T\alpha,T\beta)}$
* $\color{yellow}{定理2}$
  设$[\varepsilon_1,\varepsilon_2,\cdots,\varepsilon_n]$是n维欧氏空间V的标准正交基，V中的线性变换T为正交变换的充要条件是$[T\varepsilon_1,T\varepsilon_2,\cdots,T\varepsilon_n]$也是标准正交基
* $\color{yellow}{定理3}$
  设$[\varepsilon_1,\varepsilon_2,\cdots,\varepsilon_n]$是n维欧氏空间V的标准正交基.V中的线性变换T是正交变换的充要条件是，T在标准正交基下的矩阵H是正交矩阵
***
# n元实二次型
***
## n元实二次型及其标准形
* $\color{yellow}{n元实二次型的定义}$
  * **定义1：实二次型**
    n个实变元的实系数二次齐次函数称为实数域上的**n元二次型**,简称实二次型   
    $$\begin{aligned}
     f(x_1,x_2,\cdots,x_n) = (x_1,x_2,\cdots,x_n)\begin{pmatrix}
     a_{11} & a_{12} & \cdots & a_{1n} \\\\
     a_{21} & a_{22} & \cdots & a_{2n} \\\\
     \cdots & \cdots &        & \cdots \\\\
     a_{n1} & a_{n2} & \cdots & a_{nn} \\\\
     \end{pmatrix}\begin{pmatrix}
     x_1 \\\\
     x_2 \\\\
     \vdots \\\\
     x_n
     \end{pmatrix}
    \end{aligned}$$
    简记为$f(x_1,x_2,\cdots,x_n)=X^TAX$,其中A是对称矩阵，**A的秩就称为二次型f的秩**
  * **定理**
    n元实二次型$X^TAX$可经过坐标变换X=CY化为二次型$Y^TBY$,其中$B=C^TAC$s
  * **定义2：合同矩阵**
    设A,B是数域F上的n阶矩阵.如果存在数域F上的可逆矩阵C，使得$B=C^TAC$成立，则称A与B是**合同矩阵**    
    * **合同矩阵的性质**
      1. A与A合同
      2. 若A与B合同，则B与A合同
      3. 若A与B合同，B与C合同，则A与C合同
      4. 合同矩阵有相同的秩
  * **定义3：二次型等价**
    如果两个实二次型$X^TAX$与$Y^TBY$可经过坐标变换互相转化，则称**两个二次型是等价**的 
    * **两个实二次型等价的充分必要条件是他们的矩阵是合同矩阵**
    * **两个实二次型等价的充分必要条件是他们拥有相同的秩和正惯性指数**
* $\color{yellow}{n元实二次型的标准形}$
  * **定义：标准形**
    只含变元平方项的二次型称为二次型的标准形
    $$\begin{aligned}
     f = \sum_{i=1}^nd_ix^2_i
    \end{aligned}$$ 
    * 可以看出，标准形的矩阵为对角阵，它的秩等于主对角线上非零元的个数
  * **定理1**
    秩为r的n元实二次型$f=X^TAX$必可经过坐标变换X=CY化为标准形.进一步，将所有系数转化为±1的标准形称为**规范形**
  * **定理2：惯性定理** 
    在秩为r的n元实二次型的标准形中,正平方项的个数t是唯一确定的，从而负平方项的个数也是唯一确定的
    * 我们称n元实二次型中正平方项的个数为该二次型的**正惯性指数**，负平方项的个数为二次型的**负惯性指数**
    * 正负惯性指数之差称为二次型的**符号差**
  * **定理3**
    秩为r的n阶对称矩阵A必合同于对角矩阵，及存在可逆矩阵C使得$C^TAC = diag(D)$ 
    * 可逆矩阵C的求解方式
      1. 将二次型的矩阵A与单位阵列排
        $$\begin{pmatrix}
        A \\\\ E 
        \end{pmatrix}$$
      2. 通过初等列变换和同类型的初等行变换将A化为单位矩阵，此时对单位矩阵只进行了列变换
         * 这里同类型的变换的意思是
           由于矩阵C可逆，那么C必然可以经由对单位矩阵的一系列初等变换得到(**忘了就去翻翻前文的说明吧**),因此$C=F_1F_2\cdots F_n$
           而$C^T = F^T_n\cdots F^T_2F^T_1$.而$F_i$和$F^T_i$是同一类初等变换，只不过二者的操作是镜像的，一个对行操作，那么另一个就对列操作
      3. 当将矩阵A变为对角矩阵时，单位矩阵就变成了所求的可逆矩阵
***
## 正定二次型
* $\color{yellow}{定义1：正定二次型}$
  若对任意X≠0，恒有$X^TAX>0$，则实二次型称为**正定二次型**，正定二次型的矩阵A称为**正定矩阵**,同理定义负定二次型和负定矩阵
* $\color{yellow}{定理1}$
  n元实二次型正定的充要条件是它的正惯性指数等于n
  * 推论1：n元实二次型负定的充要条件是它的负惯性指数等于n
  * 推论2：n元实二次型正定的**必要条件**是二次型的行列式大于零
* $\color{yellow}{定理2}$
  n元实二次型f正定的充要条件是它的矩阵A的左上角的各阶主子式都大于零 
  * 推论：n元实二次型f负定的充要条件是它的矩阵A的左上角的各阶主子式中，一切奇数阶的主子式都为负数，偶数阶都为正  
***
## 正交变化化二次型为标准形
* $\color{yellow}{定理1}$
  n阶对称矩阵的特征根必为实数
* $\color{yellow}{定理2}$
  设$\lambda_0$是n阶对称矩阵A的k重特征根，则A对应于$\lambda_0$的特征子空间的维数恰好等于k
* $\color{yellow}{定理3}$
  设$\lambda_1$与$\lambda_2$是对称矩阵A的互异特征根，$X_1$,$X_2$分别是对应的特征向量，则$X_1$,$X_2$正交
* $\color{yellow}{定理4}$     
  对n阶对称矩阵A，一定存在正交矩阵C使得
  $$\begin{aligned}
   C^TAC = C^{-1}AC=\begin{pmatrix}
   \lambda_1 \\\\
   & \lambda_2 \\\\
   & &\ddots \\\\
   & & & \lambda_n
   \end{pmatrix}
  \end{aligned}$$   
* $\color{yellow}{定理5}$
  任一个n元实二次型$f=X^TAX$必存在正交变换X=CY使该二次型被化为标准形，且矩阵C由对称矩阵A各个特征根对应的特征向量**标准单位化**后的$a_i$组成,$a_i$为按列向量排布，$C=(a_1,a_2,\cdots,c_n)$
