# 2-2

## chapter 2-2

- 累积分布函数
  - $F(x)=P\{X\leq x\}\mathrm{~,~}-\infty<x<\infty$
- 分布函数（cdf）的本质特征（可用于证明）
  1. F（x）是单调不减函数
  2. F（x）是右连续函数（画图的时候注意画出不可取的点）
  3. F（x）在区间[0,1]之间
- 连续型随机变量
  - 定义$\begin{aligned}&\textbf{若}\mathrm{~r.v~}X\textbf{ 的分布函数能够表为}\\&F(x)=\int_{-\infty}^{x}f(t)dt\text{ ,}-\infty<x<\infty\\&\text{其中}f(t)\geq0,\text{则称 }X\text{为连续型r.v}\end{aligned}$
    - **使用定义求分布函数时注意好密度函数中x的取值，会影响到分布函数的x取值**
  - $\begin{aligned}\text{非负可积函数}f(t)\text{称为}\text{概率密度函数（简称为密度函数、密度，pdf）}.\end{aligned}$
  - 连续型随机变量的分布函数仅有有限个点不可导，不影响积分值
    - 这样边界上有无取值不影响积分值
  - 性质
    - 在区间上取值是连续的
    - 连续型随机变量的分布函数是连续函数，且能表现为上述积分形式（**证明一个X为连续型随机变量**）
  - 根据连续性随机变量分布函数的定义式，c为任意常数，P{X=c}=0，因为单点的下方的面积是0。但是，概率P {X=c}=0，但X=c并不是不可能事件，因为随机变量X的取值只取决于概率密度函数的积分，而不是单点的取值
    - 要注意的是，密度函数 f (x) 在某点处 c 的高度，并不反映 X 取值的概率. 但是，这个高度越大，则X 取 c 附近的值的概率就越大.也可以说，在某点密度曲线的高度反映了概率集中在该点附近的程度
