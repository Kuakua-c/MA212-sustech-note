# chapter3-5条件分布

## 二维离散型随机变量的条件频率函数

设 $(X, Y)$ 的频率函数为
$$
P\left\{X=x_i, Y=y_j\right\}=p_{i j} \quad(i, j=1,2, \cdots)
$$

考虑在 $\left\{Y=y_j\right\}$ 已发生的条件下, $\left\{X=x_i\right\}$ 发生的条件概率
$$
P\left\{X=x_i \mid Y=y_j\right\} \quad(i=1,2, \cdots)
$$

由条件概率公式, 有
$$
P\left\{X=x_i \mid Y=y_j\right\}=\frac{P\left\{X=x_i, Y=y_j\right\}}{P\left\{Y=y_j\right\}}=\frac{p_{i j}}{p_{\cdot j}} \quad(i=1,2, \cdots)
$$
**其为对于固定的j，在Y=$y_j$的条件下，随机变量X的条件频率函数，有关计算公式涉及到了边际频率函数，用于计算离散型的条件频率函数**

同理在 $\left\{X=x_i\right\}$ 已发生的条件下, $\left\{Y=y_j\right\}$ 发生的条件概率
$$
P\left\{Y=y_j \mid X=x_i\right\}=\frac{P\left\{Y=y_j, X=x_i\right\}}{P\left\{X=x_i\right\}}=\frac{p_{i j}}{p_{i .}} \quad(j=1,2, \cdots)
$$
**其为对于固定的i，在X=$x_i$的条件下，随机变量Y的条件频率函数**

### 条件频率函数的性质

(1) $P\left\{X=x_i \mid Y=y_j\right\} \geq 0 \quad(i=1,2, \cdots)$
(2)
$$
\begin{aligned}
\sum_{i=1}^{\infty} \boldsymbol{P}\left\{\boldsymbol{X}=\boldsymbol{x}_i \mid \boldsymbol{Y}=\boldsymbol{y}_j\right\} & =\sum_{i=1}^{\infty} \frac{\boldsymbol{p}_{i j}}{\boldsymbol{p}_{\cdot j}} \\
& =\frac{\mathbf{1}}{\boldsymbol{p}_{\cdot j}} \sum_{i=1}^{\infty} \boldsymbol{p}_{i j} \\
& =\frac{\mathbf{1}}{\boldsymbol{p}_{\cdot j}} \boldsymbol{p}_{\cdot j}=\mathbf{1}
\end{aligned}
$$
说明条件频率函数本身也是一种频率函数

## 二维连续型随机变量条件概率密度

- 引入

设 $(X, Y)$ 的概率密度为
$$
f(x, y)
$$

考虑在 $\{Y=y\}$ 已发生的条件下, $\{X \leq x\}$ 发生的条件概率
$$
P\{X \leq x \mid Y=y\} \quad\left(x \in R^1\right)
$$

若按条件概率公式, 则有
$$
P\{X \leq x \mid Y=y\}=\frac{P\{X \leq x, Y=y\}}{P\{Y=y\}}
$$
对于连续型随机变量，P{Y=y}=0，我们需要对其重新定义，因此我们找到一个数$\epsilon$，使其趋近于0，Y=y就能转化成$y<Y \leq y+\epsilon$
$\forall \varepsilon>0$, 考虑条件概率
$$
P\{X \leq x \mid y<Y \leq y+\varepsilon\}=\frac{P\{X \leq x, y<Y \leq y+\varepsilon\}}{P\{y<Y \leq y+\varepsilon\}} =\frac{\int_{-\infty}^x \int_y^{y+\varepsilon} f(u, v) d v d u}{\int_y^{y+\varepsilon} f_Y(v) d v}
$$

应用积分中值定理
$$
\begin{aligned}
& =\frac{\varepsilon \int_{-\infty}^x f\left(u, y_{\varepsilon}\right) d u}{\varepsilon f_Y\left(\tilde{y}_{\varepsilon}\right)} \\
& \rightarrow \int_{-\infty}^x \frac{f(u, y)}{f_Y(y)} d u \quad(\varepsilon \rightarrow 0)
\end{aligned}
$$
**这里面我们称$\frac{f(u,y)}{F_Y(y)}$为条件概率密度**

- 定义中若对于固定的y，（X，Y）的边际密度$f_Y(y)>0$，则其为在Y=y条件下，X的条件密度。称$F_{X \mid Y}(x \mid y) \triangleq \int_{-\infty}^x f_{X \mid Y}(u \mid y) d u \quad(-\infty<x<\infty)$为在该条件下，X的条件分布函数
- 类似可定义Y的
- 条件密度的性质

$$
\begin{aligned}(1)
& f_{X \mid Y}(x \mid y) \geq 0 \\
& \begin{aligned}(2)
\int_{-\infty}^{\infty} f_{X \mid Y}(u \mid y) d u & =\int_{-\infty}^{\infty} \frac{f(u, y)}{f_Y(y)} d u \\
& =\frac{1}{f_Y(y)} \int_{-\infty}^{\infty} f(u, y) d u \\
& =\frac{1}{f_Y(y)} \cdot f_Y(y)=1
\end{aligned}
\end{aligned}
$$

- 条件密度也是一种密度函数
- **使用边际密度和条件密度表示联合密度**

