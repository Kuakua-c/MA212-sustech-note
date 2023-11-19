
# 3-1,3-2

## 3-1,introduction

- 同一变量不同指标间存在联系，为了计算有关数据，我们会把它们放在一起考虑

### 二维随机变量

- 设 $\Omega$ 为样本空间, $X=X(\omega), Y=Y(\omega) \quad(\omega \in \Omega)$是定义在 $\Omega$ 上的两个r.v, 记

$$
(X, Y) \triangleq(X(\omega), Y(\omega)) \quad(\omega \in \Omega)
$$

- 称 $(X, Y)$ 为二维随机变量 (向量).
- 直观上来看，试验在二维随机变量的实验结果，可以是二维平面中得一个随机点的产生

#### 二维随机变量下，联合累积分布函数

- 定义 设 $(X, Y)$ 为二维r.v, $\forall x, y \in(-\infty, \infty)$, 定义

$$
\begin{aligned}
F(x, y) & \triangleq P(\{X \leq x\} \cap\{Y \leq y\}) \\
& \triangleq P\{X \leq x, Y \leq y\}
\end{aligned}
$$

- 则称 $F(x, y)$ 为二维 r.v $(X, Y)$ 的累积分布函数, 或称为 $X$ 与 $\boldsymbol{Y}$ 的联合累积分布函数.
- <span style="color:red">$\begin{aligned}P\{x_1<X\leq x_2,y_1<Y\leq y_2\}=F(x_2,y_2)-F(x_1,y_2)-F(x_2,y_1)+F(x_1,y_1)\geq0\end{aligned}$
- 性质（**为本质特征，可以用于证明为二维分布函数**）：

1. 任意固定 $x_0, F\left(x_0, y\right)$ 是 $y$ 的单调不减函数；任意固定 $y_0, F\left(x, y_0\right)$ 是 $x$ 的单调不减函数
2. $0 \leq F(x, y) \leq 1$, 且

$$
\begin{aligned}
& F(+\infty,+\infty)=1, F(-\infty,-\infty)=0 \\
& F(-\infty, y)=0, F(x,-\infty)=0 \quad(\forall x, y)
\end{aligned}
$$

3. $F(x, y)=F(x, y+0)$, 即 $F(x, y)$ 关于 $y$ 右连续 $F(x, y)=F(x+0, y)$, 即 $F(x, y)$ 关于 $x$ 右连续
4. $\forall x_1<x_2, y_1<y_2$ 有（**与上三条同等存在，无法由上三条推出**）

$$
\begin{aligned}
& F\left(x_2, y_2\right)-F\left(x_1, y_2\right)-F\left(x_2, y_1\right)+F\left(x_1, y_1\right) \geq 0 \\
& =P\left\{x_1<X \leq x_2, y_1<Y \leq y_2\right\}
\end{aligned}
$$

### n维上随机变量，随机向量推广

- 设 $X_1, X_2, \cdots, X_n$ 是定义在样本空间 $\Omega$ 上的 $n$ 个r.v, 则称

$$
\left(X_1, X_2, \cdots, X_n\right)
$$

为 $n$ 维随机变量或 $n$ 维随机向量.
称 $\boldsymbol{n}$ 元函数

$$
F\left(x_1, x_2, \cdots, x_n\right)=P\left\{X_1 \leq x_1, X_2 \leq x_2, \cdots, X_n \leq x_n\right\}
$$

为 $n$ 维随机向量 $\left(X_1, X_2, \cdots, X_n\right)$ 的分布函数, 或称为 r.v $X_1, X_2, \cdots, X_n$ 的联合分布 (函数).

### 边缘分布

- 如果 $(X, Y)$ 是一个二维随机变量, 则它的分量 $X$ (或者 $Y$ ) 是一维随机变量, 因此, 分量 $X$ (或者 $Y$ )也有分布. 我们称 $X$ (或者 $Y$ )的分布为 $X$ (或者 $Y$ )关于二维随机变量 $(X, Y)$ 的边缘分布.
- 边缘分布也称为边沿分布或边际分布
- $\begin{aligned}&\text{称}F_X(x)\text{为}(X,Y)\text{关于}X\text{的边际分布}(\text{函数})\\&\text{称 }F_Y(y)\text{为}(X,Y)\text{关于}Y\text{的边际分布}(\text{函数})\end{aligned}$
- 公式计算（Y一种情况一样，用F直接算P）
  - $\begin{aligned}F_X(x)&=P\{X\leq x\}\\&=P\{X\leq x,Y<+\infty\}\\&=F(x,+\infty)\end{aligned}$

## 3-2

### 离散型随机变量的联合频率函数 

