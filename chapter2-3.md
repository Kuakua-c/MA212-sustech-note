
# chapter2-3

- introduction
  - 已知随机变量X的概率分布，且已知Y=g(x),求Y的概率分布

## X为离散，Y也为离散

1. 通过Y=g(X)关系式，将X的频率转化为对应Y的频率
2. 写出Y的频率函数

## 连续型随机变量情况

1. $\operatorname{\text{求}r.v}Y\text{的分布函数}F_Y(y)=P\{Y\leq y\}$
2. 转化为关于X的概率计算问题
   1. $F_Y(y)=P\left\{g(X)\leq{y}\right\}=\int_{-\infty}^{E}f_X(x)dx$ where E define by g(X)
   2. $F_Y(y)=P\{X\leq g^{-1}(y)\}=\int_{-\infty}^{g^{-1}(y)}f_X(x)dx$(此处情况y=g(X)单增)
3. $\text{求导 }f_Y(y)=F_Y^{\prime}(y)$
   1. $f_Y(y)=F_Y^{\prime}(y)=f_X\left(g^{-1}(y)\right)\cdot\left[g^{-1}(y)\right]^{\prime}$(此处情况y=g(X)单增)

- 定理：设连续型随机变量X的密度函数为f（x），又y=g（x）是严格单调函数，其反函数h(y)=$g^{-1}(y)$连续可导，则Y的密度函数为
  - $f_{Y}(y)=\begin{cases}\mid h^{\prime}(y)\mid\cdot f(h(y)),h(y)\text{ 有意义}\\0\quad,\quad\quad\quad\quad\text{其它}\end{cases}$
- 特别，正态连续型随机变量分布的线性函数仍符合正态分布
- 2-2中标准正态分布和一般正态分布情况符合可使用该情况
- **书写反函数时注意考虑取值范围**

### 推广的定理，h（y）多段，则Y的密度函数可以表示为每一段h（y）加起来

- 设 $\mathrm{r} . \mathrm{v} X$ 的密度函数为 $f(x)$, 又函数 $g(x)$ 在互不相交的区间 $\left(a_1, b_1\right),\left(a_2, b_2\right), \cdots$ 上逐段严格单调, 且其反函数 $h_1(y), h_2(y), \cdots$ 均连续可导, 则 $Y=g(X)$ 的密度函数为

$$
f_Y(y)=\left\{\begin{array}{cc}
\sum_{i=1}\left|h_i^{\prime}(y)\right| \cdot f\left(h_i(y)\right), & h_1(y), h_2(y), \cdots \\
0 & \text { 其它 }
\end{array}\right.
$$

## 均匀分布与其他连续分布的关系

- 设 r.v. $X$ 的密度为 $f(x)$, 分布函数为 $F(x)$.
其中 $F(x)$ 在某区间 $I$ 上严格递增, $I$ 的左端点处 $F=0$,右端点处 $F=1$. $I$ 可以是有界区间, 也可以是无界区间.因此, $F^{-1}(x)$ 在 $I$ 上都有定义.
(1) 令 $Z=F(X)$, 那么 $Z \sim \mathrm{U}(\mathbf{0}, \mathbf{1})$.

$$
\begin{aligned}
P\{Z \leq z\} & =P\{F(X) \leq z\} \\
& =P\left\{X \leq F^{-1}(z)\right\} \\
& =F\left(F^{-1}(z)\right)=z
\end{aligned}
$$

(2)
$$
\begin{aligned}&\text{令 }U\sim\mathscr{U}(0,1),\:X=F^{-1}(U),\textbf{那么}X\text{的分布函数是}F(x)\\P\{X\leq x\}&=P\{F^{-1}(U)\leq x\}=P\{U\leq F(x)\}=F(x)\end{aligned}
$$