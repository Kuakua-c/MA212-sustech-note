# chapter3-7极值和顺序统计量

## 机制max(X,Y),min(X,Y)的分离

(1) 设 $X \sim F_X(x), Y \sim F_Y(y)$, 且 $\boldsymbol{X}, \boldsymbol{Y}$ 相互独立, 则
$$
\begin{aligned}
F_{\max }(z) & =P\{\max (X, Y) \leq z\} \\
& =P\{X \leq z, Y \leq z\} \\
& =P\{X \leq z\} \cdot P\{Y \leq z\} \\
& =F_X(z) \cdot F_Y(z) \\
F_{\min }(z) & =P\{\min (X, Y) \leq z\} \\
& =1-P\{\min (X, Y)>z\} \\
& =1-P\{X>z, Y>z\} \\
& =1-P\{X>z\} \cdot P\{Y>z\} \\
& =1-[1-P\{X \leq z\}] \cdot[1-P\{Y \leq z\}] \\
& =1-\left[1-F_X(z)\right] \cdot\left[1-F_Y(z)\right]
\end{aligned}
$$
$$
\begin{aligned}
F_{\max }(z) & =F_X(z) \cdot F_Y(z) \\
F_{\min }(z) & =1-\left[1-F_X(z)\right] \cdot\left[1-F_Y(z)\right]
\end{aligned}
$$
(2) 设 $X_i \sim F_{X_i}(x), i=1,2, \cdots, n$, 且 $X_1, X_2, \cdots, X_n$ 相互独立,
则
$$
\begin{aligned}
F_{\max }(z) & =P\left\{\max \left(X_1, X_2, \cdots, X_n\right) \leq z\right\} \\
& =F_{X_1}(z) F_{X_2}(z) \cdots F_{X_n}(z)
\end{aligned}
$$
$$
\begin{aligned}
F_{\text {min }}(z) & =P\left\{\min \left(X_1, X_2, \cdots, X_n\right) \leq z\right\} \\
& =1-\prod_{i=1}^n\left[1-F_{X_i}(z)\right]
\end{aligned}
$$
(3) 特别当 $X_1, X_2, \cdots, X_n$ 独立同分布于 $F(x)$ 时, 有
$$
\begin{aligned}
& F_{\max }(z)=F^n(z) \\
& F_{\min }(z)=1-[1-F(z)]^n
\end{aligned}
$$
其中$\prod$这个符号是希腊字母n的大写形式，在数学中表示求积运算，也就是累乘，类似于求和符号 $\Sigma_0$ 它的一般形式是:
$$
\prod_{i=a}^b f(i)=f(a) \times f(a+1) \times \cdots \times f(b)
$$

其中， $i$ 是指标变量， $a$ 和 $b$ 是上下限， $f(i)$ 是被乘的函数。例如，阶乘 $n !$ 可以用求积符号表示为:
$$
n !=\prod_{i=1}^n i=1 \times 2 \times \cdots \times n
$$

### X,Y独立同分布情况

$$
\begin{aligned}
\because F_{\max }(z)=F^2(z) \\
\therefore f_{\max }(z) = 2 f(z) F(z) = 2 f(z) \int_{-\infty}^z f(t) d t \\
\because F_{\min }(z) = 1-[1-F(z)]^2 \\
\therefore f_{\min }(z) =2 f(z)[1-F(z)] =2 f(z)\left[1-\int_{-\infty}^z f(t) d t\right]
\end{aligned}
$$

同理可推广，求出 $n$ 个独立同分布的 r.v. 的极值密度为:
$$
f_{\max }(z)=n f(z)[F(z)]^{n-1} \quad f_{\min }(z)=n f(z)[1-F(z)]^{n-1}
$$

#### 推广到n维情况

设 $X_1, \ldots, X_n$ 是 $n$ 个相互独立的随机变量,它们的分布函数分别为
$$
F_{X_i}(x) \quad(i=0,1, \ldots, n)
$$
$M=\max \left(X_1, \ldots, X_n\right)$ 的分布函数为:
$$
F_M(z)=F_{X_1}(z) \cdots F_{X_n}(z)
$$
$N=\min \left(X_1, \ldots, X_n\right)$ 的分布函数是
$$
F_N(z)=1-\left[1-F_{X_1}(z)\right] \cdots\left[1-F_{X_n}(z)\right]
$$

特别, 当 $X_1, \ldots, X_n$ 相互独立且具有相同分布函数 $F(x)$ 时, 有
$$
\begin{gathered}
F_M(z)=[F(z)]^n \\
F_N(z)=1-[1-F(z)]^n
\end{gathered}
$$

- 若是连续型随机变量情况则再进一步求一下密度函数

#### 微分思路的应用

