# chapter3-6联合分布随机变量函数

## introduction

若 $(X, Y) \sim f(x, y)$, 怎样求
$$
X+Y, \max \{X, Y\}, \min \{X, Y\}
$$

的分布?
一般地 设 $z=g(x, y)$ 是一个二元函数,
怎样求 r.v $Z=g(X, Y)$ 的分布?

思路：
$$
\begin{aligned}
F_Z(z) & =P\{Z \leq z\} \\
& =P\{g(X, Y) \leq z\} \\
& =\iint_{g(x, y) \leq z} f(x, y) d x d y \\
& =\cdots=\int_{-\infty}^z f_Z(u) d u \\
\therefore \quad Z & \sim f_Z(z)
\end{aligned}
$$

## 连续型情况Z=X+Y分布

设 $(X, Y) \sim f(x, y)$, 则 $Z=X+Y$ 的分布函数为
$$
\begin{aligned}
& F_Z(z)=P\{Z \leq z\}=P\{X+Y \leq z\} \\
& =\iint_{x+y \leq z} f(x, y) d x d y \\
& =\int_{-\infty}^{\infty} d y \int_{-\infty}^{z-y} f(x, y) d x \\
& \stackrel{\text { 令 } x=u-y}{=} \int_{-\infty}^{\infty} \int_{-\infty}^z f(u-y, y) d u d y \\
& =\int_{-\infty}^z\left[\int_{-\infty}^{\infty} f(u-y, y) d y\right] d u \\
& \therefore f_Z(z)=\int_{-\infty}^{\infty} f(z-y, y) d y \\
& =\int_{-\infty}^{\infty} f(x, z-x) d x \\
&
\end{aligned}
$$
**令x=u-y目的：令 x=u-y 的目的是为了将积分区域从 $x+y \leq z$ 变为$ -\infty < u < z $，这样可以方便地将二重积分化为累次积分。这是一种常见的换元法，可以利用和差换元的性质，将多元式子变为和差形式进行运算**

设 $(X, Y) \sim f(x, y)$, 则 $Z=X+Y$ 的分布函数为
$$
\begin{aligned}
F_Z(z) & =P\{Z \leq z\}=P\{X+Y \leq z\} \\
f_Z(z) & =\int_{-\infty}^{\infty} f(z-y, y) d y=\int_{-\infty}^{\infty} f(x, z-x) d x
\end{aligned}
$$

若 $X, Y$ 相互独立, 则 $Z=X+Y$ 的密度函数为
$$
\begin{aligned}
& f_Z(z)=\int_{-\infty}^{\infty} f_X(z-y) f_Y(y) d y \\
& f_Z(z)=\int_{-\infty}^{\infty} f_X(x) f_Y(z-x) d x
\end{aligned}
$$

称为卷积 (convolution)公式, 记为
$$
\begin{aligned}
f_X · f_Y & =\int_{-\infty}^{\infty} f_X(z-y) f_Y(y) d y \\
& =\int_{-\infty}^{\infty} f_X(x) f_Y(z-x) d x
\end{aligned}
$$
**使用时讨论好x范围**

### 通过卷积计算独立正态随机变量和的一般结果

设 $X, Y$ 相互独立,且
则
$$
\boldsymbol{X} \sim \boldsymbol{N}\left(\mu_1, \sigma_1^2\right), \boldsymbol{Y} \sim \boldsymbol{N}\left(\mu_2, \sigma_2^2\right)
$$
$$
\boldsymbol{X}+\boldsymbol{Y} \sim \boldsymbol{N}\left(\mu_1+\mu_2, \sigma_1^2+\sigma_2^2\right)
$$

一般地, 若 $X_1, X_2, \cdots, X_n$ 相互独立,且
$$
X_i \sim N\left(\mu_i, \sigma_i^2\right) \quad(i=1,2, \cdots, n)
$$

则对于不全为零的常数 $a_1, a_2, \cdots, a_n$ 有
$$
a_1 X_1+a_2 X_2+\cdots+a_n X_n \sim N\left(\sum_{i=1}^n a_i \mu_i, \sum_{i=1}^n a_i^2 \sigma_i^2\right)
$$
独立正态随机变量的非零线性组合仍服从正态分布
独立正态随机变量的和仍然服从正态分布，这是正态分布的可加性性质。

### 多项指数分布加和密度

设 $X_1, X_2, \cdots, X_n$ 相互独立且都服从参数为 $\lambda$ 的指数分布,求 $X_1+X_2+\cdots+X_n$ 的分布密度.