设 r.v $(X, Y)$ 的所有可能的取值为
$$
\left(x_i, y_j\right) \quad(i, j=1,2, \cdots)
$$

取值的概率为
$$
P\left\{X=x_i, Y=y_j\right\}=p\left(x_i, y_j\right) \triangleq p_{i j} \quad(i, j=1,2, \cdots)
$$

称上式为二维离散型 r.v $(X, Y)$ 的频率函数, 或称为 r.v $X, Y$ 的联合频率函数 ( joint frequency function).

- 本质特征
  - $p_{\ddot{v}}\geq0\quad(i,j=1,2,\cdots)$
  - $\sum_{i=1}^\infty\sum_{j=1}^\infty p_{ij}=1$

### 边际频率函数

- 计算

设 $(X, Y)$ 的频率函数为
$$
P\left\{X=x_i, Y=y_j\right\}=p_{i j} \quad(i, j=1,2, \cdots)
$$

则 r.v $X$ 的频率函数是
$$
\begin{aligned}
P\left\{X=x_i\right\} & =P\left(\left\{X=x_i\right\} \cap \Omega\right) \triangleq p_i . \quad(i=1,2, \cdots) \\
& =P\left(\left\{X=x_i\right\} \cap\left(\bigcup_{j=1}^{\infty}\left\{Y=y_j\right\}\right)\right) \\
& =P\left(\bigcup_{j=1}^{\infty}\left(\left\{X=x_i\right\} \cap\left\{Y=y_j\right\}\right)\right) \\
& =P\left(\bigcup_{j=1}^{\infty}\left\{X=x_i, Y=y_j\right\}\right) \\
& =\sum_{j=1}^{\infty} P\left\{X=x_i, Y=y_j\right\} \\
& =\sum_{j=1}^{\infty} p_{i j}
\end{aligned}
$$

- 定义
设 $(X, Y)$ 的频率函数为

$$
P\left\{X=x_i, Y=y_j\right\}=p_{i j} \quad(i, j=1,2, \cdots)
$$

则 r.v $X$ 的频率函数是
$$
P\left\{X=x_i\right\}=\sum_{j=1}^{\infty} p_{i j} \triangleq p_i . \quad(i=1,2, \cdots)
$$

同理 $Y$ 的频率函数是
$$
P\left\{Y=y_j\right\}=\sum_{i=1}^{\infty} p_{i j} \triangleq p_{\cdot j} \quad(j=1,2, \cdots)
$$

定义 称数列 $\left\{p_{i .}\right\}$ 为 $(X, Y)$ 关于 $X$ 的边际频率函数称数列 $\left\{p_{. j}\right\}$ 为 $(X, Y)$ 关于 $Y$ 的边际频率函数 (marginal frequency function).

- **本质上是一维的随机变量的频率函数，可以通过二位随机变量的频率函数计算得到，代表了固定x，y中某一变量以后，另一个变量的整体取值情况**
- n维拓展（做了解）
- 设 $X_1, \ldots, X_n$ 的联合频率函数为

$$
P\left\{X_1=x_1, \ldots, X_n=x_n\right\}=p\left(x_1, \ldots, x_n\right)
$$

则 r.v $X_1$ 的边际频率函数是
$$
p_{X_1}\left(x_1\right)=\sum_{x_2 \ldots x_n} p\left(x_1, x_2, \ldots, x_n\right)
$$
r.v $X_1$ 和 $X_2$ 的二维边际频率函数是
$$
p_{X_1 X_2}\left(x_1, x_2\right)=\sum_{x_3 \ldots x_n} p\left(x_1, x_2, \ldots, x_n\right)
$$

- 拓展：联合频率函数在多项分数中的应用
- 联合频率函数是一种描述两个或多个随机变量之间关系的函数，它可以用来计算多项分布的概率。多项分布是一种描述多个可能结果的离散型概率分布，它是二项分布的推广。例如，扔骰子的结果有六种可能，每种结果的概率都是 $1 / 6$ ，那么扔n次骰子，每种结果出现的次数就服从多项分布。

如果 $X 1, \mathrm{X} 2, \ldots, \mathrm{Xk}$ 是表示每种结果出现次数的随机变量，那么它们的联合频率函数就是:
$$
F\left(x_1, x_2, \ldots, x_k\right)=P\left(X_1=x_1, X_2=x_2, \ldots, X_k=x_k\right)
$$

这个函数可以用多项系数和各结果概率的乘积来表示，即:
$F(x_1,x_2,...,x_k)=\\\frac {n!} {x_1!x_2!...x_k!}p_1^{x_1}p_2^{x_2}...p_k^{x_k}$
其中，n是试验次数，p1, p2, …, pk是各结果的概率，满足p1 + p2 + … + pk = 1