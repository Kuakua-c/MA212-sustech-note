
# 3-3

## 二维连续型随机变量的分布函数

设 r.v $(X, Y)$ 的联合分布函数(joint CDF)为
$$
F(x, y)=P\{X \leq x, Y \leq y\}
$$

若存在非负可积函数 $f(x, y) \geq 0$ 使得
$$
F(x, y)=\int_{-\infty}^x \int_{-\infty}^y f(u, v) d u d v \quad\left(\forall(x, y) \in R^2\right)
$$

则称 $(X, Y)$ 为二维连续型 $\mathrm{r} . v, f(x, y)$ 称为概率密度函数 (密度函数、密度)，或称为 $X, Y$ 的联合概率密度 (joint pdf)

- 密度函数的本质特征
  - 几何意义上即为以f(x,y)为顶的二重积分的山丘图像
    (1) $f(x, y) \geq 0 \quad\left(\forall(x, y) \in R^2\right)$
    (2) $\int_{-\infty}^{+\infty} \int_{-\infty}^{+\infty} f(u, v) d u d v=1$（**可用于运算确认一些常数，在密度函数含有未知数情况下，使用时注意取值范围**）
    (3) $\forall(D（由逐段光滑曲线围成区域）) \subset R^2$,$P\{(X, Y) \in D\}=\iint_D f(x, y) d x d y$,代表了围成立体图像的体积
    (4) 对于二元函数F(x,y)，通过两次偏导定义其密度函数
        $$
        \begin{aligned}
        f(x, y) & =\frac{\partial^2 F(x, y)}{\partial x \partial y} \\
        & =\lim _{\substack{\Delta x \rightarrow 0^{+} \\
        \Delta y \rightarrow 0^{+}}} \frac{F(x+\Delta x, y+\Delta y)-F(x+\Delta x, y)-F(x, y+\Delta y)+F(x, y)}{\Delta x \Delta y} \\
        & =\lim _{\substack{\Delta x \rightarrow 0^{+} \\
        \Delta y \rightarrow 0^{+}}} \frac{P\{x<X \leq x+\Delta x, y<Y \leq y+\Delta y\}}{\Delta x \Delta y}
        \end{aligned}
        $$
        注：
        故当 $\Delta x \Delta y$ 充分小时, 有
        $$
        P\{x<X \leq x+\Delta x, y<Y \leq y+\Delta y\} \approx f(x, y) \Delta x \Delta y
        $$

例
设 r.v $(X, Y)$ 的概率密度为
$$
f(x, y)=\left\{\begin{array}{cc}
k e^{-(2 x+y)}, & x>0, y>0 \\
0, & \text { 其它 }
\end{array}\right.
$$

(1) 确定常数 $k$;（使用性质2）
(2) 求分布函数 $F(x, y)$;（使用定义式）
(3) 计算概率 $P\{Y \leq X\}$.

- 解答（3）
  - $\begin{aligned} & \text { (3) 记 } D=\{(x, y) \mid y \leq x, x, y \in(-\infty, \infty)\} \\ & \begin{aligned} \therefore \quad P\{Y \leq X\} & =P\{(X, Y) \in D\} \\ & =\iint_D f(x, y) d x d y \\ & =\iint 2 e^{-(2 x+y)} d x d y\end{aligned} \\ & =\int_0^{+\infty}  d y \int_y^{+\infty} 2 e^{-(2 x+y)} d x \\ & =\frac{1}{3}\end{aligned}$
  - 解释，这里相当于是求区域D，满足$y \leq x$和原P区域的交集，即$P\{(X, Y) \in D\}$
- 离散型随机变量的的频率函数（PMF），连续型随机变量的密度函数（PDF）

## 连续型随机变量的边际分布密度

设 $(X, Y)$ 的分布函数和密度函数分别为
$$
F(x, y), f(x, y)
$$
则 r.v $X$ 的分布函数为
$$
\begin{aligned}
F_X(x)=P\{X \leq x\} & =P\{X \leq x, Y<+\infty\} \\
& =\int_{-\infty}^x\left(\int_{-\infty}^{+\infty} f(u, y) d y\right) d u
\end{aligned}
$$

故 r.v $X$ 的密度函数为
$$
f_X(x)=\int_{-\infty}^{+\infty} f(x, y) d y \quad(-\infty<x<+\infty)
$$

同理 $Y$ 的分布函数为
$$
F_Y(y)=\int_{-\infty}^y\left(\int_{-\infty}^{+\infty} f(x, v) d x\right) d v
$$
$\boldsymbol{Y}$ 的密度函数为
$$
f_Y(y)=\int_{-\infty}^{+\infty} f(x, y) d x \quad(-\infty<y<+\infty)
$$

定义 称 $f_X(x)$ 为 $(X, Y)$ 关于 $X$ 的边际密度 (函数).称 $f_Y(y)$ 为 $(X, Y)$ 关于 $Y$ 的边际密度(函数)

- 小f可由F求导得到
- n维情况

设 $X, Y, Z$ 的联合密度函数为
$$
f(x, y, z)
$$

则 r.v $X$ 的一维边际密度函数是
$$
f_X(x)=\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} f(x, y, z) \mathrm{d} y \mathrm{~d} z
$$
r.v $\boldsymbol{X}$ 和 $\boldsymbol{Y}$ 的二维边际密度函数是
$$
f_{X Y}(x, y)=\int_{-\infty}^{\infty} f(x, y, z) \mathrm{d} z
$$