提示, 记 $X_1+X_2+\cdots+X_n \sim f_n(z)$, 则 $f_2(z)=\lambda z f_1(z)$设法导出递推公式, 然后用归纳法证明.

- 思路：利用卷积公式。这种方法的基本思路是，如果两个或多个随机变量都服从指数分布，那么它们的和的概率密度函数等于各个随机变量的概率密度函数的卷积。然后，通过递推或归纳的方式，可以得出和的概率密度函数的一般形式，也就是伽马分布的概率密度函数。这种方法需要掌握卷积公式的定义和性质，以及积分的技巧。

## 离散卷积公式

设 $X, Y$ 相互独立, 其频率函数分别为
$$
\begin{array}{ll}
P\{X=i\}=p_i & (i=1,2, \cdots) \\
P\{Y=j\}=q_j & (j=1,2, \cdots)
\end{array}
$$

令 $Z=X+Y$, 则
$$
\begin{aligned}
P\{Z=k\} & =\sum_{i=1}^{k-1} P\{X=i\} \cdot P\{Y=k-i\} \\
& =\sum_{i=1}^{k-1} P\{X=k-i\} \cdot P\{Y=i\} \\
& (k=1,2, \ldots)
\end{aligned}
$$
(离散卷积公式)

- 应用
设 $X, Y$ 独立,且 $X \sim P\left(\lambda_1\right), Y \sim P\left(\lambda_2\right)$, 求 $Z=X+Y$ 的分布.解 由离散卷积公式有

$$
\begin{aligned}
P\{Z=k\} & =\sum_{i=0}^k P\{X=k-i\} \cdot P\{Y=i\} \\
& =\sum_{i=0}^k \frac{\lambda_1^{k-i}}{(k-i) !} e^{-\lambda_1} \frac{\lambda_2^i}{i !} e^{-\lambda_2} \\
& =e^{-\left(\lambda_1+\lambda_2\right)} \sum_{i=0}^k \frac{1}{i !(k-i) !} \lambda_1^{k-i} \cdot \lambda_2^i \\
& =e^{-\left(\lambda_1+\lambda_2\right)} \frac{1}{k !} \sum_{i=0}^k \frac{k !}{i !(k-i) !} \lambda_1^{k-i} \cdot \lambda_2^i \\
& =e^{-\left(\lambda_1+\lambda_2\right)} \frac{\left(\lambda_1+\lambda_2\right)^k}{k !} \quad(k=0,1,2, \cdots) \\
\therefore \quad Z & \sim P\left(\lambda_1+\lambda_2\right) .
\end{aligned}
$$

## 连续性$Z=\frac{X}{Y}$分布

设 $(X, Y) \sim f(x, y)$, 则 $Z=X / Y$ 的分布函数为
$$
F_Z(z)=P\{X / Y \leq z\}=\iint_{\frac{x}{y} \leq z} f(x, y) \mathrm{d} x \mathrm{~d} y
$$
$$
F_Z(z)=\int_0^{+\infty} \mathrm{d} y \int_{-\infty}^{y z} f(x, y) \mathrm{d} x+\int_{-\infty}^0 \mathrm{~d} y \int_{y z}^{+\infty} f(x, y) \mathrm{d} x
$$（积分区域不是矩形，计算比较繁琐）

- 雅可比式
- $\begin{gathered}J=\frac{\partial(x, y)}{\partial(u, v)}=\left|\begin{array}{ll}\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\ \frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}\end{array}\right| \neq 0 \\ \iint_{\Omega} f(x, y) d x d y=\iint_{\Omega^{\prime}} f[x(u, v), y(u, v)]|J| d u d v\end{gathered}$
- 具体使用

