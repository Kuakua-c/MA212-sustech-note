# 总结

$$
\begin{array}{|c|c|c|c|c|c|c|c|c|c|c|c|c|}
\hline  & 累积分布函数（cdf） & 密度函数/频率函数 & 独立性 & 条件函数 & 关系式Y=g（X） & Z=X+Y（卷积） & Z=X/Y & max & min & 边缘分布 & 边缘密度,边缘频率 & 连接函数 \\
\hline 一维离散型 & F(x)=P\{X \leq x\},-\infty<x<\infty &  P\left\{X=x_k\right\}=p_k \quad(k=1,2, \cdots) & P(AB)=P(A)P(B) & P(A|B)=\frac{P(AB)}{P(B)} & \begin{aligned} & F_Y(y)=P\{g(X) \leq y\}= \\ & F_Y(y)=P\left\{X \leq g^{-1}(y)\right\} \end{aligned} &  &  &  &  &  & &\\
\hline 一维连续型 & F(x)=\int_{-\infty}^x f(t) d t,-\infty<x<\infty & \int_{-\infty}^{\infty} f(t) d t=1 & 同上 & 同上 &\begin{aligned} & F_Y(y)=P\{g(X) \leq y\}=\int_{-\infty}^E f_X(x) d x \\ & F_Y(y)=P\left\{X \leq g^{-1}(y)\right\}=\int_{-\infty}^{g^{-1}(y)} f_X(x) \end{aligned} &  & &  &  &  &  & \\
\hline 二维离散型 & \begin{aligned} F(x, y) & \triangleq P(\{X \leq x\} \cap\{Y \leq y\}) \\ & \triangleq P\{X \leq x, Y \leq y\} \end{aligned} & P\left\{X=x_i, Y=y_j\right\}=p\left(x_i, y_j\right) \triangleq p_{i j} \quad(i, j=1,2, \cdots) & \begin{aligned}&P\{X \leq x, Y \leq y\}=P\{X \leq x\} \cdot P\{Y \leq y\}\\&F(x, y)=F_X(x) \cdot F_Y(y)\end{aligned} 概率分布上表示P\left(X=x_i, Y=y_j\right)=P\left(X=x_i\right) P\left(Y=y_j\right) & P\left\{X=x_i \mid Y=y_j\right\}=\frac{P\left\{X=x_i, Y=y_j\right\}}{P\left\{Y=y_j\right\}}=\frac{p_{i j}}{p_{\cdot j}} \quad(i=1,2, \cdots) &  & XY相互独立\begin{aligned}P\{Z=k\} & =\sum_{i=1}^{k-1} P\{X=i\} \cdot P\{Y=k-i\} \\& =\sum_{i=1}^{k-1} P\{X=k-i\} \cdot P\{Y=i\} \\& (k=1,2, \ldots)\end{aligned} &  &  &  & F_X(x) = P\{X \leq x\} = P\{X \leq x, Y < \infty\} = F(x, \infty) &  P\left\{X=x_i, Y=y_j\right\}=p_{i j} \quad(i, j=1,2, \cdots) \begin{aligned} P\left\{X=x_i\right\} & =P\left(\left\{X=x_i\right\} \cap \Omega\right) \triangleq p_i . \quad(i=1,2, \cdots) \\& =P\left(\left\{X=x_i\right\} \cap\left(\bigcup_{j=1}^{\infty}\left\{Y=y_j\right\}\right)\right) \\& =P\left(\bigcup_{j=1}^{\infty}\left(\left\{X=x_i\right\} \cap\left\{Y=y_j\right\}\right)\right) \\& =P\left(\bigcup_{j=1}^{\infty}\left\{X=x_i, Y=y_j\right\}\right) \\& =\sum_{j=1}^{\infty} P\left\{X=x_i, Y=y_j\right\} \\& =\sum_{j=1}^{\infty} p_{i j} \end{aligned} & \\
\hline 二维连续型 & F(x, y)=P\{X \leq x, Y \leq y\}=\int_{-\infty}^x \int_{-\infty}^y f(u, v) d u d v \quad\left(\forall(x, y) \in R^2\right) & \begin{aligned} f(x, y) & =\frac{\partial^2 F(x, y)}{\partial x \partial y} \\ & =\lim _{\substack{\Delta x \rightarrow 0^{+} \\ \Delta y \rightarrow 0^{+}}} \frac{F(x+\Delta x, y+\Delta y)-F(x+\Delta x, y)-F(x, y+\Delta y)+F(x, y)}{\Delta x \Delta y} \\ & =\lim _{\substack{\Delta x \rightarrow 0^{+} \\ \Delta y \rightarrow 0^{+}}} \frac{P\{x<X \leq x+\Delta x, y<Y \leq y+\Delta y\}}{\Delta x \Delta y}\end{aligned} & \begin{aligned}\int_{-\infty}^x \int_{-\infty}^y f(u, v) d u d v & =P\{X \leq x, Y \leq y\} \\& =P\{X \leq x\} P\{Y \leq y\} \\& =\int_{-\infty}^x f_X(u) d u \cdot \int_{-\infty}^y f_Y(v) d v \\& =\int_{-\infty}^x \int_{-\infty}^y f_X(u) f_Y(v) d u d v\end{aligned}f(x, y)=f_X(x) f_Y(y)& P\{X \leq x \mid y<Y \leq y+\varepsilon\}=\frac{P\{X \leq x, y<Y \leq y+\varepsilon\}}{P\{y<Y \leq y+\varepsilon\}}=\frac{\int_{-\infty}^x \int_y^{y+\varepsilon} f(u, v) d v d u}{\int_y^{y+\varepsilon} f_Y(v) d v}应用积分中值定理\begin{aligned}& =\frac{\varepsilon \int_{-\infty}^x f\left(u, y_{\varepsilon}\right) d u}{\varepsilon f_Y\left(\tilde{y}_{\varepsilon}\right)} \\& \rightarrow \int_{-\infty}^x \frac{f(u, y)}{f_Y(y)} d u \quad(\varepsilon \rightarrow 0)\end{aligned} &  & \begin{aligned}& F_Z(z)=P\{Z \leq z\}=P\{X+Y \leq z\} \\& =\iint_{x+y \leq z}^{\infty} f(x, y) d x d y \\& =\int_{-\infty}^{\infty} d y \int_{-\infty}^{z-y} f(x, y) d x \\& \stackrel{\text { 今 } x=u-y}{=} \int_{-\infty}^{\infty} \int_{-\infty}^z f(u-y, y) d u d y \\& =\int_{-\infty}^z\left[\int_{-\infty}^{\infty} f(u-y, y) d y\right] d u \\& \therefore f_Z(z)=\int_{-\infty}^{\infty} f(z-y, y) d y \\& =\int_{-\infty}^{\infty} f(x, z-x) d x\end{aligned} & F_Z(z)=P\{X / Y \leq z\}=\iint_{\frac{z}{y} \leq z} f(x, y) \mathrm{d} x \mathrm{~d} y =\int_0^{+\infty} \mathrm{d} y \int_{-\infty}^{y z} f(x, y) \mathrm{d} x+\int_{-\infty}^0 \mathrm{~d} y \int_{y z}^{+\infty} f(x, y) \mathrm{d} x \begin{gathered}J=\frac{\partial(x, y)}{\partial(u, v)}=\left|\begin{array}{cc}\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}\end{array}\right| \neq 0 \\\iint_{\Omega} f(x, y) d x d y=\iint_{\Omega^{\prime}} f[x(u, v), y(u, v)]|J| d u d v\end{gathered}& \begin{aligned}F_{\max }(z) & =P\{\max (X, Y) \leq z\} \\& =P\{X \leq z, Y \leq z\} \\& =P\{X \leq z\} \cdot P\{Y \leq z\} \\& =F_X(z) \cdot F_Y(z) \end{aligned}& \begin{aligned}F_{\min }(z) & =P\{\min (X, Y) \leq z\} \\& =1-P\{\min (X, Y)>z\} \\& =1-P\{X>z, Y>z\} \\& =1-P\{X>z\} \cdot P\{Y>z\} \\& =1-[1-P\{X \leq z\}] \cdot[1-P\{Y \leq z\}] \\& =1-\left[1-F_X(z)\right] \cdot\left[1-F_Y(z)\right]\end{aligned} &\begin{aligned} F_X(x)=P\{X \leq x\} & =P\{X \leq x, Y<+\infty\} \\& =\int_{-\infty}^x\left(\int_{-\infty}^{+\infty} f(u, y) d y\right) d u\end{aligned} & f_X(x)=\int_{-\infty}^{+\infty} f(x, y) d y \quad(-\infty<x<+\infty)& F_{X Y}(x, y)=C\left(F_X(x), F_Y(y)\right),则其边际分布为 F_X(x) 和 F_Y(y) ，相应的密度为 f_{X Y}(x, y)=c\left(F_X(x), F_Y(y)\right) f_X(x) f_Y(y) \\
\hline  &  &  &  &  &  &  &  &  &  &  & & 
\end{array}
$$