### 连接函数

- 连接函数(copula): 称那些使得边际分布为均匀分布的联合累积分布函数为连接函数, 记为 $C(u, v)$.

具有性质:
1、 $C(u, v)$ 关于每个变量都是非降的;
2、 $P\{U \leq u\}=C(u, 1)=u, C(1, v)=v$.
3 、讨论具有密度函数的连接函数, 此时
$$
c(u, v)=\frac{\partial^2}{\partial u \partial v} C(u, v) \geq 0 .
$$
4、假设 $X$ 和 $Y$ 是分布函数分别为 $F_X(x)$ 和 $F_Y(y)$ 的连续r.v. , 则 $U=F_X(X)$ 和 $V=F_Y(Y)$ 是均匀分布 r.v.对于连接函数 $C(u, v)$, 考虑定义联合分布
$$
F_{X Y}(x, y)=C\left(F_X(x), F_Y(y)\right)
$$

- 则其边际分布为 $F_X(x)$ 和 $F_Y(y)$ ，相应的密度为 $f_{X Y}(x, y)=c\left(F_X(x), F_Y(y)\right) f_X(x) f_Y(y)$

- 说明: 由两个边际分布和任意连接函数, 可以构造出相同边际分布的联合分布, 即: 边际分布不能决定联合分布, 两个变量的相依性由连接函数控制
  - 表明X和Y的联合分布不由他们的边缘分布完全决定，还需要知道它们之间的关系，这个关系由联合分布表示

### 二维正态分布

- 若 $X, Y$ 的联合密度为

$$
f(x, y)=\frac{1}{2 \pi \sigma_1 \sigma_2 \sqrt{1-\rho^2}} e^{\left.-\frac{1}{2\left(1-\rho^2\right)} \frac{\left[\left(x-\mu_1\right)^2\right.}{\sigma_1^2}-2 \rho \frac{\left(x-\mu_1\right)\left(y-\mu_2\right)}{\sigma \sigma_2}+\frac{\left(y-\mu_2\right)^2}{\sigma_2^2}\right]}
$$

