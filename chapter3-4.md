
# 3-4独立随机变量

## 二维随机变量独立性

- 从一维带过来
- X的取值与Y的取值相互独立，互不相干
定义 设

$$
(X, Y) \sim F(x, y), X \sim F_X(x), Y \sim F_Y(y)
$$

若 $\forall x, y \in(-\infty, \infty)$ 有
$$
P\{X \leq x, Y \leq y\}=P\{X \leq x\} \cdot P\{Y \leq y\}
$$

即
$$
F(x, y)=F_X(x) \cdot F_Y(y)
$$

则称 r.v $X, Y$ 相互独立。

它表明，两个r.v相互独立时，联合分布函数等于两个边缘分布函数的乘积
在独立定义条件下，进一步看
设 $X, Y$ 相互独立, $\forall x_1<x_2, y_1<y_2$ 有
$$
\begin{aligned}
P\left\{x_1<X \leq x_2,\right. & \left.y_1<Y \leq y_2\right\} \\
= & F\left(x_2, y_2\right)-F\left(x_1, y_2\right)-F\left(x_2, y_1\right)+F\left(x_1, y_1\right) \\
= & F_X\left(x_2\right) F_Y\left(y_2\right)-F_X\left(x_1\right) F_Y\left(y_2\right) \\
& -F_X\left(x_2\right) F_Y\left(y_1\right)+F_X\left(x_1\right) F_Y\left(y_1\right) \\
= & {\left[F_X\left(x_2\right)-F_X\left(x_1\right)\right] \cdot\left[F_Y\left(y_2\right)-F_Y\left(y_1\right)\right] } \\
= & P\left\{x_1<X \leq x_2\right\} \cdot P\left\{y_1<Y \leq y_2\right\} \\
\therefore \quad\left\{x_1<\right. & \left.X \leq x_2\right\},\left\{y_1<Y \leq y_2\right\} \text { 相互独立. }
\end{aligned}
$$

## 概率分布函数上表现独立

设 $(X, Y)$ 的频率函数为
$$
P\left\{X=x_i, Y=y_j\right\}=p_{i j}(i, j=1,2, \cdots)
$$

则 $X, Y$ 相互独立等价于 $\forall i, j=1,2, \cdots$ 有
$$
\begin{aligned}
& \boldsymbol{P}\left\{\boldsymbol{X}=\boldsymbol{x}_i, \boldsymbol{Y}=\boldsymbol{y}_j\right\}=\boldsymbol{P}\left\{\boldsymbol{X}=\boldsymbol{x}_i\right\} \cdot \boldsymbol{P}\left\{\boldsymbol{Y}=\boldsymbol{y}_j\right\} \\
& \boldsymbol{X} \text { 与 } \boldsymbol{Y} \text { 独立 } \Longleftrightarrow \text { 对一切 } \boldsymbol{i}, \boldsymbol{j} \text { 有 } \\
& P\left(X=x_i, Y=y_j\right)=P\left(X=x_i\right) P\left(Y=y_j\right)
\end{aligned}
$$

即
$$
p_{i j}=p_{i \bullet} \cdot p_{\bullet j}
$$
**利用定义公式来证明有关事件之间的独立性，满足则独立**

## 密度函数上表示独立（连续随机变量）

设 $(X, Y)$ 为连续型 $r . v$, 且
$$
\begin{gathered}
(X, Y) \sim f(x, y) \\
X \sim f_X(x), \quad Y \sim f_Y(y)
\end{gathered}
$$

若 $\boldsymbol{X}, \boldsymbol{Y}$ 相互独立, 则
$$
\begin{aligned}
\int_{-\infty}^x \int_{-\infty}^y f(u, v) d u d v & =P\{X \leq x, Y \leq y\} \\
& =P\{X \leq x\} P\{Y \leq y\} \\
& =\int_{-\infty}^x f_X(u) d u \cdot \int_{-\infty}^y f_Y(v) d v \\
& =\int_{-\infty}^x \int_{-\infty}^y f_X(u) f_Y(v) d u d v
\end{aligned}
$$

从而在 $f(x, y), f_X(x), f_Y(y)$ 的连续点处有
$$
f(x, y)=f_X(x) f_Y(y)
$$
**通过密度函数的独立性公式证明独立性**

- 对于一些直观图形，可能有一些特殊点直接就让独立结论不成立了，会出现f=0的情况，可以直接拿来判断
- **需要注意的是，因为XY相互独立，因此边缘分布在独立情况下能完全确定联合分布**