令 $\left\{\begin{aligned} x / y & =u \\ y & =y\end{aligned}\right.$, 则变换的Jacobi式为 $\frac{\partial(x, y)}{\partial(u, y)}=\left|\begin{array}{ll}y & u \\ 0 & 1\end{array}\right|=y$
$$
\begin{aligned}
& \therefore F_Z(z)=\int_{-\infty}^z\left(\int_{-\infty}^{+\infty} f(u y, y)|y| \mathrm{d} y\right) \mathrm{d} u \\
& \therefore f_Z(z)=\int_{-\infty}^{+\infty} f(z y, y)|y| \mathrm{d} y
\end{aligned}
$$

特别当 $X, Y$ 独立时, 则有
$$
f_Z(z)=\int_{-\infty}^{+\infty} f_X(z y) f_Y(y)|y| \mathrm{d} y
$$

### 柯西分布（拓展）

柯西分布是一种连续的概率分布，它的概率密度函数为:
$$
f\left(x ; x_0, \gamma\right)=\frac{1}{\pi \gamma\left[1+\left(\frac{x-x_0}{\gamma}\right)^2\right]}
$$

其中， $x_0$ 是位置参数，表示分布的中心或众数； $\gamma$ 是尺度参数，表示分布的宽度。柯西分布的分布函数为:
$$
F\left(x ; x_0, \gamma\right)=\frac{1}{\pi} \arctan \left(\frac{x-x_0}{\gamma}\right)+\frac{1}{2}
$$

柯西分布的特点是它的均值、方差、矩和矩母函数都不存在，它的形状类似于正态分布，但是比正态分布量加厚尾，即有量多的极端值。柯西分布在物理学、光谱学、信号处理等领域有一些应用，例如，它可以描述受迫共振的微分方程的解，或者被共振或其他机制加宽的谱线形状。

## 两个随机变量变换的分布

设 $\xi, \eta$ 为独立同分布均服从指数分布的 r.v,其密度为
$$
f(x)=\left\{\begin{array}{c}
e^{-x}, x \geq 0, \\
0, x<0 .
\end{array}\right.
$$

试求 $U=\xi+\eta, V=\xi / \eta$ 的联合密度, 并证明 $U, V$ 相互独立.
解
$$
\begin{aligned}
F_{U V}(u, v) & =P\{\xi+\eta \leq u, \xi / \eta \leq v\} \\
& =\iint_{\left\{\begin{array}{l}
x+y \leq u \\
x / y \leq v
\end{array}\right.} f(x) f(y) \mathrm{d} x \mathrm{~d} y
\end{aligned}
$$

令 $x+y=\tilde{u}, x / y=\tilde{v}$, 则 $x=\frac{\tilde{u} \tilde{v}}{1+\tilde{v}}, y=\frac{\tilde{u}}{1+\tilde{v}}$,
变换的Jacobi式为
$$
J=\frac{\partial(x, y)}{\partial(\tilde{u}, \tilde{v})}=-\frac{\tilde{u}}{(1+\tilde{v})^2} \quad(\tilde{u} \geq 0, \tilde{v} \neq-1)
$$
$$
\begin{aligned}
& \therefore F_{U V}(u, v)=\iiint_{D:\left\{\begin{array}{l}
x+y \leq u \\
x / y \leq v, x \geq 0, y \geq 0
\end{array}\right.} e^{-(x+y)} \mathrm{d} x \mathrm{~d} y \\
& =\int_0^v \int_0^u e^{-\tilde{u}}|J| \mathrm{d} \tilde{u} \mathrm{~d} \tilde{v} \\
& \therefore \quad f_{U V}(u, v)=\frac{u e^{-u}}{(1+v)^2} \quad(u \geq 0, v \geq 0)
\end{aligned}
$$
$\because f_{U V}(u, v)$ 可表为 $g(u) h(v) \quad \therefore U, V$ 相互独立.

## 拓展：瑞利分布

瑞利分布是一种连续的概率分布，它的概率密度函数为:
$$
f(x ; \sigma)=\frac{x}{\sigma^2} e^{-x^2 / 2 \sigma^2}, x \geq 0
$$

其中， $\sigma$ 是尺度参数，表示分布的宽度。瑞利分布的分布函数为：
$$
F(x ; \sigma)=1-e^{-x^2 / 2 \sigma^2}, x \geq 0
$$

瑞利分布的期望值为:
$$
E(X)=\sigma \sqrt{\frac{\pi}{2}}
$$

瑞利分布的方差为:
$$
\operatorname{Var}(X)=\frac{4-\pi}{2} \sigma^2
$$

瑞利分布的特征函数为:
$$
\phi(t)=1-\sigma t e^{-\sigma^2 t^2 / 2} \sqrt{\frac{\pi}{2}}\left(\operatorname{erfi}\left(\frac{\sigma t}{\sqrt{2}}\right)-i\right)
$$

瑞利分布是威布尔分布的一种特例，当威布尔分布的形状参数为 2 时，就是瑞利分布。瑞利分布的一...人应用是描述受多个独立因素影响的随机现象, 例如粒子的速度、风速, 电磁波的幅度等。
当一个二维随机向量的两个分量呈独立的、有着相同的方差的正态分布时，这个向量的模呈Rayleigh瑞利分布