- 则称 $(X, Y)$ 服从参数为 $\left(\mu_1, \mu_2, \sigma_1^2, \sigma_2^2, \rho\right)$ 的二维正态分布，记为$(X,Y)~N(\mu_1, \mu_2, \sigma^2_1, \sigma^2_2, \rho) $$\begin{aligned} & \text { 其中各参数满足 }-\infty<\mu_1<+\infty,-\infty<\mu_2<+\infty, \sigma_1>0, \sigma_2>0,|\rho|<1\end{aligned}$
- 定理，符合二维连续正态分布的X，Y（联合分布），X和Y边际分布分别对应有关参数，x和1挂钩，y和2挂钩
原来表述： 若 $(X, Y) \sim N\left(\mu_1, \mu_2, \sigma_1^2, \sigma_2^2, \rho\right)$, 则${X \sim N\left(\mu_1, \sigma_1^2\right)}$，${Y \sim N\left(\mu_2, \sigma_2^2\right)}$
(**推导计算**)
证 $f_X(x)={\int_{-\infty}^{+\infty} f(x, y) d y}$

$$
\begin{aligned}
& =\frac{1}{2 \pi \sigma_1 \sigma_2 \sqrt{1-\rho^2}} e^{-\frac{\left(x-\mu_1\right)^2}{2 \sigma_1^2}} \int_{-\infty}^{\infty} e^{-\frac{1}{2\left(1-\rho^2\right)}\left(\frac{y-\mu_2}{\sigma_2}-\rho \frac{x-\mu_1}{\sigma_1}\right)^2} d y \\
& =\frac{1}{2 \pi \sigma_1} e^{-\frac{\left(x-\mu_1\right)^2}{2 \sigma_1^2} \int_{-\infty}^{\infty} e^{-\frac{t^2}{2}} d t} \\
& =\frac{1}{2 \pi \sigma_1} e^{-\frac{\left(x-\mu_1\right)^2}{2 \sigma_1^2}} \cdot \sqrt{2 \pi} \\
& =\frac{1}{\sqrt{2 \pi} \sigma_1} e^{-\frac{\left(x-\mu_1\right)^2}{2 \sigma_1^2}}
\end{aligned}
$$
其中令$\frac{1}{\sqrt{1-\rho^2}}\left(\frac{y-\mu_2}{\sigma_2}-\rho \frac{x-\mu_1}{\sigma_1}\right)=t$
$\therefore \boldsymbol{X} \sim N\left(\mu_1, \sigma_1^2\right)$ 同理可证 $\boldsymbol{Y} \sim N\left(\mu_2, \sigma_2^2\right)$

- **需要注意的是，具有边际正态的连续随机变量不一定是二维正态分布，其密度函数不一定为二维正态密度**

### 二维均匀分布

- 区域G 上的均匀分布，记作U ( G )，G 是平面上的有界区域, 面积为 A。若随机变量(X,Y)的联合密度函数为$f(x, y)=\left\{\begin{array}{cc}1 / A, & (x, y) \in G \\ 0, & \text { 其他 }\end{array}\right.$，则称(X,Y)服从区域G上的均匀分布
- 在G中有一面积为A1的区域G1，则(X,Y)发生在G1中的概率为A1/A（可以通过直观几何理解）
- 例题
例 设随机变量 $(X, Y)$ 服从区域 $D$ 上的均匀分布.其中 $D=\left\{(x, y) \mid x \geq 0, y \geq 0, x+\frac{y}{2} \leq 1\right\}$,试求随机变量 $(X, Y)$ 的边缘密度函数.

解: 区域 $D$ 的面积为 $A=1$
$(X, Y)$ 的联合密度函数为
$$
f(x, \quad y)= \begin{cases}1, & (x, \quad y) \in D \\ 0, & (x, \quad y) \notin D\end{cases}
$$
当 $0 \leq x \leq 1$ 时,
$$
\begin{aligned}
f_X(x) & =\int_{-\infty}^{+\infty} f(x, \quad y) d y=\int_{-\infty}^0 0 d y+\int_0^{2(1-x)} 1 d y+\int_{2(1-x)}^{+\infty} 0 d y \\
& =2(1-x)
\end{aligned}
$$

当 $x<0$ 或 $x>1$ 时, $f_X(x)=0$
随机变量 $X$ 的边缘密度函数为
$$
f_X(x)=\left\{\begin{array}{cc}
2(1-x) & 0 \leq x \leq 1 \\
0 & \text { 其它 }
\end{array}\right.
$$
同理得Y的