- 密度函数的性质
  1. $\begin{aligned}&f(t)\geq0\end{aligned}$（本质特征）
  2. $\begin{aligned}\int_{-\infty}^{\infty}f(t)dt=1\end{aligned}$（本质特征，可用于计算）
  3. $\begin{aligned}\forall\:x_1<x_2\textbf{有}\\&P\{x_1<X\leq x_2\}=F(x_2)-F(x_1)=\int_{x_1}^{x_2}f(x)dx\end{aligned}$
  4. 在f（x）的连续点处有f(x)=$F^{'}(x)$（**计算f（x）**）
     1. $\begin{aligned}\text{注解:}&\textbf{ 设 }x\textbf{是 }f(x)\textbf{ 的连续点}\\&f(x)=\lim_{\Delta x\to0^+}\frac{F(x+\Delta x)-F(x)}{\Delta x}\\&=\lim_{\Delta x\to0^+}\frac{P\{x<X\leq x+\Delta x\}}{\Delta x}\\\textbf{则当 }\Delta x\textbf{ 充分小时,有}\\&P\{x<X\leq x+\Delta x\}\approx f(x)\Delta x\end{aligned}.$
     2. 这里P近似于密度函数一小段小矩形的面积
- p分位数
  - $\begin{gathered}\text{设 }X\thicksim f(x),\text{若 }\forall\mathrm{~}0<p<1,\textbf{存在常数 }x_p\textbf{ 满足}\\P\{X\leq x_p\}=\int_{-\infty}^{x_p}f(x)\mathrm{d}x=p\quad\text{也即 }F(x_p)=p\\\text{则称 }x_p\text{ 为密度函数}f(x)\textbf{的 }P\text{分位教}(\mathrm{quantile}).\end{gathered}$
  - 特殊点，p取1/2，xp为F中位数，取一些等分点可以得到不同的分位数

### 重要连续型随机变量

#### 正态分布（需要学会查表）

- 如果随机变量X的密度函数为$f(x)=\frac1{\sqrt{2\pi}\sigma}e^{-\frac{(x-\mu)^2}{2\sigma^2}},-\infty<x<\infty$，其中参数$-\infty<\mu<\infty,\sigma>0$，则称X服从参数为（$\mu$,$\sigma^{2}$）的正态分布，记为$X\sim N(\mu,\sigma^{2})$
  - 密度函数性质，密度函数大于0，密度函数负无穷到无穷积分为1
  - $\begin{gathered}\text{特别当 }\mu=0,\sigma^2=1\text{ 时,称为 标准正态分布,记为}\\X\sim N(0,1)\\\text{其概率密度和分布函数分别为}\\\varphi(x)=\frac1{\sqrt{2\pi}}e^{-\frac{x^2}2},\:\Phi(x)=\int_{-\infty}^{x}\frac1{\sqrt{2\pi}}e^{-\frac{t^2}2}dt\end{gathered}$
  - 性质
    1. y=f(x)关于$x=\mu$对称
    2. 在$\mu$上取最大值，在其左f（x）递增，右递减
    3. 密度函数趋于无穷时为0
- 引理普通正态分布与标准正态分布之间的关系
  - $\begin{aligned}X&\sim N(\mu,\sigma^2)\mathrm{~,~}X\sim N(0,1)\text{之间的关系}\\\text{引理 若}X&\sim N(\mu,\sigma^2),\text{则}Z=\frac{X-\mu}\sigma\sim N(0,1)\end{aligned}$
  - **可以通过该引理将一般情况下的正态分布转化为标准正态分布下的情况进行讨论**
- $3\sigma\text{原则:正态r}.\text{V的值几乎都落在}(\mu-3\sigma,\mu+3\sigma)\text{内}$
- **查表**


这张表格是标准正态分布表，它用来查找标准正态分布的累积分布函数的值，即
$$
\Phi(z)=P(Z \leq z)
$$

其中Z是服从标准正态分布的随机变量，即
$$
Z \sim N(0,1)
$$

- 要学会进行正态分布查表，你需要知道以下几点:
  - 表格的行表示 $z$ 的整数部分和小数点后第一位，例如 $0.0 ， 0.1 ， 0.2$ 等。
  - 表格的列表示 $z$ 的小数点后第二位，例如 $0 ， 1 ， 2 ， 3$ 等。
  - 表格的单元格表示对应的 $\Phi(z)$ 的值，例如 $0.5000 ， 0.5040 ， 0.5080$ 等。
  - 要查找某个 $z$ 值对应的 $\Phi(z)$ 的值，你需要先将z分解为两部分，整数部分和小数点后第一位作为行索引，小数点后第二位作为列索引，然后在表格中找到交叉的单元格，就是你要的结果。
  - 例如，如果你要查找 $z=1.96$ 对应的 $\Phi(z)$ 的值，你可以将 $z$ 分解为 1.9 和 0.06 ，然后在表格中找到第 1.9 行和第 0.06 列的交叉的单元格，就是 0.9750 ，这就是你要的结果。
  - 如果你要查找的z值不在表格中，你可以用最接近的z值来近似，或者用插值法来计算。
  - 例如，如果你要查找 $z=1.96$ 对应的 $\Phi(z)$ 的值，你可以将 $z$ 分解为 1.9 和 0.06 ，然后在表格中找到第 1.9 行和第 0.06 列的交叉的单元格，就是 0.9750 ，这就是你要的结果。
  - 如果你要查找的z值不在表格中，你可以用最接近的z值来近似，或者用插值法来计算。
  - 例如，如果你要查找 $z=1.98$ 对应的 $\Phi(z)$ 的值，你可以用 $z=1.97$ 和 $z=1.99$ 之间的值来近似，即 0.9761 和 0.9772 之间的值，或者用插值法来计算，即

$$
\Phi(1.98) \approx \Phi(1.97)+0.01 \times(\Phi(1.99)-\Phi(1.97)) \approx 0.9761+0.01 \times(0.9772-0.9761) \approx 0.9762
$$


#### 均匀分布

- $\textbf{如果 }\operatorname{r.v}X\textbf{ 的密度函数为}\\f(x)=\left\{\begin{array}{c}\frac1{b-a},a<x<b\\0\text{,其它}\end{array}\right.\\\textbf{则称}X\textbf{ 服从区间}\left(a,b\right)\textbf{上的均匀分布 },\text{记为 }X{\sim}U(a,b)$
- 均匀分布中X落在某区间的概率只与其长度有关（x在有效取值内），而与位置无关

#### 指数分布

- $\begin{aligned}\textbf{如果 }\operatorname{r.v}X\textbf{ 的密度函数为}\\f(x)=\begin{cases}\lambda e^{-\lambda x},x>0\\0\text{ , }x\leq0&\end{cases}\\\text{则称 }X\text{服从参数为}\lambda>0\quad\text{的指数分布,记为}X\sim EXP(\lambda).\end{aligned}$
- 分布函数

$X$ 的分布函数为
$$
\begin{aligned}
F(x) & =\int_{-\infty}^x f(t) d t \\
& =\left\{\begin{array}{cc}
\int_0^x \lambda e^{-\lambda t} d t, x>0 \\
0, & x \leq 0
\end{array}\right. \\
& =\left\{\begin{array}{cc}
1-e^{-\lambda x}, & x>0 \\
0, & x \leq 0
\end{array}\right.
\end{aligned}
$$

##### 与泊松分布的关系

- 泊松分布
  - 在泊松流中,记时间间隔(0,t]中出现的质点数为X
  - $\begin{aligned}\text{则}X\color{red}{\sim}&P(\lambda t),\quad\text{即有}\\&P\{X=k\}=\frac{(\lambda t)^k}{k!}e^{-\lambda t},k=0,1,2,\cdots\end{aligned}$
  - 其中参数为$\lambda>0$，称为泊松强度，代表单位时间内发生的次数
- 记Y表示第一个质点出现的时间，则
  - $P\{Y>t\}=P\{X=0\}=e^{-\lambda t}$表示在0，t时间内Y>t的概率一定为X=0时对应t的泊松分布概率表达式
  - 由此得出Y的分布函数为$F(t)=P\{Y\leq t\}=1-e^{-\lambda t}\quad(t>0)$
    - 即Y符合指数分布

##### 指数分布的无记忆性

- 已经发生的事件的概率并不会影响到进一步发生的概率

设 $X \sim \operatorname{EXP}(\lambda), \forall s>0, t>0$ 考虑概率
$$
\begin{aligned}
P\{X>s+t \mid X>s\}=&\frac{P\{X>s+t, X>s\}}{P\{X>s\}} \\
&=\frac{P\{X>s+t\}}{P\{X>s\}} \\
&=\frac{e^{-\lambda(s+t)}}{e^{-\lambda s}}=e^{-\lambda t} \\
&=1-\left(1-e^{-\lambda t}\right)=1-F(t) \\
&=P\{X>t\}
\end{aligned}
$$

- 应用

响假定自动取款机对每位顾客的服务时间（单位：分钟) 服从 $\lambda=1 / 3$ 的指数分布. 如果有一顾客恰好在你前头走到空闲的取款机，求:
(1) 你至少等候 3 分钟的概率;
(2) 你等候时间在 3 分钟至 6 分钟之间的概率.

(1) $P\{X \geq 3\}=1-F(3)=1-\left(1-e^{-3 \lambda}\right)=e^{-1}=0.368$
(2) 
$\begin{aligned}P\{3 \leq X \leq 6\}=F(6)-F(3) & =\left(1-e^{-6 \lambda}\right)-\left(1-e^{-3 \lambda}\right) \\& =e^{-1}-e^{-2}=0.233\end{aligned}$

- 如果你到达时取款机正在为一名顾客服务，同设没有其他人在排队等候，问题的答案又如何?
**由指数分布的无记忆性，取款机还需要花在你前面顾客身上的服务时间，与他刚到取款机相同，从而问题的答案不变.**


#### 伽马分布

- 指数分布的推广
- 有这样一种元件，它能经受住外界的若干次冲击，但第 r 次冲击来到时，元件失效
- 当 r=1 时，这种元件的寿命服从指数分布
- 当 r 是任意自然数时，元件寿命就是第 r 次冲击来到的时间，记为 X，则 X 是 r.v，它的可靠度函数
  - $\begin{aligned}R(t)&=P\{X>t\}\\&=P\{\textbf{在}(0,t]\textbf{内出现冲击次数不超过}r\text{-1}\}\\&=\sum_{i=0}^{r-1}P\{N_t=i\}\\&=e^{-\lambda t}\sum_{i=0}^{r-1}\frac{(\lambda t)^i}{i!}\end{aligned}$
  - X的密度函数为（$\Sigma 求导？$）
    - $f(t)= \begin{cases}\frac{\lambda^r}{(r-1) !} t^{r-1} e^{-\lambda t}, & t>0 \\ 0, & t \leq 0\end{cases}$
- 一般设X为连续型随机变量
  - 伽马分布的概率密度
    - $f(x)=\begin{cases}\frac{\lambda^r}{\Gamma(r)}x^{r-1}e^{-\lambda x},x>0\\0,&x\leq0&\end{cases}$
    - $\begin{aligned}&\text{其中 }r\text{>0,}\lambda\text{>0 为常数,则称}X\text{服从参数为}(r,\lambda)\text{的 Г 分布,}\\&\text{记为 }X\text{-}\Gamma(r,\lambda)\text{。这里}\\&\Gamma(r)=\int_0^\infty x^{r-1}e^{-x}\mathrm{d}x\quad(r>0)\end{aligned}$
    - $\text{当 }r\text{ 为自然数时, }\Gamma(r)=(r-1)!$,r=1即为指数分布
- 应用：伽马模型对于地震概率的解释
  - 对于任意一次地震，下一次地震紧跟其后的可能性非常大，并且这种可能性随时间单调下降

#### 贝塔分布

- 贝塔密度刻画[0,1]上的随机变量
  - $f(u)=\frac{\Gamma(a+b)}{\Gamma(a)\Gamma(b)}u^{a-1}(1-u)^{b-1},\quad0\leq u\leq1$
  - a=b=1时即为均匀分布
  - 在贝叶斯统计中非常重要

### 概率函数

$$
f(x)\left\{\begin{array}{c}
\text { 对离散型 r.v表示频率函数,即 } \\
f(x)=P\{X=x\}, x=x_1, x_2, \cdots \\
\text { 对连续型 r.v 表示密度函数,即有 } \\
f(x) \geq 0, \int_{-\infty}^{\infty} f(x) d x=1
\end{array}\right.
$$

称 $f(x)$ 为 r.v $X$ 的概率函数

