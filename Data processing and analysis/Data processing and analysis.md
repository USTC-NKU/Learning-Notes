# Data processing and analysis 数据处理与分析
---
**$$\begin{aligned}Organized\quad in\quad NKU \end{aligned}$$**
***
[toc]
---

## 误差

---
### 绝对误差
* **绝对真误差**
  误差$\delta_x = x -a$是与测量值同量纲的，直接反映测量值的绝对值大小和方向的误差
* **总体方差与标准误差**
  1. 无限次测量所获得的全部测量误差的平方均值$\sigma^2$称为==总体误差==。
  2. 总体误差的算术平方根称为总体==标准误差==。正态分布总体中每一个测量值的标准误差均为：
  **$$\begin{aligned} \sigma_{xi} = [\sum_{i=1}^{n}\delta^2_{xi}/n]^{\frac{1}{2}} = [\sum_{i=1}^{n}(x_i - a)^2/n]^{\frac{1}{2}} \end{aligned}$$**
  3. ==算术平均值的标准误差==是标准误差$\sigma_{xi}$的$\frac{1}{\sqrt{n}}$,即：
   $$\begin{aligned}
   \sigma_{\bar{x}} = \frac{\sigma_{xi}}{\sqrt{n}}
   \end{aligned}$$
  4. ==残差==是每一个测量值与样本平均值的差,即:
   $$\begin{aligned}
       v_{xi} = x_i - \bar{x}
   \end{aligned}$$
* **样本方差与样本标准偏差**
     * ==样本标准偏差==
     $$\begin{aligned}
         s_{xi} = [{\sum_{i=1}^{n}v_{xi}^2}/(n-1)]^{\frac{1}{2}} = [\sum_{i=1}^{n}(x_i - \bar{x})^2/(n-1)]^{\frac{1}{2}}
     \end{aligned}$$
     * ==样本方差==
     样本标准偏差的平方即为样本方差
     * ==算术平均值的标准偏差==
     算术平均值的标准误差是样本标准偏差的$s_{xi}$的$\frac{1}{\sqrt{n}}$
### 相对误差
* **相对误差**
  相对误差$E_x$等于x的测量误差与其绝对量值之比
  $$\begin{aligned}
      E_x = \frac{\delta_x}{x}
  \end{aligned}$$ 
---

## 不确定度
---
### 直接测量下A类不确定度
* 情况一：**多次测量**
  在相同条件下对某物理量进行n次测量后，应由其最佳估计值$\bar{x}作为测量结果，$其A类不确定度为：
  $$\begin{aligned}
     \mu_{Ax} =  \sigma_{\bar{x}} = t(p,k)s_{\bar{x}}
  \end{aligned}$$
  其自由度 k= n - 1，n是所测量的样本的个数，t(p,k)中p是置信度，根据测量时选取的置信概率和自由度经查表可以得到t(p,k)的数值.$s_{\bar{x}}$是样本的算术平均标准偏差，算术平均值的标准误差是样本标准偏差的$s_{xi}$的$\frac{1}{\sqrt{n}}$
* 情况二：**单次测量**
  单次测量所得到的A类不确定度等于其样本标准偏差$s_{xi}$
  $$\begin{aligned}
     \mu_{Ax} = s_{xi}
  \end{aligned}$$
### 直接测量的B类不确定度
* 情况一：**单次测量**
  单次测量的B类不确定度计算公式为：
  $$\begin{aligned}
      U_{Bx} = \Delta_x/c_{(1)}
  \end{aligned}$$
  其中$\Delta_x$是仪器的允差，$c_{(1)}$是置信概率为1时的覆盖因子，对一些完全不知道其分布的误差，均假设他们服从均匀分布.
  不同分布对应的覆盖因子数值不同：
     ==1. 正态分布==  $c_{(1)}$ = 3
     ==2. 均匀分布==  $c_{(1)}$ = $\sqrt{3}$
     3. 三角分布  $c_{(1)}$ = $\sqrt{6}$
    ==4. 两点分布==  $c_{(1)}$ = 1
     5. 反正弦分布 $c_{(1)}$ = $\sqrt{2}$

* 情况二：**多次测量**
  多次测量遵从均匀分布，设仪器的分辨率为$\varepsilon_x$,B类不确定度为：
  $$\begin{aligned} U_{Bx} = \varepsilon_x / \sqrt{3}  \end{aligned}$$

### 间接测量不确定度估计
* **广义方和根**
  对于间接测量，我们通常采用间接合成的方式计算不确定度，其步骤如下：
     **1. 求全微分，或者先取对数再继续进行全微分**.
     **2. 合并同一微分量的系数**
     **3. 逐项平方，并且将微分符号d改写为标准不确定度的符号“u”。各个平方项之间用“+”连接，最后等式两端开平方根就可以得到不确定度**.
  用公式表征即为：
  $$\begin{aligned}
     U_N = \sqrt{\sum_{j=1}^{m}(\frac{\partial N}{\partial x_j}\cdot u_{xj})^2} 
  \end{aligned}$$
---
## 有效数字原则
---
### 有效数字的运算法则
1. 尾数舍入规则：
   ==小于5舍去，大于5进位，等于5时将尾数凑成偶数==
   例如：4.1868取四位有效数字即为4.187；1.63500取三位有效数字即为1.64; 1.64500取三位有效数字即为1.64
2. 四则运算规则：
   加减法：==加减法运算采取尾数对齐的法则==
   乘除法：乘除法的运算结果应比==参与运算的各个分量中，有效数字位数最少的数多去一位==
---
## 最常用的数据分析方法
1. 环差法(逐差法)
2. 最小二乘法
$$
\left\{\begin{array}{l}
b=\frac{\sum_{i=1}^{n}\left(x_{i}-x\right)(y,-y)}{\sum_{i=1}^{n}\left(x_{i}-x\right)^{2}}=\frac{\sum_{i}^{*} x_{1} y_{1}-n x y}{\sum_{i=1}^{4} x_{i}^{2}-n x^{2}} \\
a=y-b x .
\end{array}\right.
$$
此外，可以借助包括Excel，mathematics，matlab等具有数据处理与分析能力的软件进行更为复杂的数据分析