- 背景：设 $X_i(i=1, \ldots, n) \sim f(x)$ 且相互独立,怎样求 $Z=\max \left(X_1, \ldots, X_n\right)$
- 利用分布函数的定义。这种方法的基本思路是，如果 $X_1, X_2, \ldots, X_n$ 都服从 $f(x)$ ，那么它们的最大值 $Z=\max \left(X_1, X_2, \ldots, X_n\right)$ 的分布函数为:
- 
$$
F_Z(z)=P\{Z \leq z\}=P\left\{\max \left(X_1, X_2, \ldots, X_n\right) \leq z\right\}
$$

由于 $\max \left(X_1, X_2, \ldots, X_n\right) \leq z$ 等价于 $X_1 \leq z, X_2 \leq z, \ldots, X_n \leq z$ ，且 $X_1, X_2, \ldots, X_n$ 相互独立，所以有:
$$
F_Z(z)=P\left\{X_1 \leq z, X_2 \leq z, \ldots, X_n \leq z\right\}=P\left\{X_1 \leq z\right\} P\left\{X_2 \leq z\right\} \cdots P\left\{X_n \leq z\right\}=\left[F_X(z)\right]^*
$$

其中， $F_X(z)$ 是 $X_i$ 的分布函数。然后，对 $F_Z(z)$ 求导，就可以得到 $Z$ 的概率密度函数为:
$$
f_Z(z)=n\left[F_X(z)\right]^{n-1} f_X(z)
$$

其中， $f_X(z)$ 是 $X_i$ 的概率密度函数。这种方法需要掌握分布函数的定义和性质，以及求导的技巧。

- 利用微分变换法。这种方法的基本思路是，如果 $X_1, X_2, \ldots, X_n$ 都服从 $f(x)$ ，那么它们的最大值 $Z=\max \left(X_1, X_2, \ldots, X_n\right)$ 的概率密度函数为:

$$
f_Z(z)=\frac{d}{d z} P\{Z \leq z\}=\frac{d}{d z} P\left\{\max \left(X_1, X_2, \ldots, X_n\right) \leq z\right\}
$$

由于 $\max \left(X_1, X_2, \ldots, X_n\right) \leq z$ 等价于 $X_1 \leq z, X_2 \leq z, \ldots, X_n \leq z$ ，且 $X_1, X_2, \ldots, X_n$ 相互独立，所以有:
$$
f_Z(z)=\frac{u}{d z} P\left\{X_1 \leq z, X_2 \leq z, \ldots, X_n \leq z\right\}=\frac{u}{d z}\left[F_X(z)\right]^n
$$

其中， $F_X(z)$ 是 $X_i$ 的分布函数。然后，利用链式法则，就可以得到 $Z$ 的概率密度函数为:
$$
f_Z(z)=n\left[F_X(z)\right]^{n-1} f_X(z)
$$

其中， $f_X(z)$ 是 $X_i$ 的概率密度函数。这种方法需要掌握微分变换法的原理和应用，以及链式法则的使用

- 背景2
设 $X_i(i=1, \ldots, n) \sim f(x)$ 是独立同分布的连续型 r.v.将 $X_1, X_2, \ldots, X_n$ 由小到大排列为 $X_{(1)} \leq X_{(2)} \leq \ldots \leq X_{(n)}$
顺序统计量 $\left(X_{(1)}, X_{(2)}, \ldots, X_{(n)}\right)$
最小值 $X_{(1)}=\min \left\{X_1, X_2, \cdots, X_n\right\}$
最大值 $X_{(n)}=\max \left\{X_1, X_2, \cdots, X_n\right\}$

若 $\boldsymbol{n}$ 是奇数 $n=2 m+1$, 则 $X_{(m+1)}$ 称为中位数(median).
(通) 题 如何求 $X_{(k)}$ 的密度?

- 使用微分思路

$$
\begin{aligned}
& \text { 对于充分小的区间 } \quad:[x, x+\mathrm{d} x] \\
& \begin{aligned}
P\{x \leq & \left.X_{(k)} \leq x+\mathrm{d} x\right\} \\
& =\frac{n !}{(k-1) ! 1 !(n-k) !} F^{k-1}(x)[1-F(x)]^{n-k} f(x) d x \\
& =f_k(x) \mathrm{d} x
\end{aligned}
\end{aligned}
$$

故
$$
f_k(x)=\frac{n !}{(k-1) !(n-k) !} f(x) F^{k-1}(x)[1-F(x)]^{n-k}
$$

- 使用贝塔密度刻画

若 $X_i(i=1, \ldots, n) \sim \mathrm{U}[0,1]$ 且相互独立，则 $X_{(k)}$ 的密度
$$
\begin{gathered}
\frac{n !}{(k-1) !(n-k) !} x^{k-1}(1-x)^{n-k}, \quad 0 \leq x \leq 1 \\
\sim \operatorname{Beta}(k, n-k+1)
\end{gathered}
$$