- 密度函数形式可分离,但支撑区域不可分离
  - 除了形式可分离性，还有一个概念是支撑区域的可分离性。支撑区域是指随机变量的取值范围，或者说是密度函数非零的区域。如果两个随机变量X和Y的支撑区域是一个矩形，即X的取值范围是[a,b]，Y的取值范围是[c,d]，那么我们说支撑区域是可分离的，因为它可以分解为两个区间的乘积。但是，如果两个随机变量的支撑区域不是一个矩形，而是一个更复杂的形状，比如一个圆或者一个三角形，那么我们说支撑区域是不可分离的，因为它不能分解为两个区间的乘积
  - 两个随机变量的联合分布可以表示为它们的边缘分布的乘积，但是它们的取值范围不是一个矩形，而是一个更复杂的形状。这种情况下，两个随机变量不一定是相互独立的，因为它们的取值可能受到对方的影响。
- 例
若 $(X, Y)$ 的概率密度为

$$
f(x, y)=\left\{\begin{array}{rr}
2, & 0<x<y, 0<y<1 \\
0, & \text { 其它 }
\end{array}\right.
$$
解
$$
\begin{aligned}
f_X(x) & =\int_x^1 2 d y=2(1-x), & & 0<x<1 \\
f_Y(y) & =\int_0^y 2 d x=2 y, & & 0<y<1
\end{aligned}
$$

由于存在面积不为 0 的区域,
$$
f(x, y) \neq f_X(x) f_Y(y)
$$

故 $X$ 和 $Y$ 不独立.

- 3-3中连接函数中有一种函数，Farlie-Morgenstern族，是一种二元连接函数，可以表示情况为

设 $F(x)$ 和 $G(y)$ 都是一维连续型分布函数, 可以证明,对于任意的 $\alpha$, 只要满足 $|\alpha| \leq 1$, 就有
$$
H(x, y)=F(x) G(y)\{1+\alpha[1-F(x)][1-G(y)]\}
$$

是二元连续型分布函数.
可见, 仅当 $\alpha=0$ 时, $X$ 和 $Y$ 才是独立的, 此时
$$
H(x, y)=F(x) G(y)
$$

分解成了边际分布 $F(x)$ 和 $G(y)$ 的乘积

- Farlie-Morgenstern族的一个特点是，它们只能描述正相关或负相关的情况，不能描述正负相关都有的情况。因此，它们不能覆盖所有可能的相关性参数的范围。

### 二维正态分布中$\rho$与独立性的关系

- 描述
  - 若二维正态分布中XY相互独立，则$\rho$=0
  - 证明

证 $\Rightarrow$ 若 $(X, Y)$ 相互独立, 则 $f(x, y)=f_X(x) f_Y(y)$, 即
$$
\begin{array}{r}
\frac{1}{2 \pi \sigma_1 \sigma_2 \sqrt{1-\rho^2}} \exp \left\{-\frac{1}{2\left(1-\rho^2\right)}\left[\frac{\left(x-\mu_1\right)^2}{\sigma_1^2}-2 \rho \frac{\left(x-\mu_1\right)\left(y-\mu_2\right)}{\sigma_1 \sigma_2}+\frac{\left(y-\mu_2\right)^2}{\sigma_2^2}\right]\right\} \\
=\frac{1}{\sqrt{2 \pi} \sigma_1} \exp \left\{-\frac{\left(x-\mu_1\right)^2}{2 \sigma_1^2}\right\} \cdot \frac{1}{\sqrt{2 \pi} \sigma_2} \exp \left\{-\frac{\left(y-\mu_2\right)^2}{\sigma_2^2}\right\}
\end{array}
$$

令 $x=\mu_1, y=\mu_2$, 则有
$$
\begin{aligned}
& \sqrt{1-\rho^2}=1 \\
& \therefore \rho=0
\end{aligned}
$$

若 $\rho=0$, 显然
即 $X, Y$ 相互独立.
$$
f(x, y) \equiv f_X(x) f_Y(y)
$$

## n维情况

设 $n$ 维 r.v $\left(X_1, X_2, \cdots, X_n\right)$ 的分布函数
$$
F\left(x_1, x_2, \cdots, x_n\right)=P\left\{X_1 \leq x_1, X_2 \leq x_2, \cdots, X_n \leq x_n\right\}
$$

一维边际分布
$X_i$ 的分布函数
$$
\begin{aligned}
F_{X_i}\left(x_i\right) & =P\left\{X_1<\infty, \cdots, X_{i-1}<\infty, X_i \leq x_i, X_{i+1}<\infty, \cdots, X_n<\infty\right\} \\
& =F\left(\infty, \cdots, \infty, x_i, \infty \cdots, \infty\right) \quad(i=1,2, \cdots, n)
\end{aligned}
$$

二维边际分布
$X_1, X_2$ 的联合分布是
$$
\begin{aligned}
& F_{X_1 X_2}\left(x_1, x_2\right)=P\left\{X_1 \leq x_1, X_2 \leq x_2, X_3<\infty, \cdots, X_n<\infty\right\} \\
& =F\left(x_1, x_2, \infty, \cdots, \infty\right) \text { 类似可定义三维、四维等高维边际分布 }
\end{aligned}
$$

$X_3, X_2$ 的联合分布是
$$
\begin{aligned}
& F_{X_2 X_3}\left(x_2, x_3\right)=P\left\{X_1<\infty, X_2 \leq x_2, X_3 \leq x_3, X_4<\infty, \cdots, X_n<\infty\right\} \\
& =F\left(\infty, x_2, x_3, \infty, \cdots, \infty\right) \\
&
\end{aligned}
$$

## 随机向量的独立性

- 直观理解，指的是随机向量的取值是相互独立、互不相干的
- 应用
  - 根据大数定律和中心极限定理，如果一组随机变量是相互独立的，那么它们的均值和方差会随着样本量的增加而趋于稳定，而且它们的和会近似服从正态分布。这些定理为抽样调查和假设检验提供了理论基础

$\forall x_1, x_2, \cdots, x_n \in R^1$ 若有
$$
F\left(x_1, x_2, \cdots, x_n\right)=F_{X_1}\left(x_1\right) F_{X_2}\left(x_2\right) \cdots F_{X_n}\left(x_n\right)
$$

则称 $X_1, X_2, \cdots, X_n$ 相互独立.
设
$$
\begin{aligned}
& \left(X_1, X_2, \cdots, X_m\right) \sim F_1\left(x_1, x_2, \cdots, x_m\right) \\
& \quad\left(Y_1, Y_2, \cdots, Y_n\right) \sim F_2\left(y_1, y_2, \cdots, y_n\right) \\
& \left(X_1, X_2, \cdots, X_m ; Y_1, Y_2, \cdots, Y_n\right) \sim F\left(x_1, x_2, \cdots, x_m ; y_1, y_2, \cdots, y_n\right)
\end{aligned}
$$
$\forall x_1, x_2, \cdots, x_m, y_1, y_2, \cdots, y_n \in R^1$ 若有
$$
F\left(x_1, x_2, \cdots, x_m ; y_1, y_2, \cdots, y_n\right)=F_1\left(x_1, x_2, \cdots, x_m\right) \cdot F_2\left(y_1, y_2, \cdots, y_n\right)
$$

则称 $\left(X_1, X_2, \cdots, X_m\right),\left(Y_1, Y_2, \cdots, Y_n\right)$ 相互独立.

- 随机变量独立性的传递性定理
- 如果两个随机向量是相互独立的，那么它们的每个分量也是相互独立的，而且它们的连续函数也是相互独立的（函数处理过的变量依然独立）

设 $\left(X_1, X_2, \cdots, X_m\right),\left(Y_1, Y_2, \cdots, \boldsymbol{Y}_n\right)$ 相互独立, 则
(1) $X_i, Y_j$ 相互独立 $(i=1,2, \cdots, m ; j=1,2, \cdots, n)$
(2) 设 $h, g$ 分别是 $m$ 元和 $n$ 元的连续函数, 则相互独立.
$$
h\left(X_1, X_2, \cdots, X_m\right), g\left(Y_1, Y_2, \cdots, Y_n\right)
$$

- 利用独立性做题
- 例

例 设在 $\triangle A B C$ 内部任取一点 $P$, 在底边 $B C$ 上任取一点 $Q$, 求直线 $P Q$ 与线段 $A B$ 相交的概率.
解 
依题意, 点 $P$ 服从 $\triangle A B C$ 上的均匀分布, 点 $Q$ 服从区间 $(0, B C)$ 上的均匀分布, 其概率密度分别为
$$
\begin{aligned}
f_{X Y}(x, y) & = \begin{cases}\frac{2}{h \cdot B C},(x, y) \in \triangle A B C \\
0, \quad \text { 其它 }\end{cases} \\
f_Z(z) & =\left\{\begin{array}{cc}
\frac{1}{B C}, z \in(0, B C), \\
0, & \text { 其它 }
\end{array}\right.
\end{aligned}
$$

因为点 $P$ 与点 $Q$ 相互独立, 故联合概率密度为
$$
f(x, y, z)=f_{X Y}(x, y) f_Z(z)
$$