由
$$
f_{Y \mid X}(y \mid x) \triangleq \frac{f(x, y)}{f_X(x)} \quad(-\infty<y<\infty)
$$

因此
$$
f(x, y)=f_{Y \mid X}(y \mid x) f_X(x)
$$

即: 联合密度可以用边际密度和条件密度表示
两边关于 $x$ 积分, $Y$ 的边际密度可表示为
$$
f_Y(y)=\int_{-\infty}^{\infty} f_{Y \mid X}(y \mid x) f_X(x) \mathrm{d} x
$$
此为连续情形的全概率公式

### 二维随机变量独立性与条件密度的关系

$$
\begin{aligned}
X, Y \text { 相互独立 } \Leftrightarrow & f(x, y)=f_X(x) f_Y(y) \quad(a . e) \\
\Leftrightarrow & f_{X \mid Y}(x \mid y)=\frac{f(x, y)}{f_Y(y)}=f_X(x) \text { (a.e) } \\
& f_{Y \mid X}(y \mid x)=\frac{f(x, y)}{f_X(x)}=f_Y(y) \quad \text { (a.e) }
\end{aligned}
$$

### 二维正态分布中的条件密度计算

设 $(X, Y) \sim N\left(\mu_1, \mu_2, \sigma_1^2, \sigma_2^2, \rho\right)$,
$$
f(x, y)=\frac{1}{2 \pi \sigma_1 \sigma_2 \sqrt{1-\rho^2}} e^{-\frac{1}{2\left(1-\rho^2\right)}\left[\frac{\left(x-\mu_1\right)^2}{\sigma_1^2}-2 \rho \frac{\left(x-\mu_1\right)\left(y-\mu_2\right)}{\sigma_1 \sigma_2}+\frac{\left(y-\mu_2\right)^2}{\sigma_2^2}\right]}
$$
$$
f_X(x)=\frac{1}{\sqrt{2 \pi} \sigma_1} e^{-\frac{\left(x-\mu_1\right)^2}{2 \sigma_1^2}}
$$

则经过计算可得
$$
\begin{aligned}
f_{Y \mid X}(y \mid x) & =\frac{1}{\sigma_2 \sqrt{2 \pi\left(1-\rho^2\right)}} \exp \left(-\frac{1}{2} \frac{\left[y-\mu_2-\rho \frac{\sigma_2}{\sigma_1}\left(x-\mu_1\right)\right]^2}{\sigma_2^2\left(1-\rho^2\right)}\right) \\
& \sim N\left(\mu_2+\rho \frac{\sigma_2}{\sigma_1}\left(x-\mu_1\right), \sigma_2^2\left(1-\rho^2\right)\right) .
\end{aligned}
$$

即: 二维正态分布, 给定 $X$ 时 $Y$ 的条件密度是一维 (单变量)正态分布。

## summary

随机变量的边际分布完全由它们的联合分布确定
$$
F_X(x)=F(x,+\infty) \quad F_Y(y)=F(+\infty, y)
$$

离散型r.v的边际频率函数
$$
\begin{array}{r}
P\left\{X=x_i\right\}=\sum_{j=1}^{\infty} p_{i j} \triangleq p_{i .} \\
\quad(i=1,2, \cdots) \\
P\left\{Y=y_j\right\}=\sum_{i=1}^{\infty} p_{i j} \triangleq p_{\cdot j} \\
(j=1,2, \cdots)
\end{array}
$$

连续型r.v的边际分布密度
$$
\begin{gathered}
f_X(x)=\int_{-\infty}^{+\infty} f(x, y) d y \\
(-\infty<x<+\infty) \\
f_Y(y)=\int_{-\infty}^{+\infty} f(x, y) d x \\
(-\infty<y<+\infty)
\end{gathered}
$$

定理 若 $(X, Y) \sim N\left(\mu_1, \mu_2, \sigma_1^2, \sigma_2^2, \rho\right)$, 则
$$
X \sim N\left(\mu_1, \sigma_1^2\right), \quad Y \sim N\left(\mu_2, \sigma_2^2\right)
$$

条件分布
$$
P\{X \leq x \mid Y=y\} \quad\left(x \in R^1\right)
$$

这可视为在 $\{\boldsymbol{Y}=\boldsymbol{y}\}$ 发生的条件下
P.V $X$ 的概率分布——条件分布

离散型 $r . v$ 的条件频率函数
$$
\begin{gathered}
P\left\{X=x_i \mid Y=y_j\right\}=\frac{p_{i j}}{p_{\cdot j}} \\
\left(p_{\cdot j}>0, i=1,2, \cdots\right) \\
P\left\{Y=y_j \mid X=x_i\right\}=\frac{p_{i j}}{p_{i .}} \\
\left(p_i>0, j=1,2, \cdots\right)
\end{gathered}
$$

连续型 $\mathrm{r}, \mathrm{v}$ 的条件概率密度
$$
\begin{aligned}
& f_{X \mid Y}(x \mid y) \triangleq \frac{f(x, y)}{f_Y(y)} \\
& \left(f_Y(y)>0,-\infty<x<\infty\right) \\
& f_{Y \mid X}(y \mid x) \triangleq \frac{f(x, y)}{f_X(x)} \\
& \left(f_X(x)>0,-\infty<y<\infty\right)
\end{aligned}
$$