由于密度函数积分等于 1 ，因此得到
$$
\int_0^1 x^{k-1}(1-x)^{n-k} \mathrm{~d} x=\frac{(k-1) !(n-k) !}{n !} .
$$

贝塔密度用来刻画 $[0,1]$ 区间上的r.v.:
$$
f(u)=\frac{\Gamma(a+b)}{\Gamma(a) \Gamma(b)} u^{a-1}(1-u)^{b-1}, \quad 0 \leq u \leq 1
$$

- 直接推

首先，我们定义一个随机变量 $Y_k$ ，表示第 $k$ 个顺序统计量 $X_{(k)}$ 落在区间 $(x, x+\Delta x)$ 的概率，即
$$
Y_k=P\left(x<X_{(k)} \leq x+\Delta x\right)
$$

根据概率的加法原则， $Y_k$ 等于以下三种事件的概率之和:
- 事件A：恰有 $k-1$ 个样本值小于 $x$ ，恰有 1 个样本值在 $(x, x+\Delta x)$ 内，恰有 $n-k$ 个样本值大于 $x+\Delta x$ 。
- 事件B：佮有 $k$ 个样本值小于 $x$, 恰有 1 个样本值在 $(x, x+\Delta x)$ 内，恰有 $n-k-1$ 个样本值大于 $x+\Delta x$ 。
- 事件C: 恰有 $k+1$ 个样本值小于 $x$ ，恰有 1 个样本值在 $(x, x+\Delta x)$ 内，恰有 $n-k-2$ 个样本值大于 $x+\Delta x$

由于这三种事件是互斥的，所以
$$
Y_k=P(A)+P(B)+P(C)
$$

接下来，我们分别计算这三种事件的概率。
对于事件 $A$ ，我们可以用组合数的方法来计算，即
$$
P(A)=\left(\begin{array}{c}
n \\
k-1,1, n-k
\end{array}\right) f(x) \Delta x[F(x)]^{k-1}[1-F(x+\Delta x)]^{n-k}
$$

其中， $(k-1,1, n-k)$ 表示从 $n$ 个样本值中选出 $k-1$ 个小于 $x ， 1$ 个在 $(x, x+\Delta x)$ 内， $n-k$ 个大于 $x+\Delta x$ 的方法数、它等于
$$
\left(\begin{array}{c}
n \\
k-1,1, n-k
\end{array}\right)=\frac{n !}{(k-1) !(n-k) !}
$$
$f(x) \Delta x$ 表示一个样本值在 $(x, x+\Delta x)$ 内的概率， $[F(x)]^{k-1}$ 表示 $k-1$ 个样本值小于 $x$ 的概率， $[1-F(x+\Delta x)]^{n-k}$ 表示 $n-k$ 个样本值大于 $x+\Delta x$ 的概率。

类似地，对于事件 $\mathrm{B}$ 和事件 $\mathrm{C}$ ，我们可以得到
$$
\begin{gathered}
P(B)=\left(\begin{array}{c}
n \\
k, 1, n-k-1
\end{array}\right) f(x) \Delta x[F(x)]^k[1-F(x+\Delta x)]^{n-k-1} \\
P(C)=\left(\begin{array}{c}
n \\
k+1,1, n-k-2
\end{array}\right) f(x) \Delta x[F(x)]^{k+1}[1-F(x+\Delta x)]^{n-k-2}
\end{gathered}
$$

- 后续将三个概率相加，再求极限

$$
\lim _{\Delta x \rightarrow 0} \frac{Y_k}{\Delta x}=\lim _{\Delta x \rightarrow 0} \frac{n !}{(k-1) !(n-k) !} f(x)[F(x)]^{k-1}[1-F(x+\Delta x)]^{n-k}+\lim _{\Delta x \rightarrow 0} \frac{n !}{k !(n-k-1) !} f(x)[F(x)]^k[1-F(x+\Delta x)]^{n-k-1}+\lim _{\Delta x \rightarrow 0} \frac{n !}{(k+1) !(n-k-2) !} f(x)[F(x)]^{k+1}[1-F(x+\Delta x)]^{n-k-2}
$$

由于 $F(x)$ 是一个连续函数，所以当 $\Delta x \rightarrow 0$ 时，有 $F(x+\Delta x) \rightarrow F(x)$ ，因此上式可以化简为
$$
\lim _{\Delta x \rightarrow 0} \frac{Y_k}{\Delta x}=\frac{n !}{(k-1) !(n-k) !} f(x)[F(x)]^{k-1}[1-F(x)]^{n-k}
$$

这就是第 $k$ 个顺序统计量 $X_{(k)}$ 的密度函数，即
$$
f_k(x)=\frac{n !}{(k-1) !(n-k) !} f(x) F(x)^{k-1}[1-F(x)]^{n-k}
$$