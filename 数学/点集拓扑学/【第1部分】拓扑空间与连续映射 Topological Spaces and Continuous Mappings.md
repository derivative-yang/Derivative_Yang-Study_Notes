# 第1节 度量拓扑
## 1-1 度量空间
在集合上定义拓扑，最重要最常用的方法之一就是度量。
> [!度量]
> 集合  $X$  的一个 **度量(metric)** 是一个函数（称为**度量函数 distance func**）$d: X \times X \rightarrow \mathbb {R}_{\geq 0}$  s.t.
> 
> ==(d1)(非负性 non neg)== $\forall x,y\in X,d(x,y)\geq 0\land(d(x,y)=0\iff x = y)$
> 
> ==(d2)(对称性 symm)==  $\forall x,y\in X,d(x,y) = d(y,x)$  
> 
> ==(d3)(三角不等式 tria.ineq)== $\forall x, y, z \in X,d(x, y) + d(y, z) \geq d(x, z)$
> 
> 若上述条件满足，$(X,d)$ 称为**度量空间**

> [!warning] RMK
> 由于我们在定义 $d$ 时已经说了映到 $\mathbb {R}_{\geq 0}$，==(d1)==可简写为$$\forall x,y\in X,   d(x,y)=0\iff x = y$$

 > [!warning] RMK
> 深圳到广州再到汕头如果比深圳直接到汕头便宜，就不满足==tria.ineq==

> [!距离]
> $(X,d)$ 度量空间，$d(x, y)$  称  $x$  与  $y$  间在度量  $d$  下的**距离(distance)**

> [!quote] EX 0
> $X=\mathbb{R}$
> $d(x,y)=|x-y|$ 
> $\Rightarrow(X,d)$是度量空间


> [!quote] EX 1a
> $X$ fin
> $d(x,y)=\begin{cases} 1&x\neq y \\ 0&x=y\end{cases}$ 
> $\Rightarrow(X,d)$是度量空间

> [!离散度量]
> 这个度量称为**离散度量(discrete metric)**

> [!quote] EX 1b
> $X$ fin set of vertices of a connected graph
> <img src = "Pasted image 20251017173258.png" width = 100>
> $d(x,y)=\min\{\text{weigth of a path x}\leftrightarrow\text{y}\}$ （即最短路径） 
> $\Rightarrow(X,d)$是度量空间

> [!quote] EX 2a(欧氏度量 Euclidean metric in $\mathbb{R}^n$)
> $X=\mathbb{R}^n$
> 
> sps $\begin{cases} x=(x_1,\cdots,x_n) \\  y=(y_1,\cdots,y_n)\end{cases}$
> 
> $d(x,y)=\sqrt{(x_1-y_1)^2+\cdots+(x_n-y_n)^2}$ 
> $\Rightarrow(X,d)$是度量空间

> [!quote] Q
> pf the ==tria.ineq==
> 

> [!quote] EX 2b(曼哈顿度量 Manhattan metric in $\mathbb{R}^n$)
> $X=\mathbb{R}^n$
> 
> sps $\begin{cases} x=(x_1,\cdots,x_n) \\  y=(y_1,\cdots,y_n)\end{cases}$
> <img src = "Pasted image 20251017172046.png" width = 100>
> $d(x,y)=|x_1-y_1|\cdots+|x_n-y_n|$ 
> $\Rightarrow(X,d)$是度量空间
> 

> [!quote] Q
> pf the ==tria.ineq==
> 

since $\forall i\in\{1,\cdots,n\},|x_i-z_i|\leq|x_i-y_i|+|y_i-z_i|$
$$d(x,y)\leq d(x,y)+d(y,z)$$

---
> [!quote] EX 2c（平方度量(square metric) in $\mathbb{R}^n$)
> $X=\mathbb{R}^n$
> 
> sps $\begin{cases} x=(x_1,\cdots,x_n) \\  y=(y_1,\cdots,y_n)\end{cases}$
> 
> $d_{\infty}(x,y)=\underset{i\in\{1,\cdots,n\}}{\max}|x_i-y_i|$
> 
> $\Rightarrow(X,d)$是度量空间

> [!quote] Q
> pf the ==tria.ineq==
> 

> [!quote] EX 3（Amazon basin metric)
> $X=\mathbb{R}^2$
> 
> sps $\begin{cases} p=(x,y) \\ p'=(x',y') \end{cases}$
> <img src="Pasted image 20251017173156.png" width = 400>
> $d(p,p')=\begin{cases} |x-x'|+|y|+|y'|& x\neq x' \\ |y-y'| & x= x'\end{cases}$
> 
> $\Rightarrow(X,d)$是度量空间

> [!quote] EX 4a、4b (sup-metric and metric of cont func)
> $X=C[0,1]$
> 
> sup-metric  $d(f,g)=\underset{x\in[0,1]}{\max}|f(x)-g(x)|$
> metric  $d(f,g)=\displaystyle\int_0^1|f(x)-g(x)|dx$

> [!warning] RMK
> $C[0,1]$ 不能改成可积函数，比如$f(x) = \begin{cases} 1&x=\displaystyle\frac{1}{2}\\0&x\neq\displaystyle\frac{1}{2}\end{cases}$   $g(x) = \begin{cases} 1&x=\displaystyle\frac{1}{3}\\0&x\neq\displaystyle\frac{1}{3}\end{cases}$
> $d(f,g)=\displaystyle\int_0^1|f(x)-g(x)|dx$，但$f(x)\neq g(x)$

## 练习

> [!quote] Q
> 是否存在一个度量空间 $X$ 使得 $U_R(y)\subsetneq U_r(x),r<R$ ?

> [!quote] Q
> 在 $\mathbb{R}^2$ 中画出球心为$(0,0)$ 的开球，带有范数
> 1.  $|\cdot|_1$
> 2.  $|\cdot|_2$
> 3.  $|\cdot|_\infty$

> [!quote] Q
> 在 $(\mathbb{R}^2,d)$ 中画出以
> 4. $(0,0)$
> 5. $(0,1)$
> 为球心的开球，其中 $d$ 为 Amazon Basin度量

## 1-2 范数与 $l_p$ 空间
> [!范数，赋范空间]
> $\mathbb{F}-$线性空间  $V$  的一个 **范数(norm)** 是一个函数$\|\cdot\|: V \times V \rightarrow \mathbb {R}_{\geq 0}$  s.t.
> 
> ==(n1)(非负性 non neg)== $\forall v\in V,$    $\|v\|\geq 0\land(\|v\|=0\iff v=0)$
> 
> ==(n2)(齐次性 homogeneity)==$\forall v\in V,\lambda\in\mathbb{F},$   $\|\lambda v\| =|\lambda|\| v\|$  
> 
> ==(n3)(三角不等式 tria.ineq)== $\forall v,w \in V,$  $\|v+w\|\leq\|v\| + \|w\|$
> 
> 若上述条件满足，$(V,\|\cdot\|)$ 称为**赋范空间**

> [!warning] RMK
> 由于我们在定义 $\|\cdot\|$ 时已经说了映到 $\mathbb {R}_{\geq 0}$，==(n1)==可简写为$$\forall v\in V,\|v\|=0\iff v=0$$

> [!warning] RMK
> 范数在线性空间上定义了一个度量：$d(x,y)=\|x-y\|$

> [!quote] EX 2a,2b,2c,4a,4b comes from norm
>for $v\in\mathbb{R}^n$
>- EX 2a $\|v\|=\sqrt{x_1^2+\cdots+x_n^2}$
> - EX 2b $\|v\|=|x_1|+\cdots+|x_n|$
> - EX 2c $\|v\|=\underset{i\in\{1,\cdots,n\}}{\max}|x_i|$
>
> for $f\in C[0,1]$
>  - EX 4a $\|f\|=\max|f(x)|$ (called sup-norm)
> - EX 4b $\|f\|=\displaystyle\int_0^1f(x)dx$

> [! ] $l^p$ 空间（p次可和序列空间）
> for $1\leq p< \infty(p\in\mathbb{R}_{\geq1})$
> $$l_p:=\{\{x_n\}\,\,\text{seq}: \sum|x_i|^p<\infty\land \|x\|_p=(\sum|x_i|^p)^{\frac{1}{p}}\}$$
> for $p = \infty$
> $$l_p:=\{\{x_n\}\,\,\text{seq}: \lim_{p\to\infty}(\sum|x_i|^p)<\infty\land \|x\|_{\infty}=\lim_{p\to\infty}(\sum|x_i|^p)^{\frac{1}{p}}\}$$

> [!quote] EX
> - $l^1$空间，所有绝对收敛列构成的空间
> $$\{\{x_n\}\,\,\text{seq}: \sum|x_i|<\infty\land \|x\|_1=\sum|x_i|\}$$
> - $l^2$空间，所有平方收敛级数列构成的空间(此即无穷维内积空间)
> $$\{\{x_n\}\,\,\text{seq}: \sum x_i^2<\infty\land \|x\|_2=\sqrt{\sum x_i^2}\}$$
> - $l^{\infty}$空间，所有有界数列构成的空间
> $$\{\{x_n\}\,\,\text{seq}:\{x_n\}\,\,\text{bdd}\land \|x\|_{\infty}=\sup_i|x_i|\}$$
> 

> [!quote] PROP
> $l^p\subset l^q$ if $p<q$
> 

> [!quote] EX
> $\displaystyle x_n=\frac{1}{n},\sum\frac{1}{n}<\infty$ but $\displaystyle \sum\frac{1}{n^2}<\infty$
> 
> $\Rightarrow \{x_n\} \in l^2$ but $\notin l^1$
> 

> [!quote] THM
> $l^p$ are normed sp
> 

## 1-3 内积空间

> [!内积，内积空间]
> $\mathbb{F}-$线性空间  $V$  的一个 **内积(inner prod)** 是一个函数$\langle\cdot,\cdot\rangle: V \times V \rightarrow \mathbb {F}$ s.t.
> 
> ==(i1)(共轭对称性 conjugate symm)== $\forall v,w\in V,$   $\langle v,w\rangle = \overline{\langle w,v\rangle}$
> 
> ==(i2)(双线性性 bilin)==$\forall v,v',w\in V,\lambda\in\mathbb{F},$   $\begin{cases}\langle \lambda v,w\rangle = \lambda\langle v,w\rangle \\ \langle  v+v',w\rangle = \langle v,w\rangle+\langle v',w\rangle\end{cases}$
> 
> ==(i3)(正定性 positive dedinite)== $\forall v\in V,$    $\langle v,v\rangle\geq 0\land(\langle v,v\rangle=0\iff v=0)$
> 
> 若上述条件满足，$(V,\langle\cdot,\cdot\rangle)$ 称为**内积空间**

> [!warning] RMK
> 此处 ==(i3)== 不可简写为$$\forall v\in V,\langle v,v\rangle=0\iff v=0$$
> 因为正定性是对 $\langle v,v\rangle$ 而言，不是 $\langle v,w\rangle$
> 在度量空间定义中我们有$d(v,w)\geq 0$
> 在赋范空间定义中我们有$\|v\|\geq 0$
> 这两个是恒正的，而内积 $\langle v,w\rangle$ 不一定恒正，甚至可以为复数

> [!实内积空间与复内积空间]
> 如果$\mathbb {F}=\mathbb {R}$ 称**实内积空间**
> 如果$\mathbb {F}=\mathbb {C}$ 称**复内积空间**

> [!warning] RMK
> 此处定义中，注意标量域和内积的陪域都要一起切换成对应数域

> [!欧几里得空间]
> 有限维实内积空间称**欧几里得空间(Euclidean sp)**，即带有标准内积（点积 dot product）的$\mathbb{R}^n$

> [!quote] THM(欧几里得空间中的柯西-施瓦茨不等式 Cauchy-Schwarz ineq in Euclidean sp)
> 在欧几里得空间中：
> $(\langle v,w\rangle)^2 \leq\|v\|^2\|w\|^2=\langle v,v\rangle\langle w,w\rangle$ 
> (equality:$|\langle v,w\rangle| \leq\|v\|^2\|w\|$)

sps $v=(a_1,\cdots,a_n)$，  $w=(b_1,\cdots,b_n )$
NTP$\displaystyle\left| \sum_{i=1}^n a_i \overline{b_i} \right|^2 \leq \left( \sum_{i=1}^n |a_i|^2 \right) \left( \sum_{i=1}^n |b_i|^2 \right)$
$$
P(t) = \sum_{i=1}^n |a_i + t b_i|^2 \geq 0, \quad \text{对所有实数 } t
$$
$$
\begin{align*}
P(t) &= \sum_{i=1}^n (a_i + t b_i)(\overline{a_i} + t \overline{b_i}) \\
&= \sum_{i=1}^n \left( |a_i|^2 + t a_i \overline{b_i} + t \overline{a_i} b_i + t^2 |b_i|^2 \right) \\
&= \left( \sum_{i=1}^n |a_i|^2 \right) + t \left( \sum_{i=1}^n a_i \overline{b_i} \right) + t \left( \sum_{i=1}^n \overline{a_i} b_i \right) + t^2 \left( \sum_{i=1}^n |b_i|^2 \right)
\end{align*}
$$

记
$$A = \sum_{i=1}^n |a_i|^2 \quad B = \sum_{i=1}^n a_i \overline{b_i} \quad C = \sum_{i=1}^n |b_i|^2$$
则
$$
P(t) = A + B t + \overline{B} t + C t^2
$$
由 $B + \overline{B} = 2 \Re(B)$
$$
P(t) = A + 2 \Re(B) t + C t^2
$$
由于 $P(t) \geq 0$ 对所有实数 $t$ 成立，该二次函数的判别式必须非正：
$$
(2 \Re(B))^2 - 4 A C \leq 0
$$
即
$$
4 (\Re(B))^2 \leq 4 A C \quad \Rightarrow \quad (\Re(B))^2 \leq A C
$$
特别地，取 $B = \displaystyle\sum_{i=1}^n a_i \overline{b_i}$，有
$$
|B|^2 = (\Re(B))^2 + (\Im(B))^2 \geq (\Re(B))^2 \leq A C
$$
因此
$$
\left| \sum_{i=1}^n a_i \overline{b_i} \right|^2 \leq \left( \sum_{i=1}^n |a_i|^2 \right) \left( \sum_{i=1}^n |b_i|^2 \right)
$$

---
> [!quote] THM(内积空间中的柯西-施瓦茨不等式 Cauchy-Schwarz ineq)
> 在内积空间中：
> $(\langle v,w\rangle)^2 \leq\|v\|^2\|w\|^2=\langle v,v\rangle\langle w,w\rangle$ 
> (equality:$|\langle v,w\rangle| \leq\|v\|^2\|w\|$)
> 等号成立当且仅当$v$和$w$线性相关

> [!quote] PROP
> $\|v\| =\sqrt{\langle v,v\rangle}$ norm on V
> 

==(n1)== following by ==(i3)==
==(n2)== $\forall v\in V,\lambda\in\mathbb{F},$   $\|\lambda v\|=\sqrt{\langle \lambda v,\lambda v\rangle} =\sqrt{\lambda^2\langle  v, v\rangle}=|\lambda|\sqrt{\langle  v, v\rangle}=|\lambda|\| v\|$  
==(n3)== by Cauchy-Schwarz

---
> [!quote] COR
> $l^2$ norm satisfies tria.ineq
> 

$l^2$ is a Euclidean sp:

$$\begin{cases} x=(x_1,\cdots,x_n) \\  y=(y_1,\cdots,y_n)\end{cases}$$
$$(\langle x,y\rangle =\sum x_i y_i)\land(\|x\|_2=\sqrt{\langle x,x\rangle})$$ 
---
> [!warning] RMK
>$\|x\|_p$ does not come from ip for $p\neq2$

## 1-4 共轭指数与lp空间的三角不等式

> [!共轭指数]
> $p,q\in\mathbb{R},$ 称 $p$ 和 $q$ 为**共轭指数(conjugate indices)** 若$\displaystyle\frac{1}{p}+\frac{1}{q}=1$
> 定义 $1$ 和 $\infty$ 为共轭指数

> [!quote] EX
> 2和2是共轭指数，故2是唯一的**自共轭指数（self-conjugate indices）**

 > [!warning] RMK
> 事实上 Euclidean sp 是自对偶(self-dual)的，即
> $$V^*=V,f_v(w)=\langle v,w\rangle$$
> $l^p$ 和 $l^q$ 是对偶的($(l^p)^*=l^q$) 若$p$ 和 $q$ 为共轭指数

> [!quote] THM（凸函数的Jensen 不等式）
>  $\varphi : I \to \mathbb{R}$ 是区间 $I \subset \mathbb{R}$ 上的凸函数，$x_1, x_2, \dots, x_n \in I$，$\lambda_1, \lambda_2, \dots, \lambda_n \ge 0$，且 $\displaystyle\sum_{i=1}^n \lambda_i = 1$
> 则$$\varphi\left( \sum_{i=1}^n \lambda_i x_i \right) \le \sum_{i=1}^n \lambda_i \varphi(x_i)$$
> 如果 $\varphi$ 是严格凸的，那么等号成立当且仅当 $x_1 = x_2 = \dots = x_n$

用数学归纳法
($n=2$)
由凸函数定义：对 $t \in [0,1]$，有
$$
\varphi(t x_1 + (1-t) x_2) \le t \varphi(x_1) + (1-t) \varphi(x_2).
$$
取 $t = \lambda_1$，$\lambda_2 = 1-t$，则 $n=2$ 成立
$(k\Rightarrow k+1)$
sps 对任意 $k$ 个非负权重 $\lambda_i$ 满足 $\sum_{i=1}^k \lambda_i = 1$，有
$$
\varphi\left( \sum_{i=1}^k \lambda_i x_i \right) \le \sum_{i=1}^k \lambda_i \varphi(x_i).
$$


设 $\lambda_1, \dots, \lambda_{k+1} \ge 0$，$\displaystyle\sum_{i=1}^{k+1} \lambda_i = 1$ 
如果 $\lambda_{k+1} = 1$，则其他 $\lambda_i=0$，结论显然成立  
假设 $\lambda_{k+1} < 1$，令$$t = 1 - \lambda_{k+1} = \sum_{i=1}^k \lambda_i > 0$$
定义$$y = \sum_{i=1}^k \frac{\lambda_i}{t} x_i$$
则 $\displaystyle\sum_{i=1}^k \frac{\lambda_i}{t} = 1$，且 $y \in I$

故$$\sum_{i=1}^{k+1} \lambda_i x_i = t y + \lambda_{k+1} x_{k+1}$$
由 $n=2$ 的情况$$\varphi\left( t y + \lambda_{k+1} x_{k+1} \right) \le t \varphi(y) + \lambda_{k+1} \varphi(x_{k+1})$$
由归纳假设（$n=k$）
$$
\varphi(y) = \varphi\left( \sum_{i=1}^k \frac{\lambda_i}{t} x_i \right) \le \sum_{i=1}^k \frac{\lambda_i}{t} \varphi(x_i).
$$
代入得$$\varphi\left( \sum_{i=1}^{k+1} \lambda_i x_i \right) \le t \sum_{i=1}^k \frac{\lambda_i}{t} \varphi(x_i) + \lambda_{k+1} \varphi(x_{k+1}) = \sum_{i=1}^{k+1} \lambda_i \varphi(x_i)$$

---

> [!quote] THM（凹函数的Jensen 不等式）
>  $\psi : I \to \mathbb{R}$ 是区间 $I \subset \mathbb{R}$ 上的凹函数， $x_1, x_2, \dots, x_n \in I$，$\lambda_1, \lambda_2, \dots, \lambda_n \ge 0$， $\displaystyle\sum_{i=1}^n \lambda_i = 1$
> 则
> $$
> \psi\left( \sum_{i=1}^n \lambda_i x_i \right) \ge \sum_{i=1}^n \lambda_i \psi(x_i).
> $$
> 如果 $\psi$ 是严格凹的，那么等号成立当且仅当 $x_1 = x_2 = \dots = x_n$

证明同理。

---

> [!quote] THM（杨格不等式，Young ineq）
> $p$ 和 $q$ 为共轭指数，则$$ab\leq \frac{a^p}{p}+\frac{b^q}{q}$$
> 等号成立当且仅当 $a^p = b^q$

函数 $\ln(x)$ 在 $(0, +\infty)$ 上是凹函数（因为二阶导数为 $\displaystyle-\frac{1}{x^2} < 0$）
由凹函数的Jensen 不等式$$
\ln(\lambda u + (1-\lambda) v) \ge \lambda \ln u + (1-\lambda) \ln v,
$$  其中 $\lambda \in (0,1)$，$u, v > 0$
取  $$\lambda = \frac{1}{p}, \quad 1-\lambda = \frac{1}{q}, \quad u = a^p, \quad v = b^q$$
代入得$$\ln\left( \frac{a^p}{p} + \frac{b^q}{q} \right)
\ge \frac{1}{p} \ln(a^p) + \frac{1}{q} \ln(b^q)$$$$
RHS=\frac{1}{p} \cdot p \ln a + \frac{1}{q} \cdot q \ln b = \ln a + \ln b = \ln(ab)
$$  故$$\ln\left( \frac{a^p}{p} + \frac{b^q}{q} \right) \ge \ln(ab)$$
由于 $\ln$ 单调递增，去掉对数得$$\frac{a^p}{p} + \frac{b^q}{q} \ge ab$$
等号成立当且仅当 $u = v$，即 $a^p = b^q$

---
> [!quote] THM（郝尔德不等式，Hölder ineq）
> $p$ 和 $q$ 为共轭指数，$\forall i\in\{1,\cdots,n\},a_i,b_i>0$，则$$\sum_{k=1}^na_kb_k\leq (\sum a_k^p)^{\frac{1}{p}}(\sum b_k^q)^{\frac{1}{q}}$$
> 即$$\|a\|_1\|b\|_1\leq\|a\|_p\|b\|_p$$

令  $$A = \left( \sum_{k=1}^n a_k^p \right)^{1/p}, \quad B = \left( \sum_{k=1}^n b_k^q \right)^{1/q}$$
如果 $A=0$ 或 $B=0$，则 $a_k=0$ 或 $b_k=0$ 对所有 $k$ 成立，不等式显然成立（两边为 0）。  
下设 $A>0$，$B>0$
对每个 $k$，令  $$x_k = \frac{a_k}{A}, \quad y_k = \frac{b_k}{B}$$
由Young 不等式 $$x_k y_k \le \frac{x_k^p}{p} + \frac{y_k^q}{q}$$
代入$\displaystyle x_k = \frac{a_k}{A}, \quad y_k = \frac{b_k}{B}$ $$\frac{a_k b_k}{A B} \le \frac{1}{p} \cdot \frac{a_k^p}{A^p} + \frac{1}{q} \cdot \frac{b_k^q}{B^q}$$对 $k=1$ 到 $n$ 求和
$$\frac{\sum_{k=1}^n a_k b_k}{A B} \le \frac{1}{p A^p} \sum_{k=1}^n a_k^p + \frac{1}{q B^q} \sum_{k=1}^n b_k^q$$
由 $A^p = \displaystyle\sum_{k=1}^n a_k^p$，$B^q = \displaystyle\sum_{k=1}^n b_k^q$  $$\frac{\sum_{k=1}^n a_k b_k}{A B} \le \frac{1}{p} + \frac{1}{q} = 1$$
因此  
$$
\sum_{k=1}^n a_k b_k \le A B = \left( \sum_{k=1}^n a_k^p \right)^{1/p} \left( \sum_{k=1}^n b_k^q \right)^{1/q}
$$

---

> [!quote] THM（闵可夫斯基不等式，Minkowski ineq）（$l^p$ 空间中的三角不等式）
> 设 $p \ge 1$，$a_1, \dots, a_n > 0$，$b_1, \dots, b_n > 0$，则  
> $$
> \left( \sum_{k=1}^n (a_k + b_k)^p \right)^{1/p} \le \left( \sum_{k=1}^n a_k^p \right)^{1/p} + \left( \sum_{k=1}^n b_k^p \right)^{1/p}
> $$
> 即$$\|a+b\|_p\leq\|a\|_p+\|b\|_p$$

当 $p=1$ 时，三角不等式显然成立
下设 $p > 1$
记 $q$ 为 $p$ 的共轭指数，即 $\displaystyle\frac{1}{p} + \frac{1}{q} = 1$，亦即 $q = \displaystyle\frac{p}{p-1}$
考虑和式
$$
S = \sum_{k=1}^n (a_k + b_k)^p=\sum_{k=1}^n (a_k + b_k) \cdot (a_k + b_k)^{p-1}
$$
拆开$$S = \sum_{k=1}^n a_k (a_k + b_k)^{p-1} + \sum_{k=1}^n b_k (a_k + b_k)^{p-1}$$
对第一项应用Hölder 不等式
$$\sum_{k=1}^n a_k (a_k + b_k)^{p-1} \le \left( \sum_{k=1}^n a_k^p \right)^{1/p} \left( \sum_{k=1}^n (a_k + b_k)^{(p-1)q} \right)^{1/q}$$
因为 $(p-1)q = p$
$$\sum_{k=1}^n a_k (a_k + b_k)^{p-1} \le \left( \sum_{k=1}^n a_k^p \right)^{1/p} \left( \sum_{k=1}^n (a_k + b_k)^p \right)^{1/q}$$
同理，对第二项
$$\sum_{k=1}^n b_k (a_k + b_k)^{p-1} \le \left( \sum_{k=1}^n b_k^p \right)^{1/p} \left( \sum_{k=1}^n (a_k + b_k)^p \right)^{1/q}$$
两式相加$$S \le \left[ \left( \sum_{k=1}^n a_k^p \right)^{1/p} + \left( \sum_{k=1}^n b_k^p \right)^{1/p} \right] \cdot \left( \sum_{k=1}^n (a_k + b_k)^p \right)^{1/q}$$
但 $S =\displaystyle\sum_{k=1}^n (a_k + b_k)^p$，故
$$\sum_{k=1}^n (a_k + b_k)^p \le \left[ \left( \sum a_k^p \right)^{1/p} + \left( \sum b_k^p \right)^{1/p} \right] \cdot \left( \sum (a_k + b_k)^p \right)^{1/q}$$
两边同除 $\displaystyle\left( \sum (a_k + b_k)^p \right)^{\frac{1}{q}}$（若 $S=0$ 则不等式显然成立）
$$\left( \sum_{k=1}^n (a_k + b_k)^p \right)^{1 - 1/q} \le \left( \sum a_k^p \right)^{1/p} + \left( \sum b_k^p \right)^{1/p}$$
由 $\displaystyle1 - \frac{1}{q} = \frac{1}{p}$
$$
\left( \sum_{k=1}^n (a_k + b_k)^p \right)^{1/p} \le \left( \sum a_k^p \right)^{1/p} + \left( \sum b_k^p \right)^{1/p}
$$
---

## 1-5 度量空间中的开集

> [! ] 以  $x$  为中心的  $\pmb{\varepsilon}$ -球( $\pmb{\varepsilon}$-ball centered at $x$)($\pmb{\varepsilon}$ -邻域( $\pmb{\varepsilon}$-nbhd centered at $x$))
> $(X,d)$ 度量空间，$x\in X$
> $\forall\epsilon > 0$ ，**以 $x$  为中心的  $\pmb{\varepsilon}$ -球( $\pmb{\varepsilon}$-ball centered at  $x$)($\pmb{\varepsilon}$ -邻域( $\pmb{\varepsilon}$-nbhd centered at $x$))** $B _ {d} (x, \varepsilon) = \{y\in X \mid d (x, y) <\varepsilon \}$
> 在不混淆的情况下，有时在记号中省略度量 $d$ ，简记为  $B(x,\varepsilon)$ 或 $U_{\varepsilon} (x)$

> [! ] 以  $x$  为中心的  $\pmb{\varepsilon}$-去心邻域( $\pmb{\varepsilon}$-punctured nbhd centered at $x$)
> $(X,d)$ 度量空间，$x\in X$
> $\forall\epsilon > 0$ ，**以  $x$  为中心的  $\pmb{\varepsilon}$-去心邻域( $\pmb{\varepsilon}$-punctured nbhd centered at $x$)** $\mathring B _ {d} (x, \varepsilon) = \{y\in X \mid 0<d (x, y) <\varepsilon \}=B _ {d} (x, \varepsilon)\backslash\{x\}$
> 在不混淆的情况下，有时在记号中省略度量 $d$ ，简记为  $\mathring B(x,\varepsilon)$ 或 $\mathring U_{\varepsilon} (x)$

> [!quote] 度量空间中的开集
>$(X,d)$ metric.sp， $\forall M\in X,M$ is open in X if$$\forall x\in M,\exists \varepsilon >0,U_{\varepsilon}(x)\subseteq M$$
> 

> [!quote] PROP
> $(X,d)$ metric.sp，$\varnothing,X$ are open in X.
> 
> 

> [!quote] THM
> $(X,d)$ metric.sp，$\forall\cup$ open in X.
> 
> 

$\forall x \in \displaystyle\bigcup_{i \in I} U_i,\quad\exists j\in I,\quad x \in U_j$
由于 $U_j$ 是开集 $\exists \varepsilon > 0 ,B(x, \varepsilon) \subset U_j$ 
故 $B(x, \varepsilon) \subset \displaystyle\bigcup_{i \in I} U_i$
由 $x$ 的任意性，$\displaystyle\bigcup_{i \in I} U_i$ 是开集

---

> [!quote] LEM
>  $(X,d)$ 为度量空间，$x \in X$，$\varepsilon_1, \varepsilon_2 > 0$，且 $\varepsilon_1 < \varepsilon_2$，则$$B_{\varepsilon_1}(x) \subseteq B_{\varepsilon_2}(x)$$

取任意 $y \in B_{\varepsilon_1}(x)$，由开球定义
$$d(y,x) < \varepsilon_1$$
因为 $\varepsilon_1 < \varepsilon_2$，所以
$$d(y,x) < \varepsilon_1 < \varepsilon_2$$
因此 $d(y,x) < \varepsilon_2$，即 $y \in B_{\varepsilon_2}(x)$

由 $y$ 的任意性，
$$B_{\varepsilon_1}(x) \subseteq B_{\varepsilon_2}(x)$$
---

> [!warning] RMK
> 这里是包含而不是真包含的原因是，可能这两个球中间没有点。所以可能出现相等的情况。
> 
> 

> [!quote] THM
> $(X,d)$ metric.sp，fin $\cap$ open in X.
> 
> 

若 $\displaystyle\bigcap_{k=1}^n U_k = \varnothing$，则空集是开集（因为空集没有点，条件自动成立）
下设交集非空
$\forall x \in \displaystyle\bigcap_{k=1}^n U_k$，$x \in U_k, \forall k=1,\dots,n$ 
由于 $U_k$ 是开集 $\exists\varepsilon_k > 0,B(x, \varepsilon_k) \subset U_k$
取 $\varepsilon = \min\{\varepsilon_1, \varepsilon_2, \dots, \varepsilon_n\} > 0$
则 $B(x, \varepsilon) \subset B(x, \varepsilon_k) \subset U_k$ 对每个 $k$ 成立，  
因此 $B(x, \varepsilon) \subset \displaystyle\bigcap_{k=1}^n U_k$
由 $x$ 的任意性，$\displaystyle\bigcap_{k=1}^n U_k$ 是开集

---

## 1-6 度量空间中的内点
> [!NOTE] 内点(ipt)，内部(Int)，开集(open set)
> $(X,d)$ 是度量空间，$x\in M\subseteq X$
> $x$ 是 $M$ 的 **内点(ipt)** 若 $\exists \varepsilon>0,U_{\varepsilon}(x)\subseteq M$
> **内部(Int)** $\text{Int }M=\{x:x\text{ ipt of }M\}$

> [!quote] THM
> $M$ 是开集$\Leftrightarrow\text{Int }M=M$

> [!quote] THM
> $U\subseteq\mathbb{R}$ open $\Leftrightarrow U=\displaystyle\bigcup_{\text{at most countable}} (a_i,b_i) \quad(a_i\in\{-\infty\}\cup\mathbb{R},b_i\in\mathbb{R}\cup\{+\infty\},a_i\cap b_i=\varnothing)$

> [!quote] PROP
> $(X,d)$，其中 $d$ 为离散拓扑，则$\forall x,\{x\}$ open

take $\varepsilon =\displaystyle\frac{1}{2},U_{\varepsilon}(x)=\{x\}\subseteq \{x\}$，that is $\forall x,\{x\}$ open

---

> [!warning] RMK
> In $\mathbb{R}^n$，$\forall$ “reasonable“(合理的) set of strict ineq(严格大小于) def an open set.
>  for ex: $\{x\in\mathbb{R}^n:x_1>0\}$ or $\left\{(x,y):\begin{cases}2x>y\\ y^2+y>3x+2\end{cases}\right\}$ or $\cdots$ are open

> [!quote] PROP
> $X=\mathbb{R}^{n^2}(\simeq  Mat(n))$，$GL(n)=\{A\in Mat(n)|det(A)\neq 0\}$ open



## 1-7 度量空间中的闭集与极限点
> [!NOTE] 度量空间中的极限点/聚点（lpt）
> $X$ 度量空间，$M\subseteq X$
> $x\in X$(not necessary in $M$) **极限点/聚点（lpt）** of $M$ if $\forall\varepsilon>0,\check U_{\varepsilon}(x)\cap M\neq\varnothing$

contains a pt from $M\Leftrightarrow$ contains inf many pts from $M$

> [!NOTE] 度量空间中的孤立点（isolated pt），导集
> $X$ 度量空间，$M\subseteq X$
> $x\in M$ **孤立点（isolated pt）** if $\exists\varepsilon>0,U_{\varepsilon}(x)\cap M=\{x\}$
> 孤立点集称**导集**

> [!NOTE] 度量空间中的闭包（closure）
> $X$ 度量空间，$M\subseteq X$
> $\overline M=M\cup\{\text{all the lpts of }M\}$ **闭包（closure）** of $M$

> [!quote] PROP
> $X$ 度量空间，$M\subseteq X$
> $\overline M = M\iff M$ closed

> [!quote] THM
> $X$ 度量空间，$M\subseteq X$
> (1) $M$ open in $X\Rightarrow$ $M^{c}$ closed
> (2) $M$ closed in $X\Rightarrow$ $M^{c}$ open

> [!quote] EX
> by the thm, $\{ \det A = 0\}$ closed set $\iff$ $\{\det A \neq 0\}$ open

> [!quote] PROP
> $X$ 度量空间，$M\subseteq X$ closed $\iff$ $\forall y\in M^c,\exists\varepsilon>0,U_{\varepsilon}(y)\cap M=\varnothing$

> [!warning] RMK
> that is, $\forall$ pt $\notin M$ can be separated from $M$

度量空间一定是Hausdorff空间
## 1-8 度量拓扑

> [!NOTE] 度量拓扑(metric topology)
> $d$  是集合  $X$  的一个度量，则全体  $\varepsilon$ -球  $B(x, \varepsilon)$  的族（$x \in X,\varepsilon > 0$）是  $X$  的某一个拓扑的基，这个拓扑称为由度量  $d$  诱导出来的**度量拓扑(metric topology)**

对于任意  $\varepsilon > 0$  有  $x \in B(x, \varepsilon)$ ，所以基定义中的第一个条件显然满足
在验证基定义中的第二个条件之前，我们首先证明：若  $y$  是基元素  $B(x, \varepsilon)$  的一个点，则存在以  $y$  为中心的一个基元素  $B(y, \delta)$ ，它包含在  $B(x, \varepsilon)$  之中。取  $\delta$  为正数  $\varepsilon - d(x, y)$ ，则当  $z \in B(y, \delta)$  时， $d(y, z) < \varepsilon - d(x, y)$ ，由此得到
$$d (x, z) \leqslant d (x, y) + d (y, z) <   \varepsilon$$

从而证明了  $B(y,\delta)\subset B(x,\varepsilon)$  
<img src="73536d782745c5b1bd359d5b3ea32a8c822ee5e231d7ec7a77b576ee99911838.jpg" width = 150>
现在来验证基的第二个条件。设  $B_{1}$  和  $B_{2}$  为两个基元素，并且  $y \in B_{1} \cap B_{2}$ 。根据刚才的证明，可以取正数  $\delta_{1}$  和  $\delta_{2}$ ，使得  $B(y, \delta_{1}) \subset B_{1}$  和  $B(y, \delta_{2}) \subset B_{2}$ 。令  $\delta$  为  $\delta_{1}$  和  $\delta_{2}$  中较小的一个，便可见  $B(y, \delta) \subset B_{1} \cap B_{2}$ 

---
我们应用刚才证明的结论，将度量拓扑的定义重新改写成：集合  $U$  是由  $d$  诱导出来的度量拓扑中的开集，当且仅当对于每一个  $y \in U$ ，存在一个  $\delta > 0$  使得  $B_d(y, \delta) \subset U$ 
这个条件显然蕴涵  $U$  是开集，反之，若  $U$  是开集，它必定包含着包含点  $y$  的一个基元素  $B = B_{d}(x,\varepsilon)$  ，因此，  $B$  又包含着以  $y$  为中心的一个基元素  $B_{d}(y,\delta)$
> [!quote] EX 
> 离散度量诱导出来的拓扑是离散拓扑，例如基元素 $B(x,1)$ 就只包含着点 $x$

> [!quote] EX
> 度量 $d (x, y) = | x - y |$ 是 $\mathbb{R}$ 上的标准度量（容易验证 $d$ 是一个度量）。由它诱导出的拓扑与序拓扑相同。这是因为序拓扑中的每一个基元素都是度量拓扑中的一个基元素。事实上，$(a, b) = B (x, \varepsilon)$
> 其中  $x = \displaystyle\frac{a + b}{2}$  ，  $\varepsilon = \displaystyle\frac{b - a}{2}$  ，反之，每一个  $\varepsilon$  球  $B(x,\varepsilon)$  等于一个开区间  $(x - \varepsilon ,x + \varepsilon)$

> [! ] 可度量化(metricable) 空间
> $X$ 是一个拓扑空间。如果 $X$ 的拓扑是由集合 $X$ 的某一度量 $d$ 所诱导出来的，则称 $X$ 是一个**可度量化(metricable) 空间**

数学中许多重要的空间都是可度量化的，但也有一些不是。对于一个空间来说，可度量化往往是一个最理想的性质，因为度量的存在性为空间中一些定理的证明提供了一个重要工具。

因此，拓扑学中一个基本的也是重要的课题就是寻找保证拓扑空间可度量化的条件。我们在第4章中的目标之一，就是求出这样的条件，它便是著名的Urysohn度量化定理。更进一步的度量化定理在第6章讲述。本节只限于证明  $\mathbb{R}^n$  和  $\mathbb{R}^m$  是可度量化的。

虽然可度量化是拓扑学的一个重要课题，但是对于度量空间的研究，并不真正属于拓扑学，而更多的是属于分析学．一个空间是否是可度量化的，仅仅依赖于空间的拓扑．但与  $X$  的具体度量有关的一些性质一般并不是这样，所以它们不是拓扑性质．例如，我们可以在度量空间中给出下面的定义.

定义 设  $X$  是具有度量  $d$  的一个度量空间。 $X$  的子集  $A$  称为有界的，如果存在某数  $M$ ，使得对于  $A$  中任意两点  $a_1$  和  $a_2$  有

$$
d \left(a _ {1}, a _ {2}\right) \leqslant M.
$$

若  $A$  是有界的， $A$  的直径(diameter)定义为一个数

$$
\operatorname {d i a m} A = \sup  \left\{d \left(a _ {1}, a _ {2}\right) \mid a _ {1}, a _ {2} \in A \right\}.
$$

集合的有界性就不是一个拓扑性质，这是由于它仅依赖于  $X$  所采用的特定度量。例如，若  $X$  是具有度量  $d$  的一个度量空间，则存在一个度量  $\bar{d}$  诱导出的  $X$  的拓扑，使得对于  $\bar{d}$  而言， $X$  的每一个子集都是有界的。 $\bar{d}$  可以由以下定理给出。

定理20.1 设  $X$  是具有度量  $d$  的一个度量空间．则用

$$
\bar {d} (x, y) = \min  \{d (x, y), 1 \}
$$

所定义的  $\bar{d}$  ：  $X\times X\to \mathbb{R}$  是一个度量，并且  $\bar{d}$  和  $d$  诱导出的拓扑是  $X$  的同一个拓扑.

> [! ] 相应于 $d$ 的标准有界度量(standard bounded metric)
> 度量  $\bar{d}$  称为相应于 $d$ 的**标准有界度量(standard bounded metric)**

容易验证  $\bar{d}$  满足度量的前两个条件．下面验证三角不等式，即$$\bar {d} (x, z) \leqslant \bar {d} (x, y) + \bar {d} (y, z)$$若  $d(x, y) \geqslant 1$  或  $d(y, z) \geqslant 1$ ，则不等式右端至少为 1；而根据定义，其左边最多为 1，所以不等式成立。下面只考虑  $d(x, y) < 1$  且  $d(y, z) < 1$  的情形。这时$$d (x, z) \leqslant d (x, y) + d (y, z) = \bar {d} (x, y) + \bar {d} (y, z)$$根据定义， $\bar{d}(x, z) \leqslant d(x, z)$ ，所以对于  $\bar{d}$ ，三角不等式成立

注意在任何一个度量空间中，满足  $\varepsilon < 1$  的  $\varepsilon$ -球形成度量拓扑的一个基，这是由于含有  $x$  的每一基元素都包含一个这种在点  $x$  的  $\varepsilon$ -球。因为对于两种度量  $d$  和  $\bar{d}$  而言，满足  $\varepsilon < 1$  的  $\varepsilon$ -球的集合是同一个集合，从而这两种度量诱导出的是  $X$  上的同一个拓扑

---

我们想证欧氏度量和平方度量都诱导出  $\mathbb{R}^n$  上的通常拓扑．为此需要以下引理.

> [!quote] LEM
> $d$  和  $d'$  是集合  $X$  上的两个度量。  $\mathcal{T}$  和  $\mathcal{T}'$  分别是由它们诱导的拓扑，则  $\mathcal{T}'$  细于  $\mathcal{T}$  当且仅当对于每一个  $x \in X$  及每一个  $\varepsilon > 0$  ，存在一个  $\delta > 0$  ，使得$B _ {d ^ {\prime}} (x, \delta) \subset B _ {d} (x, \varepsilon)$

设  $\mathcal{T}'$  细于  $\mathcal{T}$ 。给定  $\mathcal{T}$  的一个基元素  $B_{d}(x, \varepsilon)$ ，根据引理13.3，存在拓扑  $\mathcal{T}'$  的一个基元素  $B'$ ，使得  $x \in B' \subset B_{d}(x, \varepsilon)$ ，于是存在一个以  $x$  为中心的球  $B_{d'}(x, \delta) \subset B'$ 。
反之，假定  $\varepsilon-\delta$  条件成立．对于  $\mathcal{T}$  中含有点  $x$  的一个基元素  $B$  ，可以求出  $B$  中以  $x$  为中心的一个球  $B_{d}(x,\epsilon)$  ，再根据已知条件，存在一个  $\delta$  ，使得  $B_{d^{\prime}}(x,\delta)\subset B_{d}(x,\varepsilon)$  ，于是根据引理13.3得到  $\mathcal{T}'$  细于  $\mathcal{T}$  

---

> [!quote] THM
> 由欧氏度量  $d$  及平方度量  $\rho$  所诱导的  $\mathbb{R}^n$  的拓扑与  $\mathbb{R}^n$  的积拓扑相同

设  $x = (x_{1}, \dots, x_{n})$  与  $y = (y_{1}, \dots, y_{n})$  是  $\mathbb{R}^{n}$  的两个点，可以通过简单的代数运算验证$$\rho (x, y) \leqslant d (x, y) \leqslant \sqrt {n} \rho (x, y)$$
上式中前一个不等式表明，$B _ {d} (x, \epsilon) \subset B _ {\rho} (x, \epsilon)$
对于所有的  $x$  和  $\varepsilon$  成立，这是因为若  $d(x, y) < \varepsilon$ ，则  $\rho(x, y) < \varepsilon$ 。类似地，后一个不等式表明，对于所有的  $x$  及  $\varepsilon$  有$B _ {\rho} (x, \varepsilon / \sqrt {n}) \subset B _ {d} (x, \varepsilon)$
根据上一个引理可见，这两个度量拓扑相同

现证积拓扑与由度量  $\rho$  所给出的拓扑是相同的
令$$B = \left(a _ {1}, b _ {1}\right) \times \dots \times \left(a _ {n}, b _ {n}\right)$$为积拓扑中的一个基元素，  $x = (x_{1},\dots ,x_{n})$  为  $B$  的一个元素．对于每一个  $_i$  ，存在一个  $\varepsilon_{i}$，$$\left(x _ {i} - \varepsilon_ {i}, x _ {i} + \varepsilon_ {i}\right) \subset \left(a _ {i}, b _ {i}\right)$$
选取  $\varepsilon = \min \{\varepsilon_1,\dots ,\varepsilon_n\}$  ，容易验证  $B_{\rho}(x,\epsilon)\subset B$  ，这就证明了  $\rho$  -拓扑细于积拓扑
反之，设  $B_{\rho}(x,\epsilon)$  是  $\rho$ -拓扑的一个基元素，给定元素  $y\in B_{\rho}(x,\epsilon)$  ，我们需要找出积拓扑的一个基元素  $B$  ，使 $y\in B \subset B _ {\rho} (x, \varepsilon)$
这是显然的．因为对于积拓扑而言，$$B _ {\rho} (x, \varepsilon) = (x _ {1} - \varepsilon , x _ {1} + \varepsilon) \times \dots \times (x _ {n} - \varepsilon , x _ {n} + \varepsilon)$$
本身就是一个基元素

---
现在我们来考虑无限笛卡儿积  $\mathbb{R}^{\omega}$  。人们自然会想到将度量  $d$  及度量  $\rho$  推广到这个空间。比如，我们尝试用$$d (\boldsymbol {x}, \boldsymbol {y}) = \left[ \sum_ {i = 1} ^ {\infty} \left(x _ {i} - y _ {i}\right) ^ {2} \right] ^ {1 / 2}$$
定义  $\mathbb{R}^{\omega}$  的一个度量  $d$ 。但是这一公式未必有意义，原因是级数不一定收敛。（然而，这个公式可以在  $\mathbb{R}^{\omega}$  的某一个重要子集上定义一个度量，见习题。）
类似地，人们也试图用
$$\rho (x, y) = \sup  \left\{\mid x _ {n} - y _ {n} \mid \right\}$$
将平方度量  $\rho$  推广到  $\mathbb{R}^{\omega}$  上．但是，这再度涉及到它未必有意义的问题．然而，若我们用  $\mathbb{R}$  中相应的有界度量  $\bar{d}(x, y) = \min \{|x - y|, 1\}$  来代替度量  $d(x, y) = |x - y|$ ，则定义有意义．由此引出的  $\mathbb{R}^{\omega}$  上的度量称为一致度量
> [! ] 一致度量（uniform metric），一致拓扑（uniform topology）
> 对于任意指标集  $J$  ，可按以下方式在一般的笛卡儿积  $\mathbb{R}^J$  上定义一致度量如下
> 给定指标集  $J$  以及  $\mathbb{R}^J$  中的点  $x = (x_{\alpha})_{\alpha \in J}$  和  $y= (y_{\alpha})_{\alpha \in J}$  ，定义  $\mathbb{R}^J$  的一个度量  $\bar{\rho}$  为
> $$\bar {\rho} (x, y) = \sup  \left\{\bar {d} \left(x _ {\alpha}, y _ {\alpha}\right) \mid \alpha \in J \right\}$$
> 其中  $\bar{d}$  是  $\mathbb{R}$  的标准有界度量， $\bar{\rho}$  称为  $\mathbb{R}^J$  上的**一致度量（uniform metric）**，由  $\bar{\rho}$  所诱导出来的拓扑称为**一致拓扑（uniform topology）**

一致拓扑与积拓扑和箱拓扑之间有以下关系：
> [!quote] THM
> $\mathbb{R}^J$  上的一致拓扑细于积拓扑，粗于箱拓扑。当  $J$  为无限集时，这三个拓扑两两不同

设给定一个点  $x = (x_{\alpha})_{\alpha \in J}$  和包含  $x$  的一个积拓扑基元素  $\displaystyle\prod U_{\alpha}$ . 令  $\alpha_{1}, \dots, \alpha_{n}$  是使  $U_{\alpha} \neq \mathbb{R}$  的那些指标. 对于每一个  $\alpha_{i}$ , 选取  $\varepsilon_{i} > 0$ , 使得以  $x_{\alpha_{i}}$  为中心关于度量  $\bar{d}$  的  $\varepsilon_{i}^{-}$ 球包含于  $U_{\alpha_{i}}$ . 由于  $U_{\alpha_{i}}$  在  $\mathbb{R}$  中是开的, 所以这样的  $\varepsilon_{i}^{-}$ 球是存在的. 令  $\varepsilon = \min \{\varepsilon_{1}, \dots, \varepsilon_{n}\}$ . 则有以  $x_{\alpha_{i}}$  为中心关于度量  $\rho$  的  $\varepsilon^{-}$ 球包含于  $\displaystyle\prod U_{\alpha}$ . 对于  $\mathbb{R}^{J}$  的一个点  $z$ , 若  $\bar{\rho}(x, z) < \varepsilon$ , 则对于所有  $\alpha, \bar{d}(x_{\alpha}, z_{\alpha}) < \varepsilon$ , 因此  $z \in \displaystyle\prod U_{\alpha}$ . 从而, 一致拓扑细于积拓扑
另一方面，令  $B$  为以  $x$  为中心关于度量  $\bar{\rho}$  的  $\varepsilon$ -球．这时， $x$ 在箱拓扑下的邻域$$U = \Pi \left(x _ {\alpha} - \frac {1}{2} \varepsilon , x _ {\alpha} + \frac {1}{2} \varepsilon\right)$$
包含于  $B$  ，这是因为，若  $y\in U$  ，则对于所有的  $\alpha$  有  $\bar{d} (x_{\alpha},y_{\alpha}) <   \frac{1}{2}\varepsilon$  ，因此  $\rho (x,y)\leqslant \frac{1}{2}\varepsilon$
当  $J$  是无限集时，这三个拓扑互不相同的证明我们留作习题

---
对于  $J$  为无限集的情形，我们还没能决定  $\mathbb{R}^j$  上的箱拓扑与积拓扑是否是可度量化的
事实上，我们将看到，只是在  $J$  是可数集并且取积拓扑的情况下，  $\mathbb{R}^j$  才是可度量化的
> [!quote] THM
> 设  $\bar{d}(a, b) = \min \{|a - b|, 1\}$  是  $\mathbb{R}$  上的标准有界度量。对于  $\mathbb{R}^n$  的两个点  $x, y$ ，定义
> $$D (x,y) = \sup  \left\{\frac {\bar {d} (x _ {i} , y _ {i})}{i} \right\}$$
> 那么  $D$  是诱导  $\mathbb{R}^n$  的积拓扑的一个度量

除了三角不等式外，度量的其他性质显然是满足的
以下证三角不等式，注意对于所有的  $i$  有$$\frac {\bar {d} \left(x _ {i} , z _ {i}\right)}{i} \leqslant \frac {\bar {d} \left(x _ {i} , y _ {i}\right)}{i} + \frac {\bar {d} \left(y _ {i} , z _ {i}\right)}{i} \leqslant D (x, y) + D (y, z)$$
因而$$\sup  \left\{\frac {\bar {d} (x _ {i} , z _ {i})}{i} \right\} \leqslant D (x, y) + D (y,z)$$令  $U$  为度量拓扑中的一个开集，  $x\in U$  ，在积拓扑中找一个开集 $V$ ，使得 $x\in V\subset U$  ，在  $U$  中选取一个  $\varepsilon$  -球  $B_{D}(x,\varepsilon)$  ，其次，可将  $N$  取得足够大，使得 $\displaystyle\frac{1}{N} <  \varepsilon$ ，最后，令 $V$ 是积拓扑的基元素$$V = \left(x _ {1} - \varepsilon , x _ {1} + \varepsilon\right) \times \dots \times \left(x _ {N} - \varepsilon , x _ {N} + \varepsilon\right) \times \mathbb {R} \times \mathbb {R} \times \dots$$我们来证明  $V \subset B_{D}(x,\varepsilon)$  ：对于 $\mathbb{R}^{\omega}$ 中的任意一点  $y$  以及  $i \geqslant N$
$$\frac {\bar {d} \left(x _ {i} , y _ {i}\right)}{i} \leqslant \frac {1}{N}$$
因此
$$D (x,y) \leqslant \max  \left\{\frac {\bar {d} \left(x _ {1} , y _ {1}\right)}{1}, \dots , \frac {\bar {d} \left(x _ {N} , y _ {N}\right)}{N}, \frac {1}{N} \right\}$$

如果  $y$  在  $V$  中，上面的式子小于  $\varepsilon$  ，于是  $V\subset B_{D}(x,\varepsilon)$  ，这便是所要证的
反之，考虑积拓扑的一个基元素$$U = \prod_ {i \in \mathbf {Z} _ {+}} U _ {i}$$
其中，当  $i = \alpha_{1},\dots ,\alpha_{n}$  时，  $U_{i}$  是  $\mathbb{R}$  中的开集．对于其他的指标  $i$  ，  $U_{i} = \mathbb{R}$  ，给定  $x\in U$  ，可以在度量拓扑中选取一个开集  $V$  ，使得  $x\in V\subset U$  ，在  $\mathbb{R}$  中选取一个以  $x_{i}$  为中心并且被  $U_{i}$  所包含的区间  $(x_{i} - \varepsilon_{i},x_{i} + \varepsilon_{i})$  ，其中，  $i = \alpha_{1},\dots ,\alpha_{n}$  ，要求  $\varepsilon_i\leqslant 1$ ，定义$$\varepsilon = \min  \left\{\varepsilon_ {i} / i \mid i = \alpha_ {1}, \dots , \alpha_ {n} \right\}$$我们证$$x\in B _ {D} (x, \varepsilon) \subset U$$事实上，设 $y$ 是 $B_{D}(x,\varepsilon)$ 的一个点，那么对于所有的 $i$$$\frac {\bar {d} \left(x _ {i} , y _ {i}\right)}{i} \leqslant D (x, y) <   \epsilon$$若 $i = \alpha_{1},\dots ,\alpha_{n}$  ，则  $\varepsilon \leqslant \displaystyle\frac{\varepsilon_{i}}{i}$  ，因此  $\bar{d} (x_i,y_i) <   \varepsilon_i\leqslant 1.$  由此推出  $|x_i - y_i| <  \varepsilon_i.$  因此，  $y\in \displaystyle\prod U_{i}$

---

## 练习
1. (a) 在  $\mathbb{R}^n$  中定义$$d ^ {\prime} (x, y) = \left| x _ {1} - y _ {1} \right| + \dots + \left| x _ {n} - y _ {n} \right|$$
证明  $d^{\prime}$  是诱导出  $\mathbb{R}^n$  的通常拓扑的一个度量．当  $n = 2$  时，画出  $d^{\prime}$  下的基元素.

(b) 更一般地，对于  $p \geqslant 1$  和  $\pmb{x}$ ， $\pmb{y} \in \mathbb{R}^n$ ，定义

$$
d ^ {\prime} (x, y) = \left[ \sum_ {i = 1} ^ {n} | x _ {i} - y _ {i} | ^ {p} \right] ^ {1 / p},
$$

假定  $d^{\prime}$  是一个度量．试证明它诱导出  $\mathbb{R}^n$  的通常拓扑.

2. 证明： $\mathbb{R} \times \mathbb{R}$  在字典序拓扑下是可度量化的。

3. 设  $X$  是以  $d$  为度量的一个度量空间

(a) 证明  $d: X \times X \to \mathbb{R}$  是连续的.

(b) 设  $X'$  是一个空间，作为集合与  $X$  相同。证明：若  $d: X' \times X' \to \mathbb{R}$  连续，则  $X'$  的拓扑细于  $X$  的拓扑。

可将这个习题中的结论总结为：若  $X$  有一度量  $d$ ，则  $d$  诱导的拓扑是使得函数  $d$  连续的所有拓扑中最粗的拓扑。

4. 考虑  $\mathbb{R}^n$  的积拓扑、一致拓扑和箱拓扑。

(a)哪些拓扑是使得以下从  $\mathbb{R}$  到  $\mathbb{R}^{\omega}$  的函数连续的拓扑？

$$
\begin{array}{l} f (t) = (t, 2 t, 3 t, \dots), \\ g (t) = (t, t, t, \dots), \\ h (t) = \left(t, \frac {1}{2} t, \frac {1}{3} t, \dots\right). \\ \end{array}
$$

(b)哪些拓扑是使得以下序列收敛的拓扑？

$$
\begin{array}{l} w _ {1} = (1, 1, 1, 1, \dots), \quad x _ {1} = (1, 1, 1, 1, \dots), \\ w _ {2} = (0, 2, 2, 2, \dots), \quad x _ {2} = \left(0, \frac {1}{2}, \frac {1}{2}, \frac {1}{2}, \dots\right), \\ w _ {3} = (0, 0, 3, 3, \dots), \quad x _ {3} = \left(0, 0, \frac {1}{3}, \frac {1}{3}, \dots\right), \\ \dots \dots \\ \mathbf {y} _ {1} = (1, 0, 0, 0, \dots), \quad \mathbf {z} _ {1} = (1, 1, 0, 0, \dots), \\ \mathbf {y} _ {2} = \left(\frac {1}{2}, \frac {1}{2}, 0, 0, \dots\right), \quad \mathbf {z} _ {2} = \left(\frac {1}{2}, \frac {1}{2}, 0, 0, \dots\right), \\ \mathbf {y} _ {3} = \left(\frac {1}{3}, \frac {1}{3}, \frac {1}{3}, 0, \dots\right), \quad \mathbf {z} _ {3} = \left(\frac {1}{3}, \frac {1}{3}, 0, 0, \dots\right), \\ \dots \dots \dots \\ \end{array}
$$

5. 设  $\mathbb{R}^{\infty}$  是由  $\mathbb{R}^{\omega}$  中所有终端为 0 的序列组成的子集。在一致拓扑下， $\mathbb{R}^{\infty}$  在  $\mathbb{R}^{\omega}$  中的闭包是什么？证明你的结论。

6. 设  $\bar{\rho}$  是  $\mathbb{R}^{\omega}$  的一致度量。给定  $x = (x_{1}, x_{2}, \dots) \in \mathbb{R}^{\omega}$  和  $0 < \varepsilon < 1$ ，令

$$
U (x, \varepsilon) = (x _ {1} - \varepsilon , x _ {1} + \varepsilon) \times \dots \times (x _ {n} - \varepsilon , x _ {n} + \varepsilon) \times \dots .
$$

(a) 证明  $U(x, \varepsilon)$  不等于  $\varepsilon$ -球  $B_{\bar{\rho}}(x, \varepsilon)$ .

(b) 证明  $U(x, \varepsilon)$  不是一致拓扑空间中的开集.

(c)证明

$$
B _ {\bar {p}} (x, \varepsilon) = \bigcup_ {\delta <   \varepsilon} U (x, \delta).
$$

7. 考虑第19节习题8中定义的映射  $h: \mathbb{R}^{\omega} \to \mathbb{R}^{\omega}$ . 并且赋予  $\mathbb{R}^{\omega}$  一致拓扑. 当  $a_{i}$  和  $b_{i}$  满足什么条件时,  $h$  连续? 什么条件会使得  $h$  为同胚?

8. 设  $X$  为  $\mathbb{R}^{\omega}$  中所有满足  $\sum x_{i}^{2}$  收敛的序列  $\pmb{x}$  所构成的子集．用公式

$$
d (x, y) = \left[ \sum_ {i = 1} ^ {\infty} \left(x _ {i} - y _ {i}\right) ^ {2} \right] ^ {1 / 2}
$$

定义  $X$  上的一个度量(见习题10).  $X$  分别由  $\mathbb{R}^n$  的箱拓扑、一致拓扑和积拓扑继承了三个拓扑. 用上式给出的度量  $d$  也定义了  $X$  的一个拓扑, 称之为  $\ell^2$ -拓扑.

(a)证明：对于  $X$  而言，以下包含关系成立：

箱拓扑  $\supset \ell^2$  - 拓扑  $\supset$  一致拓扑.

(b)所有终端为0的序列所构成的集合  $\mathbb{R}^{\infty}$  是  $X$  的子集．证明：作为  $X$  的子空间，  $\mathbb{R}^{\infty}$  所继承的四种拓扑互不相同.

(c) 集合

$$
H = \prod_ {n \in \mathbf {Z} _ {+}} [ 0, 1 / n ]
$$

是  $X$  的一个子集．称之为Hilbert立方(Hilbert cube).试比较  $H$  作为  $X$  的子空间所继承的四种拓扑.

9. 我们可以这样证明  $\mathbb{R}^n$  的欧氏度量  $d$  是一个度量：对于  $x, y \in \mathbb{R}^n$  和  $c \in \mathbb{R}$ ，定义

$$
\begin{array}{l} \boldsymbol {x} + \boldsymbol {y} = (x _ {1} + y _ {1}, \dots , x _ {n} + y _ {n}), \\ c x = \left(c x _ {1}, \dots , c x _ {n}\right), \\ \boldsymbol {x} \cdot \boldsymbol {y} = x _ {1} y _ {1} + \dots + x _ {n} y _ {n}. \\ \end{array}
$$

(a) 证明  $x \cdot (y + z) = (x \cdot y) + (x \cdot z)$ .  
(b) 证明  $|x \cdot y| \leqslant \| x \| \| y \|$ . [提示: 若  $x, y \neq 0$ , 令  $a = 1 / \| x \|$ ,  $b = 1 / \| y \|$ , 应用  $\| ax \pm by \| \geqslant 0$ .]  
(c) 证明  $\| x + y \| \leqslant \| x \| + \| y \|$ . [提示: 计算  $(x + y) \cdot (x + y)$ , 并应用(b)小题].  
(d)证明  $d$  是一个度量.

10. 设  $X$  为  $\mathbb{R}^{\omega}$  中所有使得  $\sum x_{i}^{2}$  收敛的序列  $(x_{1}, x_{2}, \cdots)$  所构成的集合。（这里我们要承认有关无穷数列的某些基本性质。倘若你对这些性质不熟悉，请参见下一节的习题11。）

(a) 证明：若  $x, y \in X$ ，则  $\sum |x_i y_i|$  收敛。[提示：应用习题9中(b)小题，证明部分和有界。]  
(b) 设  $c \in \mathbb{R}$ . 证明: 若  $\pmb{x}, \pmb{y} \in X$ , 则有  $\pmb{x} + \pmb{y} \in X$  和  $c\pmb{x} \in X$ .  
(c)证明

$$
d (\boldsymbol {x}, \boldsymbol {y}) = \left[ \sum_ {i = 1} ^ {\infty} (x _ {i} - y _ {i}) ^ {2} \right] ^ {1 / 2}
$$

是  $X$  上的一个度量.

*11. 证明：若  $d$  是  $X$  的一个度量，则

$$
d ^ {\prime} (x, y) = d (x, y) / (1 + d (x, y))
$$

是诱导  $X$  的拓扑的一个有界度量．[提示：对于  $x > 0$  ，设  $f(x) = x / (1 + x)$  ，应用中值定理证明  $f(a + b) - f(b) \leqslant f(a).]$

## 1-9 度量空间中的连续映射与等距映射

> [!NOTE] 度量空间中的连续映射
> $(X_1,d_1),(X_2,d_2)$ metric sp, $f:X_1\to X_2$ cont $\iff\forall$ 开集 $A\subseteq X_2$， $f^{-1}(A)$  是 $X_1$ 中的一个开子集

我们也熟知一种 $\varepsilon-\delta$ 定义。下面证这两个定义等价
> [! quote] THM
> $(X_1,d_1),(X_2,d_2)$ metric sp, $f:X_1\to X_2$ cont $\iff$ $$\forall x\in X_1,\forall\varepsilon>0,\exists \delta>0,\forall x'\in X_1,(d_1(x,x')<\delta\Rightarrow d_2(f(x),f'(x))<\varepsilon$$

> [!warning] RMK
> $f:X\to Y$ cont,bij $\Rightarrow\exists f^{-1}:Y\to X$ ($f$ no neccesary cont)
> 

> [!quote] EX
> $X=\{0\}\cup(1,2]$
> $Y=[0,1]$
> 
> $f:\begin{cases} 0\to 0\\ x\to x-1&x>0\end{cases}$  cont, bij
> $\Rightarrow\exists f^{-1}$ but not cont, since $\{0\}\subseteq X$ open($U_{\frac{1}{2}}(0)\subseteq X$) but $\{0\}\subseteq Y$ not open

> [!quote] EX
> $X=[0,1]$ with discrete metric
> $Y=[0,1]$ with standard metric
> $f:X\to Y,x\mapsto x$
> $\forall U\subseteq [0,1]=Y,f^{-1}(U)$ open in $X$ but not cont: $\displaystyle f^{-1}(\frac{1}{2})=\frac{1}{2}\in X, \frac{1}{2}$ open
> $\displaystyle(f^{-1})^{-1}(\frac{1}{2})$ not open in $[0,1]=Y$ 

> [!NOTE] 等距的(isometric)，等距映射(isometry)
> $(X,d),(Y,d')$ 是度量空间。$(X,d),(Y,d')$ are **等距的(isometric)** if $\exists f:X\to Y$ bij, $d(f(x),f(y))=d(x,y)$, in this case, $f$ is called an **等距映射(isometry)**

> [!quote] PROP
> $\forall$ isometry is a homeomorphism

> [!warning] RMK
> in metric sp, some homeomorphic is not isometry, some homeomorphic is not isometric

> [!quote] EX
> In $\mathbb{R}^2$, use Euclidean metric、norm,
> $D=\{(x,y):x^2+y^2=1\}$ homeomorphic to $S=\{(x,y):\max(|x|,|y|)=1\}$, but not isometric

> [!quote] EX
> $(0,1)\simeq \mathbb{R}$

> [!quote] PROP
> $X,Y,Z$ metric sp
> $f:X\to Y, g:Y\to Z$ cont $\Rightarrow g\circ f:X\to Z$ cont

> [!quote] PROP
> $X,Y,Z$ metric sp
> $f:X\to Y, g:Y\to Z$ homeomorphism $\Rightarrow g\circ f:X\to Z$ homeomorphism

> [!quote] PROP
> homeomorphism is an eq rel
## 1-10 度量拓扑续
这一节中，我们讨论度量拓扑与前面引进的一些概念之间的关系
正如我们所期望的那样，度量空间的子空间还是度量空间．如果  $A$  是拓扑空间  $X$  的一个子空间， $d$  是  $X$  上的一个度量，那么  $d$  在  $A \times A$  上的限制便是诱导  $A$  的拓扑的一个度量。证明留给读者完成。
我们不打算就序拓扑作进一步的讨论。易见有些序拓扑是可度量化的（如  $\mathbb{Z}_{+}$  与  $\mathbb{R}$ ），有些则不然。
每一个度量拓扑都满足Hausdorff公理．若  $x$  和  $y$  是度量空间  $(X,d)$  中不同的两点，令 $\varepsilon = \frac{1}{2} d(x,y)$  ，则由三角不等式可得  $B_{d}(x,\varepsilon)$  与  $B_{d}(y,\varepsilon)$  无交.
积拓扑的特殊情形已经研究过，证明了  $\mathbb{R}^n$  与  $\mathbb{R}^{\omega}$  是可度量化的。一般说来，可度量化空间的可数积是可度量化的。其证明仿照  $\mathbb{R}^{\omega}$  可度量化的证明进行，我们留作习题。
这里将对连续函数给予特别的关注。本节余下的部分将研究这个问题。
当我们考虑度量空间上的连续函数时，本书所进行的讨论很接近于微积分和分析学，有两件事情要做：
第一，希望将我们所熟知的连续性的“ $\varepsilon-\delta$  定义”推广到一般度量空间上，并且对连续性的“收敛序列定义”也做同样的工作
第二，除了在第18节中讨论过的那些构造连续函数的方法之外，还希望研究两种构造连续函数的方法。一个是取连续实值函数的和、差、积、商。另一个是取一致收敛的连续函数序列的极限
> [!quote] 定理
> 设  $f: X \to Y$ ， $X$  和  $Y$  是分别具有度量  $d_X$  和  $d_Y$  的可度量化空间，则  $f$ 连续 $\Leftrightarrow$ 对给定的  $x \in X$  和  $\varepsilon > 0$ ，存在  $\delta > 0$ ，使得
> $$d _ {X} (x, y) <   \delta \Longrightarrow d _ {Y} (f (x), f (y)) <   \varepsilon$$
> 

$\Rightarrow)$
设 $f$ 连续。给定 $x$ 和 $\varepsilon$ ，集合$f ^ {- 1} (B (f (x), \varepsilon))$ 是 $X$ 的含  的开集，从而它包含某一个以    为中心的  $\delta$ -球  $B(x, \delta)$ 。若  $y$  在这个 $\delta$-球中，则 $f(y)$ 在以 $f(x)$ 为中心的 $\varepsilon$-球中
$\Leftarrow)$
设  $\varepsilon-\delta$  条件满足，令  $V$  是  $Y$  的一个开集，我们证明  $f^{-1}(V)$  在  $X$  中是开的。设  $x$  是  $f^{-1}(V)$  的一个点。因为  $f(x) \in V$ ，所以存在一个以  $f(x)$  为中心的  $\varepsilon$ -球  $B(f(x), \varepsilon)$  包含于开集  $V$ 。根据  $\varepsilon-\delta$  条件，存在以  $x$  为中心的  $\delta$ -球  $B(x, \delta)$ ，使得  $f(B(x, \delta)) \subset B(f(x), \varepsilon)$ 。于是  $B(x, \delta)$  是包含于  $f^{-1}(V)$  的点  $x$  的一个邻域，因此  $f^{-1}(V)$  是一个开集

---
再看连续性的收敛序列定义．我们首先讨论收敛序列与集合的闭包间的关系．根据分析学中的经验，人们确信：若点  $x$  是  $X$  的子集  $A$  的闭包中的点，那么存在一个  $A$  的点的一个序列收敛到  $x$ 
一般而言，这是不对的，但在度量空间中这个结论成立
> [!quote] LEM(序列引理(sequence lemma))
> 设  $X$  是一个拓扑空间， $A \subset X$ 。若  $A$  中有一个收敛于  $x$  的序列，则  $x \in \overline{A}$ 。若  $X$  为可度量化空间，则逆命题也成立

设  $x_{n} \to x$ ，其中  $x_{n} \in A$ 。这时  $x$  的任意邻域都包含  $A$  的一个点，根据定理 17.5， $x \in \overline{A}$ 。反之，设  $X$  是可度量化的， $x \in \overline{A}$ 。令  $d$  为诱导出  $X$  的拓扑的一个度量。对于任意正整数  $n$ ，取以  $x$  为中心  $1/n$  为半径的邻域  $B_{d}\left(x, \frac{1}{n}\right)$ ，在它与  $A$  的交中选取点  $x_{n}$ 。我们证明序列  $x_{n}$  收敛于  $x$  ，这是因为任何包含  $x$  的开集  $U$  ，必定包含一个以  $x$  为中心的  $\varepsilon$ -球  $B_{d}(x, \varepsilon)$  ，如果取足够大的  $N$  ，使得  $\frac{1}{N} < \varepsilon$  ，那么对于所有  $i \geq N$  有  $x_{i}$  属于  $U$  

---
> [!quote] THM
> 设  $f: X \to Y$ . 若  $X$  为可度量化的空间, 则  $f$  连续的充分必要条件是对于  $X$  中每一个收敛序列  $x_{n} \to x$ , 序列  $f(x_{n})$  收敛于  $f(x)$ 

设  $f$  连续．给定  $x_{n} \to x$  ，我们证明  $f(x_{n}) \to f(x)$  ．令  $V$  是  $f(x)$  的一个邻域，则  $f^{-1}(V)$  是  $x$  的一个邻域．于是存在  $N$  ，使得对于  $n \geqslant N$  有  $x_{n} \in f^{-1}(V)$  ，因此对  $n \geqslant N$  ， $f(x_{n}) \in V$

我们证明充分性．设收敛序列的条件满足．若  $A$  是  $X$  的一个子集，下面证明  $f(\overline{A}) \subset \overline{f(A)}$ ．如果  $x \in \overline{A}$ ，则根据上一个引理可见：存在  $A$  中点的序列  $x_{n}$  收敛于  $x$ ．根据假设，序列  $f(x_{n})$  收敛于  $f(x)$ ．因为  $f(x_{n}) \in f(A)$ ，根据上一个引理可见  $f(x) \in \overline{f(A)}$ ．（注意，并不要求  $Y$  是可度量化的.）这就证明了  $f(\overline{A}) \subset \overline{f(A)}$

---
附带指出，在证明引理21.2和定理21.3时，并没有用到  $X$  是可度量化空间这么强的条件，而只要求在  $x$  处有球  $B_{d}(x, 1/n)$  的一个可数族．这启发我们引入以下定义

> [!NOTE] 可数基(countablebasis)，第一可数性公理(firstcountability axiom)
> 空间  $X$  称为在  $\pmb{x}$  处有**可数基(countablebasis)**，如果存在  $\pmb{x}$  的可数邻域族  $\{U_n\}_{n\in \mathbb{Z}_+}$  ，使得 $\pmb{x}$  的任意邻域  $\pmb{U}$  至少包含一个  $U_{n}$  ，如果空间  $X$  在每一点处有一个可数基，则称  $X$  满足**第一可数性公理(firstcountability axiom)**

若 $X$ 在 $x$ 处有一个可数基，则引理21.2的证明仍可完成．只要用集合$$B _ {n} = U _ {1} \cap U _ {2} \cap \dots \cap U _ {n}$$
代替球  $B_{d}\left(x,\displaystyle\frac{1}{n}\right)$  便可以了．定理21.3的证明也可以不加改变地完成
一个可度量化空间总满足第一可数性公理，我们将会看到其逆不真。为了证明有关空间的一些定理，就像Hausdorff公理那样，有时必须在拓扑空间上加上第一可数性公理。第4章将详细地讨论相关内容
现在研究构造连续函数的其他方法，这需要用到以下引理：
引理21.4加法、减法和乘法运算是从  $\mathbb{R}\times \mathbb{R}$  到  $\mathbb{R}$  中的连续函数，除法运算是从  $\mathbb{R}\times$ $(\mathbb{R} - \{0\})$  到  $\mathbb{R}$  中的连续函数
读者也许会发现这个引理在前面已经证明过了，就是标准的“ $\varepsilon-\delta$  论证”。你也可以在下面的习题12中找到证明的要点。因此，不难写出证明的细节

> [!quote] THM
> $X$  是一个拓扑空间， $f, g: X \to \mathbb{R}$  连续，则  $f + g$ 、 $f - g$ 、 $f \cdot g$  都是连续的。若对于所有  $x, g(x) \neq 0$ ，则  $f / g$  也是连续的

根据定理18.4， $h:X\to \mathbb{R}\times \mathbb{R}，h (x) = f (x) \times g (x)$ 连续
函数  $f + g$  是  $h$  和加法运算 $+: \mathbb {R} \times \mathbb {R} \longrightarrow \mathbb {R}$ 的复合，因而  $f + g$  连续
对于  $f - g$  、  $f\cdot g$  及  $f / g$  证明是类似的

---
> [!NOTE] 一致收敛(converges uniformly)
>  $f_{n}:X\to Y$  是一个从集合 $X$ 到度量空间 $Y$ 的函数的序列，  $d$ 是 $Y$ 中的度量．我们称序列  $(f_n)$  **一致收敛(converges uniformly)** 于函数  $f: X \to Y$ ，如果对于任意给定的  $\varepsilon > 0$ ，存在整数  $N$ ，对于  $n > N$  以及任意  $x \in X$  有
> $$d \left(f _ {n} (x), f (x)\right) <   \varepsilon$$
> 

收敛的一致性不仅依赖于  $Y$  的拓扑，也依赖于  $Y$  上的度量．我们有以下关于一致收敛序列的定理
> [!quote] THM(一致极限定理(uniform limit theorem))
> $f_{n}\colon X\to Y$  是从拓扑空间  $X$  到度量空间  $Y$  的连续函数的一个序列．若  $(f_n)$  一致收敛于  $f$  ，则  $f$  连续

设  $V$  是  $Y$  的一个开集， $x_0$  为  $f^{-1}(V)$  的一个点．我们要找出  $x_0$  的一个邻域  $U$ ，使得  $f(U) \subset V$
令  $y_0 = f(x_0)$  ，先取  $\pmb{\varepsilon}$  ，使得  $\pmb{\varepsilon}$  -球  $B(y_{0},\varepsilon)$  包含在  $V$  中，然后应用一致收敛性选取  $N$  ，使得对于所有  $n\geqslant N$  以及任意  $x\in X$  有
$$d \left(f _ {n} (x), f (x)\right) <   \frac{\varepsilon}{3}$$
最后再应用 $f_{N}$ 的连续性，取 $x_0$ 的一个邻域  $U$  ，使 $f_{N}$ 将 $U$ 映射到 $Y$ 的以  $f_{N}(x_{0})$  为中心的  $\displaystyle\frac{\varepsilon}{3}$  球内
下证明  $f$  将 $U$ 映到 $B(y_0, \varepsilon)$ 中，从而映射到  $V$  中，这便是我们所要证明的。为此，我们注意当  $x \in U$  时，有
$$\begin{array}{l} d (f (x), f _ {N} (x)) <\displaystyle\frac{\varepsilon}{3}\quad (\text {根 据} N \text {的 选 取}) \\ d \left(f _ {N} (x), f _ {N} \left(x _ {0}\right)\right)<\displaystyle\frac{\varepsilon}{3}\quad (\text {根 据} U \text {的 选 取}) \\ d (f _ {N} (x _ {0}), f (x _ {0}))<\displaystyle\frac{\varepsilon}{3}\quad (\text {根 据} N \text {的 选 取}) \\ \end{array}$$
把这三个式子相加，由三角不等式
$$d (f (x), f (x _ {0})) <   \varepsilon $$

---
> [!warning] RMK
> 一致收敛概念与一致度量的定义有关系。例如，考虑由全体函数  $f: X \to \mathbb{R}$  的集合连同其上一致度量  $\bar{\rho}$  所形成的空间  $\mathbb{R}^X$ 。不难看出，函数序列  $f_n: X \to \mathbb{R}$  一致收敛于  $f$  的充分必要条件是当把  $f_n$  看成度量空间  $(\mathbb{R}^X, \bar{\rho})$  的元素时，序列  $(f_n)$  收敛于  $f$ 。有关的证明留作习题

下面是一些不可度量化空间的例子
> [!quote] EX
> $\mathbb{R}^{\omega}$  在箱拓扑下是不可度量化的
> 我们将证明序列引理对  $\mathbb{R}^n$  不成立．设  $A$  为  $\mathbb{R}^n$  中所有坐标都是正数的点所组成的那个子集，即
> $$A = \{(x _ {1}, x _ {2}, \dots) \mid\forall i \in \mathbb {Z} _ {+}, x _ {i} > 0 \}$$
> 设  $\mathbf{0}$  是  $\mathbb{R}^n$  的“原点”，即零点  $(0, 0, \dots)$ ，它的每一个坐标都是 0。在箱拓扑中， $\mathbf{0} \in \overline{A}$ ，这是因为，如果$$B = \left(a _ {1}, b _ {1}\right) \times \left(a _ {2}, b _ {2}\right) \times \dots$$是含有 0 的任意一个基元素, 则  $B$  与  $A$  相交, 比如点$$\left(\frac {1}{2} b _ {1}, \frac {1}{2} b _ {2}, \dots\right)$$
> 就属于  $B \cap A$
> 但是，我们可以断定在  $A$  中没有收敛于  $\mathbf{0}$  的点的序列．对于  $A$  中的序列  $(a_{n})$  
> $$\boldsymbol {a} _ {n} = \left(x _ {1 n}, x _ {2 n}, \dots , x _ {i n}, \dots\right)$$
> 其中每一个坐标  $x_{m} > 0$  ，这就可以构造出  $\mathbb{R}$  的箱拓扑的基元素  $B^{\prime}$
> $$B ^ {\prime} = \left(- x _ {1 1}, x _ {1 1}\right) \times \left(- x _ {2 2}, x _ {2 2}\right) \times \dots$$
> $B^{\prime}$  含有原点  $\mathbf{0}$ ，却不包含序列  $(a_{n})$  的元素：这是因为  $a_{n}$  的第  $n$  个坐标  $x_{mn}$  不属于区间  $(-x_{nn}, x_{nn})$ 。所以点  $a_{n}$  不可能属于  $B^{\prime}$ 。因此在箱拓扑下，序列  $a_{n}$  不收敛于  $\mathbf{0}$ 

> [!quote] EX
> 不可数个  $\mathbb{R}$  的积空间是不可度量化的
> 设  $J$  为不可数指标集．我们来证明：  $\mathbb{R}^J$  在积拓扑下不满足序列引理
> 设  $A$  为  $\mathbb{R}^J$  的子集，其元素  $(x_{\alpha})$  满足：除了有限个  $\alpha$  之外，对其余所有的  $\alpha$  有  $x_{\alpha} = 1$ 。令  $\mathbf{0}$  为  $\mathbb{R}^J$  的“原点”，它的所有坐标都是0
> 可以论断  $\mathbf{0}$  属于  $A$  的闭包. 事实上, 令  $\Pi U_{\alpha}$  为含有  $\mathbf{0}$  的一个基元素, 那么仅对有限个  $\alpha$ , 比如说  $\alpha = \alpha_{1}, \dots, \alpha_{n}$ , 有  $U_{\alpha} \neq \mathbb{R}$ . 设  $(x_{\alpha})$  为  $A$  中一点, 对于  $\alpha = \alpha_{1}, \dots, \alpha_{n}$ , 取  $x_{\alpha} = 0$ . 对其余所有的  $\alpha$ , 取  $x_{\alpha} = 1$ . 那么  $(x_{\alpha}) \in A \cap \Pi U_{\alpha}$ , 这便证明了  $\mathbf{0} \in \overline{A}$ 
> 但是  $A$  中不存在收敛于  $\mathbf{0}$  的点的序列．我们对此证明如下：设  $(\pmb{a}_n)$  为  $A$  的点的一个序列. 给定  $n$  ，设  $J_{n}$  表示指标集  $J$  的子集，其元素  $\alpha \in J_{n}$  是使  $\pmb{a}_{n}$  的第  $\alpha$  个坐标异于1的指标．集合 $J_{n}$  的并是有限集的可数并，因而是可数的．但是  $J$  不可数，那么  $J$  中必有一个指标，比如说 $\beta$  ，使得它不在每一个  $J_{n}$  中．这就是说：对于每一个点  $\pmb{a}_{n}$  ，都有它的第  $\beta$  个坐标等于1
> 令  $U_{\beta}$  为  $\mathbb{R}$  中的开区间  $(-1, 1)$ ， $U$  为  $\mathbb{R}^J$  的一个开集  $\pi_{\beta}^{-1}(U_{\beta})$ 。那么  $U$  是  $\mathbf{0}$  的一个邻域，并且它不包含任何点  $a_n$ ，所以序列  $(a_n)$  不可能收敛于  $\mathbf{0}$

## 练习
> [!quote] Q
> 设  $A \subseteq X$ . 若  $d$  是  $X$  的拓扑的一个度量, 证明  $d \mid A \times A$  是  $A$  的子空间拓扑的一个度量

> [!quote] Q
> 设 $X$ 和 $Y$ 是分别具有度量 $d_X$ 和 $d_Y$ 的度量空间．对于 $X$ 中任意两点 $x_1$ 和 $x_2$ ， $f: X \to Y$  满足条件$$d _ {Y} \left(f \left(x _ {1}\right), f \left(x _ {2}\right)\right) = d _ {X} \left(x _ {1}, x _ {2}\right)$$
> 证 $f$  是一个嵌入 

> [!等距嵌入(isometric imbedding)]
> $f$  称为  $X$  到  $Y$  中的一个**等距嵌入(isometric imbedding)**

> [!quote] Q
> 设对于  $n \in \mathbb{Z}_+$ ,  $X_n$  是以  $d_n$  为度量的度量空间
> (a)证明$$\rho (x, y) = \max  \left\{d _ {1} \left(x _ {1}, y _ {1}\right), \dots , d _ {n} \left(x _ {n}, y _ {n}\right) \right\}$$
> 是积空间  $X_{1} \times \dots \times X_{n}$  上的一个度量
> (b) 设  $\bar{d}_i = \min \{d_i, 1\}$ . 证明$$D (x, y) = \sup  \left\{\bar {d} _ {i} \left(x _ {i}, y _ {i}\right) / i \right\}$$是积空间  $\Pi X_{i}$  上的一个度量

> [!quote] Q
> 证明  $\mathbb{R}_t$  和有序矩形都满足第一可数公理。（当然，这并不意味着它们是可度量化的）  

4. 定理 在空间  $\mathbb{R}$  中，设  $x_{n} \to x$  且  $y_{n} \to y$  ，则
$$
\begin{array}{l} x _ {n} + y _ {n} \rightarrow x + y \\ x _ {n} - y _ {n} \rightarrow x - y \\ x _ {n} y _ {n} \rightarrow x y \\ \end{array}
$$
并且如果每一个  $y_{n}\neq 0$  和  $y\neq 0$  则有
$$x _ {n} / y _ {n} \rightarrow x / y$$

提示：应用引理21.4．根据第19节中的习题可见：如果  $x_{n}\rightarrow x$  和  $y_{n}\rightarrow y$  ，则有  $x_{n}\times y_{n}\rightarrow$ $x\times y$

6.  $f_{n}\colon [0,1]\to \mathbb{R}$  定义为  $f_{n}(x) = x^{n}$  证明：对于每一个  $x\in [0,1]$  序列  $(f_n(x))$  收敛，但是序列  $(f_{n})$  不一致收敛.  
7. 设  $X$  是一个集合， $f_n: X \to \mathbb{R}$  是函数的一个序列。 $\bar{\rho}$  是空间  $\mathbb{R}^X$  上的一致度量。证明：序列  $(f_n)$  一致收敛于函数  $f: X \to \mathbb{R}$  当且仅当把  $f_n$  看成度量空间  $(\mathbb{R}^X, \bar{\rho})$  的元素时，序列  $(f_n)$  收敛于  $f$ 。  
8. 设  $X$  是一个拓扑空间， $Y$  是一个度量空间． $f_{n}$  ： $X \to Y$  是连续函数的一个序列， $x_{n}$  是  $X$  中收敛于  $x$  的一个点的序列．证明：若序列  $(f_{n})$  一致收敛于  $f$  ，则  $(f_{n}(x_{n}))$  收敛于  $f(x)$  
9. 设函数  $f_{n} \colon \mathbb{R} \rightarrow \mathbb{R}$  定义为
$$f _ {n} (x) = \frac {1}{n ^ {3} [ x - (1 / n) ] ^ {2} + 1}$$
参见图21.1.设  $f$  ：  $\mathbb{R}\to \mathbb{R}$  为零函数
(a)证明：对于任何  $x\in \mathbb{R}$  ，  $f_{n}(x)\rightarrow f(x)$  
(b)证明：  $f_{n}$  不一致收敛于  $f$  ．（这说明定理21.6的逆不成立，即，虽然  $f_{n}$  不一致收敛于  $f$  ，其极限函数  $f$  也可能连续）
10. 应用连续性的闭集式定义（定理18.1），证明下列集合是  $\mathbb{R}^2$  的闭子集
$$
\begin{array}{l} A = \{x \times y \mid x y = 1 \} \\ S ^ {1} = \{x \times y \mid x ^ {2} + y ^ {2} = 1 \} \\ B ^ {2} = \{x \times y \mid x ^ {2} + y ^ {2} \leqslant 1 \} \\ \end{array}
$$
集合  $B^2$  称为  $\mathbb{R}^2$  的（闭）单位球(unit ball)
11. 证明无穷级数的下列基本性质
(a) 若  $(s_n)$  是一个有界实数序列，并且对于任意  $n$  有  $s_n \leqslant s_{n+1}$ ，则  $(s_n)$  收敛.  
(b) 设  $(a_{n})$  是一个实数序列，
$$
s _ {n} = \sum_ {i = 1} ^ {n} a _ {i}
$$
证明若  $\sum a_{i}$  收敛于  $s$  ，  $\sum b_{i}$  收敛于  $t$  ，则  $\sum (ca_{i} + b_{i})$  收敛于  $cs + t$
![](0c8ed1462fed2926d538045bd3b8f4f9a78229fc4e3ec8211d9f863e500d9845.jpg)  
图21.1
(c) 证明无穷级数的比较判别法 (comparison test): 若对于每一个  $i$  有  $|a_i| \leqslant b_i$ , 并且级数  $\sum b_i$  收敛, 则级数  $\sum a_i$  收敛
提示: 证明级数  $\sum |a_i|$  与  $\sum c_i$  收敛, 其中  $c_i = |a_i| + a_i$
(d)给定一个函数序列  $f_{n}\colon X\to \mathbb{R}$  ，令$$s _ {n} (x) = \sum_ {i = 1} ^ {n} f _ {i} (x)$$
证明一致收敛性的 Weierstrass M-判别法(Weierstrass M-test)：若对于所有的  $x \in X$  和  $i$  有  $|f_i(x)| \leqslant M_i$ ，并且级数  $\sum M_i$  收敛，则序列  $(s_n)$  一致收敛于一个函数  $s$ 
提示：令  $r_n = \sum_{i=n+1}^{\infty} M_i$ 。证明：若  $k > n$ ，则  $|s_k(x) - s_n(x)| \leqslant r_n$ 。因此， $|s(x) - s_n(x)| \leqslant r_n$ 。
12. 证明  $\mathbb{R}$  中的代数运算的连续性如下：应用  $\mathbb{R}$  的度量  $d(a, b) = |a - b|$  和  $\mathbb{R}^2$  的度量$$\rho \left(\left(x, y\right), \left(x _ {0}, y _ {0}\right)\right) = \max  \left\{\mid x - x _ {0} \mid , \mid y - y _ {0} \mid \right\}$$
(a) 证明加法运算连续
提示: 任意给定  $\varepsilon$ , 令  $\delta = \varepsilon / 2$ , 并且注意$$d (x + y, x _ {0} + y _ {0}) \leqslant | x - x _ {0} | + | y - y _ {0} |$$
(b) 证明乘法运算连续
提示: 任意给定  $(x_0, y_0)$  及  $0 < \epsilon < 1$ , 令$$3 \delta = \varepsilon / (| x _ {0} | + | y _ {0} | + 1)$$
并且注意
$$d (x y, x _ {0} y _ {0}) \leqslant | x _ {0} | | y - y _ {0} | + | y _ {0} | | x - x _ {0} | + | x - x _ {0} | | y - y _ {0} |$$
(c) 证明取倒数运算是从  $\mathbb{R} - \{0\}$  到  $\mathbb{R}$  的连续映射
提示: 证明  $(a, b)$  的原像是开集. 就  $a$  和  $b$  为正、为负和为零考虑五种情况
(d) 证明减法运算和除法运算是连续的




# 第2节 拓扑空间
## 2-1 拓扑空间
拓扑空间的定义经历了很长时间才形成。看上去有些抽象，但当你用不同的方法构造拓扑空间时会对它有更好的理解
> [!拓扑(topology)、拓扑空间(topological space)]
> 集合  $X$ 上的一**拓扑(topology)** 是  $X$  的子集族  $\mathcal{T}$ ，满足
> 1. （空集全集在）$\varnothing、X\in\mathcal{T}$ 
> 2. （对任意并和有限交封闭）$\mathcal{T}$ 中任意元素的并、有限元素的交在$\mathcal{T}$中
> 一指定了拓扑 $\mathcal{T}$ 的集合 $X$ （即$(X,T)$）称一**拓扑空间(topological space)**
> （无歧义时可不提 $\mathcal{T}$ ，说 $X$ 上的一拓扑空间）

> [!warning] 除非特别说明，以下默认$(X,T)$为拓扑空间

> [!开集(open set)（拓扑空间中的元素）]
> $U\subseteq X$  是  $X$  中的 **开集(open set)** 若  $U\in\mathcal{T}$

> [!warning] 拓扑空间定义的开集表述
> 用开集的定义，可以说：
> 一集合  $X$  连同它的子集(称开集)的一族是拓扑空间，若
> 1. $\varnothing$ 和 $X$ 是开集
> 2. 开集的任意并、有限交是开集

> [!quote] EX
> $X = \{a, b, c\}$ ，以下是拓扑
> <img src="WechatIMG417 1.jpg" width="80" height="" alt="">
> （只有两个开集  $X$  和  $\varnothing$）
> <img src="images/c1009be3ac7800375a6878a22b72eb9686de440a38e82fdcd746b2eb39c09553.jpg" width=80 height="" alt="">
> <img src="images/fd13f2d2102645cdc9723d1ec068ab748ec1aa095599c6078ca0349ddbcf5b03.jpg" width="80" height="" alt="">
> <img src="images/aefa90c7ea8d7e717935bc14f2a810c79dd7d5ee28ce5a46cb8ae4efc1a520c8.jpg" width="80" height="" alt="">
> <img src="images/2a8b6b1870caaa8ac87ee613188e2c32dee4362231984d6eaad9fa826237d872.jpg" width="80" height="" alt="">
> <img src="images/9a48c9ea3e6facc4b5432bd5ef2f764146454152d97df799fc60655da5f820fb.jpg" width="80" height="" alt="">
> <img src="images/87b5a63d77bc554692e33e3d21fed0e3491f84fb1789f259ef899d936481f69b.jpgg" width="80" height="" alt="">（开集是  $X$ ， $\varnothing$ ， $\{a, b\}$ ， $\{b\}$  和  $\{b, c\}$）
> <img src="images/827cbc68d2718167bb066ba4aaa858075ac73c84820612cec6b162f7a033dcae.jpg" width="80" height="" alt="">
> <img src="images/491a186cf42b2a60cae576c9cf56fac19956caf4c469e82a4055689225a7bc68.jpg" width="80" height="" alt="">
> （开集是 $X$ 的所有子集）
> 下面不是一个拓扑
><img src="images/cff79412020694b2bf2a6f810e60de587a78e38ee543c86d3e792b2c6eee39fc.jpg" width="80" height="" alt="">
><img src="images/2a660b814742f8439ad5b6854c66a2b17b51fa01358a47f6fae88f77e53186fa.jpg" width="80" height="" alt="">

> [!quote] 离散拓扑的存在性
>   $X$  为任意的一个集合， $\mathcal{P}(X)$  是 $X$ 的一个拓扑

> [!离散拓扑（discrete topology）]
> $\mathcal{P}(X)$称**离散拓扑（discrete topology）**

> [!quote] 平庸拓扑的存在性
> $\{X,\varnothing\}$  是  $X$  的一个拓扑

> [!平庸拓扑（平凡拓扑）（trivial topology）（密着拓扑（indiscrete topology））]
> $\{X,\varnothing\}$ 称 **密着拓扑（indiscrete topology）** 或 **平庸拓扑（平凡拓扑）（trivial topology）**

## 练习
> [!quote] Q
>$X$ 是一个拓扑空间， $A$ 是 $X$ 的一个子集。假定对于每一个 $x \in A$，存在包含 $x$ 的一个开集 $U$，使得 $U \subset A$。证明  $A$  是  $X$  中的一个开集

> [!quote] Q
> 将2-1例中集合  $X = \{a, b, c\}$  的 9 个拓扑加以比较。即对于每两个拓扑，判定它们是否可以比较。如果可以比较，请指出哪一个较细

> [!quote] Q
> 证明第12节例4中给出的族  $\mathcal{T}_c$  是集合  $X$  的一个拓扑．族
> $$
> \mathcal {T} _ {\infty} = \{U \mid X - U \quad \text {或 为 无 限 集 ， 或 为 空 集 ， 或 为} X \}
> $$
> 是  $X$  上的一个拓扑吗？

> [!quote] Q
> (a) 设  $\{\mathcal{T}_{\alpha}\}$  是  $X$  的拓扑的一个族。证明  $\bigcap \mathcal{T}_{\alpha}$  是  $X$  上的一个拓扑。 $\bigcup \mathcal{T}_{\alpha}$  是  $X$  上的一个拓扑吗？
> (b) 设  $\{\mathcal{T}_{\alpha}\}$  是  $X$  的拓扑的一个族。证明  $X$  上存在包含所有  $\mathcal{T}_{\alpha}$  的唯一一个最小的拓扑，也存在包含于所有  $\mathcal{T}_{\alpha}$  的唯一一个最大的拓扑。
> (c) 设  $X = \{a, b, c\}$ , 令
> $$
> \mathcal {T} _ {1} = \{\emptyset , X, \{a \}, \{a, b \} \} \quad \text {和} \quad \mathcal {T} _ {2} = \{\emptyset , X, \{a \}, \{b, c \} \},
> $$
> 求出包含着  $\mathcal{T}_1$  和  $\mathcal{T}_2$  的最小拓扑，以及包含于  $\mathcal{T}_1$  和  $\mathcal{T}_2$  的最大拓扑
## 2-2 补拓扑与拓扑的比较

> [!quote] 有限补拓扑的存在性
>  $\mathcal{T}_f=\{U:(U=\varnothing)\lor (X-U\text{ fin})\}$是  $X$  上的一个拓扑

 - $X - X = \emptyset$  有限，且 $X - \emptyset = X\Rightarrow X、\emptyset\in\mathcal{T}_f$
 - 设集族 $\{U_\alpha\}\subseteq\mathcal{T}_f$，为了证明  $\bigcup U_\alpha$  在  $\mathcal{T}_f$  中，只要确定
$$X - \bigcup U _ {\alpha} = \cap (X - U _ {\alpha})$$
 由每一个集合  $X - U_{\alpha}$  有限，右边的集合是有限
- $U_{1}, \dots, U_{n}$  是  $\mathcal{T}_f$  的非空元素，为了证明  $\cap U_i$  在  $\mathcal{T}_f$  中，只要确定
$$
 X - \bigcap_ {i = 1} ^ {n} U _ {i} = \bigcup_ {i = 1} ^ {n} (X - U _ {i})
$$

因为上式右边是有限集的有限并，所以是有限集

--- 
> [!有限补拓扑(余有限拓扑)（finite complement topology）]
>  $\mathcal{T}_f$称**有限补拓扑（finite complement topology）**

> [!quote] 可数补拓扑的存在性
>  $\mathcal{T}_{\epsilon}=\{U:(U=\varnothing)\lor (X-U\text{ cou})\}$是  $X$  上的一个拓扑

> [!可数补拓扑(余可数拓扑)（countable complement topology）]
>  $\mathcal{T}_f$称**可数补拓扑（countable complement topology）**

> [!拓扑的粗、细、严格粗、严格细]
> $\mathcal{T}、\mathcal{T}'$  是集合  $X$  上两拓扑
 > - $\mathcal{T}'$  **细于 (finer)**  $\mathcal{T}$ 或 $\mathcal{T}$  **粗于 (coarser)**  $\mathcal{T}'$，若$$\mathcal{T}' \supseteq \mathcal{T}$$
 > - $\mathcal{T}'$  **严格细于 (strictly finer)**  $\mathcal{T}$ 或 $\mathcal{T}$  **严格粗于 (strictly coarser)**  $\mathcal{T}'$，若$$\mathcal{T}' \supsetneq \mathcal{T}$$
 > - $\mathcal{T}$  与  $\mathcal{T}'$  **可比较**，若  $$(\mathcal{T}' \supseteq \mathcal{T})\lor(\mathcal{T} \supseteq \mathcal{T}')$$ 

把拓扑空间 $X$ 想成石子堆，若干堆石子合在一起都是开集。现把石子敲成更小的碎块，那么开集族就变大了。因此拓扑空间就变细了
$X$  上的两个拓扑不一定可以比较（即偏序）。可参考上例

# 第3节 拓扑的基

## 3-1 拓扑的基

上节的每一个例子都是用开集族  $\mathcal{T}$  来刻画拓扑的，这样做一般显得不太方便。更多的时候是首先指定  $X$  的子集的一个较小的族，然后用它来确定拓扑
> [!拓扑的基，由基生成的拓扑]
> 集合 $X$ 的一子集族 $\mathcal{B}$ 称 $X$ 的某拓扑的一 **基(basis)** （基中元素称**基元素(basis element)**）若
> 1. ==（基元素覆盖）== $\forall x\in X,\exists$ $B\in\mathcal{B}$(基元素)$,x\in B$
> 2.  ==（两个覆盖可化为一个共同覆盖）== $B_{1}、B_{2}\in\mathcal{B}$(基元素)$,x\in B_{1}\cap B_{2} \Rightarrow\exists B_{3} \subseteq B_{1} \cap B_{2}$(基元素)$,x\in B_3$
> 此时这个拓扑称**由  $\mathcal{B}$  生成的拓扑  $\mathcal{T}$  (topology $\mathcal{T}$ generated by $\mathcal{B}$)**
> 即$\forall x \in U,\exists$ 基元素  $B \in \mathcal{B},x \in B\land B \subseteq U$ ，那么 $X$ 的子集 $U$ 称为 $X$ 的开集（即是 $\mathcal{T}$ 的一个元素）

> [!quote] 良定义性证明
> 由基 $\mathcal{B}$ 生成的族 $\mathcal{T}$ 是 $X$ 的一拓扑
<img src="images/26b879ee46c77e35d45c37253dd3e7ca02838b021fcb1cb31850d27a611972a9.jpg" width="280" height="" alt="">

 - ==（空集全集在）==若 $U=\varnothing$，显然满足开集的定义
	 $\forall x \in X,$ 由==（基元素覆盖）==，$\exists$ 包含  $x$  的某基元素 $B$ 且 $B \subseteq X$  ，故  $X\in\mathcal{T}$
 - ==（任意并封闭）==现取  $\mathcal{T}$  中元素的加标族  $\{U_{\alpha}\}_{\alpha \in J}$ ，下证任意并 $U = \displaystyle\bigcup_ {\alpha \in J} U _ {\alpha}\in\mathcal{T}$
	 $\forall x\in U$  ，$\exists$ 指标  $\alpha$  ， $x\in U_{\alpha}$
	由  $U_{\alpha}$  是开集，$\exists$ 基元素  $B,x\in B\subseteq U_{\alpha}$
	由  $x\in B、B\subseteq U$  ，由定义  $U$  为开集
	任取 $\mathcal{T}$ 的两元素  $U_{1}$  和  $U_{2}$ ，下证  $U_{1} \cap U_{2}$  属于  $\mathcal{T}$ 
	给定  $x \in U_{1} \cap U_{2}$ ，取包含  $x$  的基元素  $B_{1}$ ，使得  $B_{1} \subseteq U_{1}$ 
	再取包含  $x$  的基元素  $B_{2}$ 使  $B_{2} \subseteq U_{2}$ 
	根据基所满足的第二个条件，存在一包含  $x$  的基元素  $B_{3}$ ，使得  $B_{3} \subseteq B_{1} \cap B_{2}$ （参见图 13.3）
	故  $x \in B_{3}、B_{3} \subseteq U_{1} \cap U_{2}$ ，从而根据定义可见  $U_{1} \cap U_{2}$  属于  $\mathcal{T}$ 
 - ==（有限交封闭）==（归纳）下证 $\mathcal{T}$ 中元素的有限交 $U_{1} \cap \dots \cap U_{n}$ 在 $\mathcal{T}$ 中
	 $n = 1$  显然
	$n - 1\Rightarrow n$  
	因$\left(U _ {1} \cap \dots \cap U _ {n}\right) = \left(U _ {1} \cap \dots \cap U _ {n - 1}\right) \cap U _ {n},$由归纳假设， $U_{1} \cap \dots \cap U_{n-1}$  属于  $\mathcal{T}$ 
	应用刚才证明的结果， $U_{1} \cap \dots \cap U_{n-1}$  与  $U_{n}$  的交也属于  $\mathcal{T}$ 

---
> [!quote] EX
> <img src="images/6f302154f4920fee5f81d354dc70606a6451a081f5ff10b5e5a47f67fd8deb57.jpg" width="150" height="" alt="">
> 
> ![]() $\mathcal{B}$ 为平面上所有圆形域(开球，即圆的内部)所组成的族，则满足基的定义中的两个条件（第二个条件如图所示）
> 在由  生成的拓扑中，平面的一个子集 $U$ 是开集若对 $U$ 中任意 $x$ ，都有含于 $U$ 中的某一个包含 $x$ 的开球

> [!quote] EX
> <img src="images/c8c595faf49af2da15a01f33e0d0146fc8f72639e009a801bb8fca9137527aeb.jpg" width="150" height="" alt=""> 
> 
> $\mathcal{B}^{\prime}$ 为平面上所有矩形域(开盒，即矩形的内部)的族，其中矩形的边平行于两个坐标轴，则  $\mathcal{B}^{\prime}$  满足基的定义中的两个条件.第二个条件如图13.2所示．这个条件是显然满足的，这是由于任何两个基元素的交，其本身就是一个基元素(或者是空集).以后我们将会看到，在平面上由基  $\mathcal{B}^{\prime}$  生成的拓扑与例1中基  $\mathcal{B}$  生成的拓扑是一样的

> [!quote] EX
> 集合 $X$ 的所有单点子集的族是 $X$ 上离散拓扑的一个基
## 练习
> [!quote] Q
> 证明若  $\mathcal{A}$  是  $X$  的拓扑的一个基，则由  $\mathcal{A}$  生成的拓扑等于包含着  $\mathcal{A}$  的  $X$  的所有拓扑的交。若  $\mathcal{A}$  是一个子基，请证明同样的结论。

> [!quote] Q
> 证明 $\mathbb{R}_l$  的拓扑与  $\mathbb{R}_K$  的拓扑不可比较

> [!quote] Q
> 考虑  $\mathbb{R}$  的下列拓扑：
> $$
> \begin{array}{l} \mathcal {T} _ {1} = \text {标 准 拓 扑}, \\ \mathcal {T} _ {2} = \mathbb {R} _ {K} \text {的 拓 扑}, \\ \mathcal {T} _ {3} = \text {有 限 补 拓 扑}, \\ \mathcal {T} _ {4} = \text {上 限 拓 扑 ， 即 以 全 体 形 如} (a, b ] \text {的 集 合 为 基 的 拓 扑 ，} \\ \mathcal {T} _ {5} = \text {以 全 体 形 如} (- \infty , a) = \{x \mid x <   a \} \text {的 集 合 为 基 的 拓 扑}. \\ \end{array}
> $$
> 对于上述每一个拓扑，确定它包含着上述拓扑中哪些与它不同的拓扑

> [!quote] Q
> (a) 应用引理 13.2 证明可数族
> 
> $$
> \mathcal {B} = \{(a, b) \mid (a<b)\in\mathbb{Q}\}
> $$
> 
> 为生成  $\mathbb{R}$  的标准拓扑的一个基
> 
> (b)证明集族
> 
> $$
> \mathcal {C} = \{\left[ a, b\right) \mid (a<b)\in\mathbb{Q}\}
> $$
> 
> 为  $\mathbb{R}$  的某一个拓扑的基，并且所生成的拓扑与下限拓扑不同

## 3-2 拓扑基的性质

> [!quote] 引理 基生成拓扑的等价表述
> $\mathcal{B}$  是集合 $X$ 的拓扑 $\mathcal{T}$ 的一基，则 $\mathcal{T}$ 等于 $\mathcal{B}$ 中元素所有并的族

给定 $\mathcal{B}$ 中元素的一个族，这些 $\mathcal{B}$ 的元素也是 $\mathcal{T}$ 的元素
由于  $\mathcal{T}$  是一个拓扑，它们的并也在  $\mathcal{T}$  中
反之，给定 $U \in \mathcal{T},\forall x \in U$ ，取  $\mathcal{B}$  的一元素  $B_x$ ，使得 $x \in B_x \subset U$ 。从而 $U$ 等于 $\mathcal{B}$ 中元素的一个并

---
上述引理表明  $X$  中的每一开集 $U$ 都可以表示成某些基元素之并。然而 $U$ 这种表示不唯一。因而，拓扑学中“基”这个概念有别于它在代数学中的用法，在代数学中，将一个给定向量写成基向量的线性组合时其表达式是唯一的
我们已经用两种不同的方法描述了如何由基生成拓扑。有时要反过来做，即由一个拓扑找出生成它的基。下面介绍如何由给定的拓扑得到基的一种方法，以后要多次用到
> [!quote] 引理 基的判定
>$X$ 是一个拓扑空间。 $\mathcal{C}$ 是 $X$ 的开集的一个族，满足对于 $X$ 的每一个开集 $U$ 及每一个 $x \in U$ ，存在 $\mathcal{C}$ 的一个元素 $C$  ，使得 $x \in C \subset U$ 。那么 $\mathcal{C}$ 就是 $X$ 上这个拓扑的一个基

==1.== 对于  $x \in X$  ，因为  $X$  本身是开集，根据假设存在  $C \in \mathcal{C}$ ，使得  $x \in C \subset X$ 。
==2.== 设  $x \in C_1 \cap C_2$ ，其中  $C_1$  和  $C_2$  是  $\mathcal{C}$  的两个元素。因为  $C_1$  和  $C_2$  是开集，所以  $C_1 \cap C_2$  也是开集。于是根据假设，存在  $C_3 \in \mathcal{C}$ ，使得  $x \in C_3 \subset C_1 \cap C_2$ 。设  $\mathcal{T}'$  表示  $X$  的由  $\mathcal{C}$  所生成的拓扑， $\mathcal{T}$  为  $X$  的拓扑。上述引理表明  $\mathcal{T}'$  细于  $\mathcal{T}$ 。反之，因为  $\mathcal{C}$  的每一个元素都是  $\mathcal{T}$  的一个元素，所以  $\mathcal{C}$  的元素的任意并在  $\mathcal{T}$  中。于是根据==引理 基生成拓扑的等价表述==  $\mathcal{T}' \subset \mathcal{T}$ 。故  $\mathcal{T}' = \mathcal{T}$ 

---
当拓扑是由基给出的时候，就可以用基作为判定拓扑粗细的一个标准。下面就是这样的一个准则
> [!quote] LEM
> 设  $\mathcal{B}$  和  $\mathcal{B}'$  分别是  $X$  的拓扑  $\mathcal{T}$  和  $\mathcal{T}'$  的基。TFAE
> (1)  $\mathcal{T}'$  细于  $\mathcal{T}$  
> (2) $\forall x \in X$  及包含  $x$  的每一个基元素  $B \in \mathcal{B}$ , $\exists$基元素  $B' \in \mathcal{B}'$ ,  $x \in B' \subset B$

 $(2) \Rightarrow (1)$ 
 对于 $\mathcal{T}$ 的一个元素 $U$，下证 $U \in \mathcal{T}'$
  取  $x \in U$ ，因为  $\mathcal{B}$  生成  $\mathcal{T}$ ，则$\exists$元素  $B \in \mathcal{B}$ ，使得  $x \in B\subseteq U$ 。条件(2)告诉我们，$\exists$元素  $B' \in \mathcal{B}',x \in B'\subseteq B$ 。故  $x \in B' \subseteq U$ 。由定义  $U \in \mathcal{T}'$
$(1) \Rightarrow (2)$ 
给定  $x \in X$  和  $B \in \mathcal{B}$ , 其中  $x \in B$ . 根据定义,  $B \in \mathcal{T}$ , 再根据条件(1),  $\mathcal{T} \subseteq\mathcal{T}'$ . 因此  $B \in \mathcal{T}'$ . 因为  $\mathcal{B}'$  生成  $\mathcal{T}'$ , 所以存在一个元素  $B' \in \mathcal{B}'$ , 使得  $x \in B'\subseteq B$ 

---
> [!quote] EX
> 可以看出，平面上所有圆形域的族 $\mathcal{B}$ 与所有矩形域的族 $\mathcal{B}'$ 生成的是同一拓扑
> 在学习了度量空间之后，我们还将对这个例子更正式地加以讨论
>

## 3-3 拓扑的子基

下面我们来定义 $\mathbb{R}$ 上三种有趣的拓扑
> [! ] $\mathbb{R}$ 上的标准拓扑(standard topology)、$\mathbb{R}$ 上的下限拓扑(lower limit topology)、$\mathbb{R}$ 上的  $K$-拓扑(K-topology)
> - $\mathcal{B}$  为 $\mathbb{R}$ 上所有开区间$$(a, b) = \{x \mid a <   x <   b \}$$
> 的族．由  $\mathcal{B}$  生成的拓扑称为 **$\mathbb{R}$上的标准拓扑(standard topology)** 。 当我们考虑$\mathbb{R}$时，若无特别声明，我们将总假设考虑的是这个标准拓扑
> - $\mathcal{B}'$  为$\mathbb{R}$ 上所有半开区间
> $$
> [ a, b) = \{x \mid a \leqslant x <   b \}
> $$
> 的族，由  $\mathcal{B}'$  生成的拓扑称为  **$\mathbb{R}$  上的下限拓扑 (lower limit topology)**。具有下限拓扑的  $\mathbb{R}$  记作  $\mathbb{R}_l$ 
> - 对于  $n \in \mathbb{Z}_+$ ，令  $K$  表示所有形如  $\displaystyle\frac{1}{n}$  的数所组成的集合，令  $\mathcal{B}''$  是由所有开区间  $(a, b)$  及形如  $(a, b) - K$  形式的集合的族。由  $\mathcal{B}''$  所生成的拓扑称为  **$\mathbb{R}$  上的  $K$ -拓扑(K-topology)**.具有  $K$  -拓扑的  $\mathbb{R}$  记作  $\mathbb{R}_K$

易见，这三个集族都是基，在每一集族中的两个基元素的交或者是另一个基元素，或者是空集．这些拓扑间的关系如下：
> [!quote] LEM
> $\mathbb{R}_l$  和  $\mathbb{R}_K$  的拓扑都严格细于标准拓扑，但它们之间不可比较

以  $\mathcal{T}$ ,  $\mathcal{T}'$ ,  $\mathcal{T}''$  分别表示  $\mathbb{R}$ ,  $\mathbb{R}_{\ell}$ ,  $\mathbb{R}_K$  中的拓扑. 任意给定  $\mathcal{T}$  中的一个基元素  $(a, b)$  以及一个点  $x \in (a, b)$ ,  $\mathcal{T}'$  中的元素  $[x, b)$  包含着  $x$  并且包含于  $(a, b)$ . 另一方面, 任意给定  $\mathcal{T}'$  中的一个基元素  $[x, d)$ , 却不存在  $\mathcal{T}$  中的元素  $(a, b)$ , 使得它包含于  $[x, d)$  同时又包含着  $x$ . 因此  $\mathcal{T}'$  严格细于  $\mathcal{T}$
对  $\mathbb{R}_K$  进行类似的讨论．任意给定  $\mathcal{T}$  中的一个基元素  $(a,b)$  以及一个点  $x\in (a,b)$  ，则  $(a,b)$  是  $\mathcal{T}''$  中的一个基元素并且包含着  $x$  ，另一方面，任意给定  $\mathcal{T}''$  中的一个基元素  $B = (-1,1) - K$  以及  $B$  中一个点0，却不存在包含于  $B$  中并且包含着0的开区间
请读者自证  $\mathbb{R}_l$  的拓扑与  $\mathbb{R}_K$  的拓扑不可比较，放在练习中

---
这有一个问题。对由一个基  $\mathcal{B}$  生成的拓扑，可以描述成  $\mathcal{B}$  中元素任意并的族。那如果对一个给定的族，像取任意并那样取它们的有限交会得到些什么呢？这个问题引出拓扑的子基这个概念。
> [! ] 拓扑的子基(subbasis)、由子基生成的拓扑(topology generated by the subbasis  $\mathcal{S}$ )
> $X$ 的某拓扑的一个**子基(subbasis)**  $\mathcal{S}$  是  $X$  的子集的一个族，它的并等于  $X$ 
> **由子基  $\mathcal{S}$  生成的拓扑(topology generated by the subbasis  $\mathcal{S}$ ) ** $\mathcal{T}$  定义为  $\mathcal{S}$  中元素的有限交的所有并的族

> [!quote] THM
> 由子基  $\mathcal{S}$  生成的拓扑 $\mathcal{T}$  确实是一个拓扑

只需证 $s$ 中元素的所有有限交的族  $\mathcal{B}$  是一个基，再根据引理13.1可见  $\mathcal{B}$  中元素任意并的族  $\mathcal{T}$  是一个拓扑
给定  $x\in X$  ，它一定属于  $\mathcal{S}$  的一个元素，因而属于  $\mathcal{B}$  的一个元素，这就是基的第一个条件．下面验证第二个条件．设
$$
B _ {1} = S _ {1} \cap \dots \cap S _ {m} \quad \text {和} \quad B _ {2} = S _ {1} ^ {\prime} \cap \dots \cap S _ {n} ^ {\prime}
$$
为  $\mathcal{B}$  的两个元素，它们的交
$$
B _ {1} \cap B _ {2} = \left(S _ {1} \cap \dots \cap S _ {m}\right) \cap \left(S _ {1} ^ {\prime} \cap \dots \cap S _ {n} ^ {\prime}\right)
$$
仍是  $\mathcal{S}$  中元素的一个有限交，因而属于  $\mathcal{B}$

---

# 第4节 序拓扑
## 4-1 序拓扑

若  $X$  是全序集，可应用序关系在 $X$ 上定义一标准拓扑，称之为序拓扑
> [! ] 全序集的区间
> 设  $X$  是具有全序关系  $<$  的一个集合，给定  $X$  的两个元素$a < b$ ，由  $a$  和  $b$  所决定的区间
> $$\begin{array}{l} (a, b) = \{x \mid a <   x <   b \} \\ (a, b ] = \{x \mid a <   x \leqslant b \} \\ [ a, b) = \{x \mid a \leqslant x <   b \}\\ [ a, b ] = \{x \mid a \leqslant x \leqslant b \} \\ \end{array}$$
> 第一种类型的集合称为 $X$ 的**开区间(open interval)**，最后一种类型称为$X$ 的**闭区间(closed interval)** ，第二种、第三种类型的集合则称为  $X$  的**半开区间（half-open interval)**

> [! warning] RMK
>用“开”字，是暗示在赋予  $X$  某一个拓扑之后  $X$  中的开区间都是开集。其他术语的用意类此

> [!序拓扑 (order topology)]
>  $X$ 是全序集，其元素多于一个。设  $\mathcal{B}$  为下述类型所有集合的族：
> (1)  $X$  的所有开区间  $(a, b)$ 
> (2) 所有形如  $[a_0, b)$  的区间，其中  $a_0$  是  $X$  的最小元（如果存在）
> (3) 所有形如  $(a, b_0]$  的区间，其中  $b_0$  是  $X$  的最大元（如果存在）
> 则族  $\mathcal{B}$  是  $X$  的某一个拓扑的基。此拓扑称为**序拓扑 (order topology)**

> [!warning] RMK
> 如果  $X$  无最小元，那就没有第二种类型的集合，如果  $X$  没有最大元，那就没有第三种类型的集合

我们验证  $\mathcal{B}$  满足作为一个基所要满足的条件。先注意，对于 $X$ 的任意一个元素 $x$，它至少在  $\mathcal{B}$  的一个元素中；最小元(如果存在)在所有类型(2)的集合中，最大元(如果存在)在所有类型(3)的集合中，其他的元素则在类型(1)的集合中。其次注意，上述各类型中任意两集合之交，仍然是属于上述类型的一种，或者是一个空集。其他需要验证的情形留给读者完成。

> [!quote] EX
> 上一节定义的  $\mathbb{R}$  的标准拓扑，恰好就是由  $\mathbb{R}$  中的常用序关系给出的序拓扑

> [!quote]  EX
> 在字典序下研究集合  $\mathbb{R} \times \mathbb{R}$ , 其元素记作  $x \times y$  (这样是为了避开记号上的困难).  $\mathbb{R} \times \mathbb{R}$  既无最大元也无最小元, 于是  $\mathbb{R} \times \mathbb{R}$  上的序拓扑有一个以形如  $(a \times b, c \times d)$  (其中  $a < c$  或者  $a = c$ ,  $b < d$ ) 的所有开区间的族组成的基。可验证, 仅由第二种类型的区间组成的子族也是  $\mathbb{R} \times \mathbb{R}$  上序拓扑的一个基. 请读者自己验证
> <img src="30c0456d27f9b567a4dd42434615727212af076cfa539e813f93f256d06182cb.jpg" width=400> 

> [!quote]  EX
> 正整数集  $\mathbb{Z}_{+}$  是具有最小元的全序集． $\mathbb{Z}_{+}$  上的序拓扑是离散拓扑，因为它的每一个单点集是开集：若  $n > 1$  ，则单点集  $\{n\} = (n - 1, n + 1)$  是一个基元素．若  $n = 1$  ，则单点集  $\{1\} = [1, 2)$  也是一个基元素

> [!quote]  EX
> 具有最小元的全序集的另一个例子是在字典序下的集合  $X = \{1,2\} \times \mathbb{Z}_{+}$  ．用  $a_{n}$  记 $1\times n$  ，用  $b_{n}$  记  $2\times n$  ，则  $X$  可以表示成
> $$a _ {1}, a _ {2}, \dots$$
> $$b _ {1}, b _ {2}, \dots$$
> $X$  上的序拓扑不是离散拓扑．它的大部分单点集是开集，但是有一个例外，就是单点集  $\{b_{1}\}$  任何包含  $b_{1}$  的开集，必定包含着包含  $b_{1}$  的一个基元素(根据定义)，而包含  $b_{1}$  的任何一个基元素必含有序列  $a_{i}$  中的点.
## 4-2 射线

> [!全序集的射线]
>$X$  是全序集， $a$  是  $X$  的一个元素，由 $a$ 决定的**射线 (ray)**
> $$
> \begin{array}{l} (a, + \infty) = \{x \mid x > a \}\\ (- \infty , a) = \{x \mid x <   a \}\\ [ a, + \infty) = \{x \mid x \geqslant a \}\\ (- \infty , a ] = \{x \mid x \leqslant a \}\\ \end{array}
> $$
> 前两种类型的集合称为**开射线(open ray)**，后两种类型的集合称为**闭射线(closed ray)**

> [!warning] RMK
> 使用“开”这个词，是因为  $X$  中的开射线在序拓扑下是开集。其余情形类此
> 
> 如射线  $(a, +\infty)$  ．若  $X$  有最大元  $b_{0}$  ，则  $(a, +\infty)$  等于基元素  $(a, b_{0}]$  ．若  $X$  没有最大元，则  $(a, +\infty)$  等于所有形如  $(a, x)$  的基元素的并，其中  $x > a$ 。故不论在哪种情形下， $(a, +\infty)$  总是开集。对于射线  $(- \infty, a)$  来说也是如此

所有开射线组成 $X$ 上序拓扑的一个子基。事实上，由于开射线在序拓扑下是开集，所以由开射线所生成的拓扑含于序拓扑．另一方面，序拓扑中的每一基元素为有限个开射线之交
而  $(a,b)$  等于  $(-\infty ,b)$  与  $(a, + \infty)$  之交，同时  $[a_0,b)$  和  $(a,b_0]$  （如果存在的话）都是开射线．因此，由开射线所生成的拓扑也包含了序拓扑


# 第5节 二元积拓扑
## 5-1 二元积拓扑
有一个在笛卡儿积  $X \times Y$   ($X$ 和 $Y$ 是拓扑空间) 上定义拓扑的标准方法
> [!NOTE] $X \times Y$  上的积拓扑（二元积拓扑）
> 设  $X$  和  $Y$  是拓扑空间， $X \times Y$  上的**积拓扑(product topology)** 是以族  $\mathcal{B}$ :所有形如  $U \times V$($U,V$ 分别是 $X,Y$ 的开子集)  的集合的族为基的拓扑 

> [!quote] THM
>   $\mathcal{B}$  是一个基

第一个条件是显然的，这是由于 $X\times Y$ 本身就是一个基元素．第二个条件也是易于验证的．事实上，任意两个基元素  $U_{1}\times V_{1}$  与  $U_{2}\times V_{2}$  的交是$$\left(U _ {1} \times V _ {1}\right) \cap \left(U _ {2} \times V _ {2}\right) = \left(U _ {1} \cap U _ {2}\right) \times \left(V _ {1} \cap V _ {2}\right)$$由于  $U_{1} \cap U_{2}$  和  $V_{1} \cap V_{2}$  分别是  $X$  和  $Y$  的开集，所以上述集合是一个基元素
<img src ="85c3bbde093ea57eb5868a1a1dc10192835cd44b6fbbeafbe588e0f39eafdf53.jpg" width = 350>
值得注意的是：族  $\mathcal{B}$  不是  $X\times Y$  的一个拓扑．如图中两个矩形的并就不是两个集合的积，因而不属于  $\mathcal{B}$  ，但它是  $X\times Y$  中的开集

---
我们每次引进一个新概念，总是试图弄清它与前面引进的概念之间的关联。现问：当 $X$ 和 $Y$ 的拓扑是由它们的基给出时，积拓扑会产生什么性质呢？
> [!quote] THM
> 若  $\mathcal{B}$  是  $X$  的拓扑的一个基， $\mathcal{C}$  是  $Y$  的拓扑的一个基，则族
> $$
> \mathcal {D} = \{B \times C \mid B \in \mathcal {B} \text {并 且} C \in \mathcal {C} \}
> $$
> 是  $X \times Y$  的拓扑的一个基

我们应用引理 13.2. 给定  $X \times Y$  的一个开集  $W$  以及  $W$  的一个点  $x \times y$ . 根据积拓扑的定义, 存在一个基元素  $U \times V$ , 使得  $x \times y \in U \times V \subset W$ . 因为  $\mathcal{B}$  和  $\mathcal{C}$  分别是  $X$  和  $Y$  的基, 所以我们可以在  $\mathcal{B}$  中选取一个元素  $B$ , 使得  $x \in B \subset U$ , 也可以在  $\mathcal{C}$  中选取一个元素  $C$ , 使得  $y \in C \subset V$ . 于是  $x \times y \in B \times C \subset W$ . 从而族  $\mathcal{C}$  符合引理 13.2 的条件, 因此  $\mathcal{D}$  是  $X \times Y$  的一个基

---
> [!quote] EX
> 我们有  $\mathbb{R}$  的一个标准拓扑——序拓扑。这个拓扑与它自身的积称之为  $\mathbb{R} \times \mathbb{R} = \mathbb{R}^2$  上的标准拓扑。它有一个基是  $\mathbb{R}$  上所有开集的积的族，而刚才证明的定理告诉我们： $\mathbb{R}$  中所有开区间的积  $(a, b) \times (c, d)$  这个更小的族也可以作为  $\mathbb{R}^2$  的拓扑的一个基。每一个这样的积可以画成  $\mathbb{R}^2$  中一个矩形的内部。因此  $\mathbb{R}^2$  的标准拓扑正好是第 13 节例 2 中研究过的那一种
> 有时也需要用子基来表示积拓扑。为此，我们先定义某些叫做投射的函数。

## 5-2 投射

> [! ] 投射(projections)
> $\pi_1: X \times Y \to X，\pi_ {1} (x, y) = x$
> $\pi_2:X\times Y\to Y，\pi_ {2} (x, y) = y$
> 映射  $\pi_1$  和  $\pi_2$  分别称为  $X \times Y$  到它的第一因子和第二个因子上的**投射(projections)**

> [!warning] RMK
> 用“到……上”这个词是因为 $\pi_1$ 和 $\pi_2$ 都是满射（除去  $X$  和  $Y$  中有一个是空集的情形，因为这时  $X \times Y$  是空集，整个讨论就没有意义了）

设  $U$  是  $X$  的一个开子集，那么集合  $\pi_1^{-1}(U)$  恰好就是  $U \times Y$ ，它是  $X \times Y$  中的开集。同样地，若  $V$  是  $Y$  的一个开集，则$\pi_ {2} ^ {- 1} (V) = X \times V$也是  $X \times Y$  中的开集。这两个集合的交是  $U \times V$ 
<img src ="86284d991a1480c700d2f5346200de68711233c71dcfa9006b7294c2d75c4b19.jpg" width = 300>

这个事实引出下面的定理
> [!quote] THM
> 族
> $$
> \mathcal {S} = \left\{\pi_ {1} ^ {- 1} (U) \mid U \text {是} X \text {中 的 开 集} \right\} \cup \left\{\pi_ {2} ^ {- 1} (V) \mid V \text {是} Y \text {中 的 开 集} \right\}
> $$
> 是  $X \times Y$  的积拓扑的一个子基

用  $\mathcal{T}$  表示  $X \times Y$  的积拓扑，设  $\mathcal{T}'$  是由  $S$  生成的拓扑，因为  $S$  的每一个元素都属于  $\mathcal{T}$ ，所以  $S$  的元素的有限交的任意并也属于  $\mathcal{T}$ 。因此， $\mathcal{T}' \subset \mathcal{T}$ 。另一方面，拓扑  $\mathcal{T}$  的任意基元素  $U \times V$  是  $S$  中元素的有限交，这是因为$$U \times V = \pi_ {1} ^ {- 1} (U) \cap \pi_ {2} ^ {- 1} (V)$$所以  $U \times V$  属于  $\mathcal{T}'$ , 因此  $\mathcal{T} \subseteq \mathcal{T}'$ 

---


# 第6节 子空间拓扑
## 6-1 子空间拓扑

> [!quote] 命题 子空间拓扑是拓扑
> $(X,\mathcal{T})$ 是一拓扑空间， $Y\subseteq X\implies\mathcal {T} _ {Y} = \{Y \cap U \mid U \in \mathcal {T} \}$ 是  $Y$  的一个拓扑

==（空集全集在）== $\varnothing = Y \cap \varnothing , \quad Y = Y \cap X\implies\varnothing,Y\in\mathcal{T}_Y$  
==(有限交、任意并封闭)==
$$\begin{array}{l} \left(U _ {1} \cap Y\right) \cap \dots \cap \left(U _ {n} \cap Y\right) = \left(U _ {1} \cap \dots \cap U _ {n}\right) \cap Y \\ \displaystyle\bigcup_ {a \in J} (U _ {a} \cap Y) = (\bigcup_ {a \in J} U _ {a}) \cap Y \\ \end{array}$$

---
> [!NOTE] 子空间拓扑(subspace topology)
> $(X,\mathcal{T})$ 是一拓扑空间， $Y\subseteq X$，$\mathcal {T} _ {Y} = \{Y \cap U \mid U \in \mathcal {T} \}$ 称为**子空间拓扑(subspace topology)**
> 此时 $Y$  称 $X$ 的一个**拓扑子空间(subspace)**

> [!quote] 引理
> $\mathcal{B}$  是  $X$  的拓扑的一基$\implies\mathcal {B} _ {Y} = \{B \cap Y \mid B \in \mathcal {B} \}$ 是 $Y$ 上子空间拓扑的一基

$\forall U\in\mathcal{T},\quad y \in U \cap Y,\quad \exists B\in\mathcal{B},\quad y \in B \subseteq U \implies y \in B \cap Y \subseteq U \cap Y$ 

由==引理 基的判定==， $\mathcal{B}_Y$ 是 $Y$ 的子空间拓扑的一个基

---
> [!warning] 注
> $Y$ 中开集 $\neq X$ 中开集，故使用“开集”一词必须小心。究竟它指的是 $Y$ 的拓扑的一个元素，还是 $X$ 的拓扑的一个元素？

我们作出以下规定
> [!NOTE] $Y$ 中一开集（相对于  $Y$  而言的一开集），$X$ 中一开集（相对于  $X$  而言的一开集）
> 若  $Y$  是  $X$  的一拓扑子空间，集合 $U$ 
> - 属于 $Y$ 的拓扑，则称 $U$ 是 **$Y$ 中一开集（相对于  $Y$  而言的一开集）**
> - 属于 $X$ 的拓扑，则称 $U$ 是 $X$ **中一开集（相对于  $X$  而言的一开集）**

在一种特殊情况下， $Y$ 中的任何一个开集也是 $X$ 中的开集
> [!quote] 引理 子空间开集是原空间开集的条件
> $Y$ 是 $X$ 一拓扑子空间，若 $Y$ 是 $X$ 的一个开集，则
> $U$ 是 $Y$ 的一个开集$\implies U$ 是 $X$ 的一个开集

由 $U$ 是 $Y$ 的一个开集，$\exists X$ 的开集 $U_x,U = Y \cap U_x$
由 $Y$ 与 $U_x$ 都是 $X$ 的开集， $Y \cap U_x$ 也是 $X$ 的开集

---

## 练习
> [!quote] Q
> $Y$ 是 $X$ 的一个子空间并且 $A$ 是 $Y$ 的一个子集，证 $A$ 从 $Y$ 继承的子空间拓扑与 $A$ 从  $X$ 继承的子空间拓扑是同一个拓扑 

> [!quote] Q
> 若  $\mathcal{T}$  和  $\mathcal{T}'$  是  $X$  上的两个拓扑，并且  $\mathcal{T}'$  严格细于  $\mathcal{T}$ ，那么对于  $X$  的子集  $Y$  上的相应的子空间拓扑有些什么结论？  

> [!quote] Q
> 考虑作为  $\mathbb{R}$  子空间的集合  $Y = [-1, 1]$ ，下面集合中哪些是  $Y$  的开集？哪些是  $\mathbb{R}$  的开集？
> $$
> \begin{array}{l}A = \left\{x \mid \displaystyle\frac {1}{2} <   | x | <   1 \right\} \\ B = \left\{x \mid \displaystyle \frac {1}{2} <   | x | \leqslant 1 \right\}\\ C = \left\{x \mid \displaystyle \frac {1}{2} \leqslant | x | <   1 \right\}\\ D = \left\{x \mid \displaystyle \frac {1}{2} \leqslant | x | \leqslant 1 \right\}\\ E = \left\{x \mid 0 <   | x | <   1\land\displaystyle\frac{1}{x}\notin \mathrm {Z} _ {+} \right\}\end{array}
> $$

> [!quote] Q
> $f: X \to Y$  称为一个开映射(open map)，如果对于  $X$  的每一个开集  $U$ ，集合  $f(U)$  是  $Y$  中的一个开集。证明  $\pi_1: X \times Y \to X$  及  $\pi_2: X \times Y \to Y$  都是开映射

> [!quote] Q
> $X$  和  $X'$  分别表示具有拓扑  $\mathcal{T}$  和  $\mathcal{T}'$  的同一个集合。 $Y$  和  $Y'$  表示分别具有拓扑  $\mathcal{U}$  和  $\mathcal{U}'$  的同一个集合
> (a) 证明：若  $\mathcal{T}' \supset \mathcal{T}$  并且  $\mathcal{U}' \supset \mathcal{U}$ ，则  $X' \times Y'$  上的积拓扑细于  $X \times Y$  上的积拓扑
> (b)(a)的逆是否成立？验证你的结论

> [!quote] Q
> 证明可数族$$\{(a, b) \times (c, d) \mid (a <b, c <d)\land (a,b, c, d\in\mathbb{Q})\}$$是  $\mathbb{R}^2$  的一个基

> [!quote] Q
> $X$  为全序集．试问： $Y$  为  $X$  的一个凸子集，是否意味着  $Y$  是  $X$  的一个区间或射线？  

> [!quote] Q
> $L$  为平面上的一条直线，试描述  $L$  分别从  $\mathbb{R}_{\ell} \times \mathbb{R}$  和  $\mathbb{R}_{\ell} \times \mathbb{R}_{\ell}$  继承的子空间拓扑．这两种拓扑都是我们所熟悉的拓扑

> [!quote] Q
> 证明  $\mathbb{R} \times \mathbb{R}$  上的字典序拓扑与积拓扑  $\mathbb{R}_d \times \mathbb{R}$  是同一拓扑，这里  $\mathbb{R}_d$  表示  $\mathbb{R}$  上的离散拓扑，并将这个拓扑与  $\mathbb{R}^2$  上的标准拓扑进行比较 

> [!quote] Q
> $I = [0, 1]$ . 试比较  $I \times I$  的积拓扑,  $I \times I$  上的字典序拓扑,  $I \times I$  从  $\mathbb{R} \times \mathbb{R}$  的字典序拓扑继承而来的子空间拓扑

## 6-2 子空间拓扑与二元积拓扑
讨论子空间拓扑的二元积拓扑和序拓扑：有关积拓扑的相应结论与人们的期望相符，而关于序拓扑的相关结论则不然
> [!quote] 定理 拓扑子空间的二元积拓扑是二元积拓扑的子空间拓扑
> $X,Y$ 是拓扑空间，$A\subseteq X$， $B\subseteq Y$，则 $A \times B$ 的积拓扑是  $A \times B\subseteq X \times Y$ 上的子空间拓扑

设 $U_X\times U_Y$ 是 $X \times Y$ 的一个基元素，其中 $U_X$ 是 $X$ 一开集， $U_Y$ 是 $Y$ 的一个开集。于是  $(U_X\times U_Y) \cap (A \times B)$  是  $A \times B$  的子空间拓扑的一个基元素
集合论证过$$(U_X\times U_Y) \cap (A \times B) = (U_X \cap A) \times (U_Y \cap B)$$
由 $U_X \cap A$  和  $U_Y\cap B$  分别是 $A$ 和 $B$ 上子空间拓扑的开集，故 $(U_X \cap A) \times (U_Y \cap B)$  是 $A \times B$ 积拓扑的一基元素
基相同，两拓扑相同

---
> [!NOTE] $X \times Y$ 上的积拓扑继承的子空间拓扑
> $X,Y$ 是拓扑空间，$A\subseteq X$， $B\subseteq Y$，称 $A \times B\subseteq X \times Y$ 上的子空间拓扑为 **$X \times Y$ 上的积拓扑继承的子空间拓扑**
> 

> [!warning] 注
> 全序集 $X$ 具有序拓扑，$Y\subseteq X$ 将 $X$ 上的序关系限制在 $Y$ 上使 $Y$ 也为全序集
> 由此得到的  $Y$ 上的序拓扑与 $Y$ 从 $X$ 继承的子空间拓扑未必是同一拓扑

下面给出一个相同的例子和两个不同的例子
> [!quote] 例
> $Y = [0, 1]\subseteq\mathbb{R}$，取通常序关系
> 子空间拓扑的基是所有形如  $(a, b) \cap Y$  的集合所成的族：
> 
> $$
> (a, b) \cap Y = \begin{cases} (a, b) & a,b\in Y \\ [ 0, b) & a\notin Y,b\in Y \\ (a, 1 ] & a\in Y,b\notin Y\\ Y \text { or } \varnothing & a,b\notin Y \end{cases}
> $$
> z l这里面每个集合都是 $Y$ 的开集（但第二、三两种类型的集合不是空间  $\mathbb{R}$  的开集）
> 这些集合组成了 $Y$ 上序拓扑的一基，故这个例子中子空间拓扑(作为  $\mathbb{R}$  的一拓扑子空间)与序拓扑是一样的

> [!quote] EX
> $Y =[0,1)\cup\{2\}\subseteq\mathbb{R}$，取通常序关系
> 对 $Y$ 的子空间拓扑，$\{2\}$ 是开集，因为它是开集  $\left(\displaystyle\frac{3}{2},\frac{5}{2}\right)\cap Y$
> 但对 $Y$ 的序拓扑，$\{2\}$ 不是开集
> 对于  $Y$  序拓扑的任何包含 $2$ 的基元素，形如 $\{x \mid (x,a \in Y)\land (a <   x \leqslant 2) \}$ 必定包含  $Y$  中小于 $2$ 的点
> （后面我们学了连通性会知道，这说明：对序拓扑而言，$Y =[0,1)\cup\{2\}$ 是连通的）

> [!quote] EX
> $I = [0,1]$  ．由  $\mathbb{R}\times \mathbb{R}$  上字典序的限制得到  $I\times I$  上的字典序．然而  $I\times I$  上的序拓扑与它从  $\mathbb{R}\times \mathbb{R}$  上继承的子空间拓扑是不同的拓扑
> 如$\{\displaystyle\frac{1}{2}\} \times(\displaystyle\frac{1}{2},1]$是  $I\times I$  的子空间拓扑的开集，但不是序拓扑中的开集
> 子空间拓扑  <img src ="272e156e198d172aacdc3574c3e9cbeb2cd919d2e479a2a49b785903dec4c7ca.jpg" width = 100>序拓扑 <img src ="60bc584b52bb165e5ef32958120cc9aca886c41767919930c1cbc2883f8328a3.jpg" width = 100>

> [! ] 有序矩形(ordered square)
> 具有字典序拓扑的拓扑空间  $I \times I$  称为**有序矩形(ordered square)**，记作  $I_{o}^{2}$ 

对于全序集 $X$ 上的一个区间或一条射线而言，将不会出现上两例的“不正常情况”
> [!NOTE] 凸的(convex)(凸子集)，拓扑凸子空间，凸子空间拓扑
> $X$ 为全序集，称 $Y\subseteq X$  在 $X$ 中是**凸的(convex)** （$Y$ 为 $X$ 的一个**凸子集**）若 $\forall a,b\in Y,(a,b)\subseteq Y$
> 凸子集对应的拓扑子空间和子空间拓扑分别称为 **拓扑凸子空间** 和 **凸子空间拓扑**

> [!quote] 命题
> $X$ 中的区间和射线都是 $X$ 中的凸子集

> [!quote] 定理 拓扑凸子空间的序拓扑是序拓扑的凸子空间拓扑
> 全序集 $X$ 具有序拓扑，$Y$ 是 $X$ 的一凸子集，则 $Y$ 的序拓扑与限制 $X$ 的序拓扑在 $Y$ 上得到的子空间拓扑是同一拓扑
> 

==序拓扑包含了子空间拓扑==
设 $(a, +\infty)$ 是 $X$ 的一条射线，考虑它与 $Y$ 的交
若 $a \in Y$，则 $(a, + \infty) \cap Y = \{x \mid x \in Y\land x > a \}$ 为全序集  $Y$  中的一条开射线
若 $a \notin Y$，由于 $Y$ 是一凸子集，则 $a$ 是 $Y$ 的一下界或 $a$ 是 $Y$ 的一上界，故 $(a, +\infty) \cap Y$ 等于整个 $Y$ 或空集
故射线 $(a, +\infty)$ 与 $Y$ 的交为 $Y$ 中的一条开射线或 $Y$ 自身或空集
同理射线 $(-\infty, a)$ 与 $Y$ 的交为 $Y$ 中的一条开射线或 $Y$ 自身或空集
由于所有形如  $(a, +\infty) \cap Y$  和  $(-\infty, a) \cap Y$  的集合已构成了    的子空间拓扑的一个子基，并且它们中每一个都是序拓扑的开集，故序拓扑包含了子空间拓扑
==子空间拓扑包含了序拓扑==
注意  的每条开射线都是 $X$ 中一条开射线与 $Y$ 的交，因而它是 $Y$ 的子空间拓扑的开集。由于 $Y$ 的开射线构成了 $Y$ 的序拓扑的一个子基，故序拓扑包含于子空间拓扑

---
> [!NOTE] $X$ 的序拓扑继承的子空间拓扑
> 全序集 $X$ 具有序拓扑，$Y$ 是 $X$ 的一凸子集，称 $Y$ 的序拓扑与限制 $X$ 的序拓扑在 $Y$ 上得到的子空间拓扑为 **$X$ 的序拓扑继承的子空间拓扑**

> [!warning] 注
> 为避免混淆，我们作这样的约定：当讨论全序集 $X$ 的子集 $Y$ 时，除非有特别的说明，总设 $Y$ 取定的是子空间拓扑
# 第7节 闭集与极限点
## 7-1 闭集
我们已掌握少数几个拓扑空间的例子，以下我们着手引入一些与拓扑空间有关的基本概念。本节将讨论闭集、集合的闭包、极限点等概念，而这些又将导致我们去讨论拓扑空间中的一个公理，即Hausdorff公理
> [!NOTE] 闭集(closed set)
> 拓扑空间  $X$  的一个子集 $A$ 若满足 $X - A$  是开集，则称  $A$  为一个**闭集(closed set)**

> [!quote] 例
> $\mathbb{R}$  的子集  $[a,b]$  是一闭集，因为它的补 $\mathbb {R} - [a, b] = (-\infty,a)\cup(b,+\infty)$ 是一开集
>同理 $[a, +\infty)$ 是一闭集，因为它的补  $(-\infty ,a)$  是一开集
>这些事实正是我们使用“闭区间”、“闭射线”这类术语的原因
>$\mathbb{R}$ 的子集 $[a,b)$ 既不是开集又不是闭集

> [!quote] EX
> $\mathbb{R}^2$  上集合 $\{x \times y \mid x,y \geqslant 0 \}$ 是闭集，这是由于它的补是集合 $(- \infty , 0) \times \mathbb {R}$ 和 $\mathbb {R} \times (- \infty , 0)$ 的并，而其中每一个都是  $\mathbb{R}$  中两个开集的积，所以是  $\mathbb{R}^2$  中的一个开集

> [!quote] EX
> 对集合 $X$ 的有限补拓扑， $X$  自身及  $X$  的所有有限集构成  $X$  的闭集族

> [!quote] EX
> 对集合 $X$ 的离散拓扑，每一个集合都是开集，从而每一个集合也都是闭集

> [!quote] EX
> 考虑实直线上具有子空间拓扑的子集 $Y = [ 0, 1 ] \cup (2, 3)$
> 在这个空间中，由于$[0，1]$是  $\mathbb{R}$  中的开集  $\displaystyle\left(-\frac{1}{2},\frac{3}{2}\right)$  与  $Y$  的交，所以集合$[0,1]$是一个开集类似地，$(2,3)$作为  $Y$  的子集也是一个开集，同时，作为  $\mathbb{R}$  的子集也是开集．由于$[0,1]$及$(2,3)$在  $Y$  中互为补，因此$[0,1]$和($2,3)$作为  $Y$  的子集都是闭集

空间  $X$  的闭集族与开集族的性质十分类似
> [!quote] 命题
> $X$ 是一拓扑空间，则
> (1) $\varnothing$ 和 $X$ 是闭的
> (2) 闭集的任意交是闭的
> (3) 闭集的有限并是闭的

==(1) ==因为 $\varnothing$ 与 $X$ 的补分别是开集 $X$  与 $\varnothing$ , 所以 $\varnothing$ 与 $X$ 是闭集
==(2)(3)==应用DeMorgan律分别得到拓扑空间定义的==(3)(2)==

---
可以用满足本定理三条性质的集族(将其元素称之为“闭集”)替换开集族来刻画空间的拓扑，然后把开集定义成闭集的补，然后像之前一样建立一个体系。这个做法不会带来什么特别的方便，大多数数学家还是统一用开集来定义拓扑
当涉及子空间时，对于“闭集”这个词的使用就要小心。设 $Y$ 是 $X$ 的一个子空间，我们称 $A$ 是 $Y$ 中的闭集，是指 $A$ 是 $Y$ 的一个子集，并且 $A$ 是 $Y$ 的子空间拓扑中的闭集（$Y\backslash A$ 是 $Y$ 中的开集）
> [!quote] THM
>  $X$ 是拓扑空间，$Y\subseteq X$ 定义了子空间拓扑，则
> $$A\subseteq Y\text{ closed in }Y\iff\exists C\subseteq X,C\text{ closed in }X,A=Y\cap C$$

$\Leftarrow)$
由 $C$ 是 $X$ 的一个闭集，$X - C$ 是 $X$ 的一个开集
由子空间拓扑的定义，$(X - C) \cap Y$ 是 $Y$ 的一个开集
注意到 $(X - C) \cap Y = Y - A$ ，故 $Y - A$ 是 $Y$ 的一个开集，故 $A$ 是 $Y$ 的一个闭集
<img src="e752bbe5a4fb68b947d4e97abe867c3f006016a8e5a731edb3926d3416987237.jpg" width = 150>
$\Rightarrow)$
设$A$ 是 $Y$ 的一个闭集，则 $Y - A$ 是 $Y$ 的一个开集
根据定义 $Y - A$ 等于 $X$ 的一个开集 $U$ 与 $Y$ 的交。$X - U$ 是 $X$ 的一个闭集且  $A = Y \cap (X - U)$ ，因此 $A$ 等于 $X$ 的一个闭集与 $Y$ 的交
<img src="9a80a286f9823e8243e91ff3c1475394f958f833fd5d17281edbadf1c8b56a75.jpg" width = 150>

---

$A$ 是 $X$ 的子空间 $Y$ 的一个闭集，那它可能是 $X$ 的闭集，也可能不是
和开集一样，集合 $A$ 是否是 $X$ 的闭集也有一个判别准则，以下定理留给读者自己证明
> [!quote] THM
> $Y$ 是 $X$ 的一个子空间，若 $A$ 是 $Y$ 的一个闭集并且 $Y$ 是 $X$ 的一个闭集，则 $A$ 是 $X$ 的一个闭集

> [!NOTE] 内部 (interior)，闭包 (closure) 
> $X$ 是拓扑空间，$A\subseteq X$，
> $A$ 的 **内部 (interior)** 定义为包含于  $A$  的所有开集的并
> $A$  的 **闭包 (closure)** 定义为包含着  $A$  的所有闭集的交
> $A$  的内部记作  $\operatorname{Int} A$  或  $\dot{A}$ ， $A$  的闭包记作  $\operatorname{Cl} A$  或  $\overline{A}$ 

显然 $\dot{A}$  是开集， $\overline{A}$  是闭集。因此$\dot {A} \subseteq A \subseteq \overline{A}$
若  $A$  是一个开集，则  $A = \dot{A}$  ．若  $A$  是一个闭集，则  $A = \overline{A}$

集合的内部我们用得不多，但是集合的闭包却很重要
如果涉及 $X$ 和一子空间 $Y$，在取闭包时需十分小心
若 $A\subseteq Y$，则 $A$ 在 $Y$ 中的闭包与 $A$ 在 $X$ 中的闭包一般不同。此时我们仍用 $\overline{A}$ 表示 $A$ 在 $X$ 中的闭包，而 $A$ 在 $Y$ 中的闭包可以借助 $\overline{A}$ 给出：
> [!quote] 定理
> $Y$  是 $X$ 的一个子空间，$A\subseteq Y$， $\overline{A}$ 表示 $A$ 在 $X$ 中的闭包，则 $A$ 在 $Y$ 中的闭包 $B=\overline{A} \cap Y$ 

$\subseteq)$

$\bar{A}$  是  $X$  中的闭集, 根据定理17.2,  $\bar{A} \cap Y$  是  $Y$  的闭集. 因为  $\bar{A} \cap Y$  包含  $A$ , 并且根据定义,  $B$  等于  $Y$  中包含  $A$  的所有闭子集的交, 故 $B \subseteq (\bar{A} \cap Y)$

$\supseteq)$

设 $B$  是 $Y$ 的一个闭集，由定理17.2，存在 $X$ 中某闭集  $C$  ，使得  $B = C \cap Y$  则  $C$  是 $X$ 中包含 $A$ 的一个闭集。又因为 $\overline{A}$ 是所有这种闭集的交，所以 $\overline{A} \subseteq C$
故 $(\overline{A} \cap Y) \subseteq (C \cap Y) = B$

---

闭包定义本身并没有向我们提供求具体闭包的简单方法，因为 $X$ 的闭集族像开集族一样，太多了。下面一个定理给出了描述闭包的另一种方法，它仅用到 $X$ 的拓扑基，十分方便

> [!NOTE] 相交(intersect)，无交，无交并
> 集合 $A$ 与集合 $B$ **相交(intersect)**，是指交 $A\cap B$ 不是空集，反之称 **无交**
> 无交时的并集称 **无交并**，记作 $A\sqcup B$
> 

> [!quote] 定理
> $X$ 是拓扑空间，$A\subseteq X$，
> (a)  $x \in \overline{A}\iff$每一个包含 $x$ 的开集 $U$ 都与 $A$ 相交
> (b) $X$ 的拓扑由一个基给出，则  $x\in \overline{A}\iff$每一个包含 $x$ 的基元素 $B$ 都与 $A$ 相交

==(a)== 逆否命题证明：即证 $x \notin \overline{A} \Longleftrightarrow$ 存在一个包含 $x$ 的开集 $U$ 与 $A$ 无交
$\Rightarrow)$
若  $x \notin \overline{A}$ ，则 $x\in X\backslash\overline{A}$，故开集 $U = X\backslash\overline{A}$ 包含 $x$，但 $A\subseteq \overline A$，故 $U$ 与 $A$ 无交
$\Leftarrow)$
取 $x\in U$ 使得 $U\cap A=\varnothing$，则 $X\backslash U$ 是闭集，$x\notin X\backslash U$，$X\backslash U\subseteq A$，故 $\overline A\subseteq X\backslash U$ 且 $x\in\overline A$
==(b)== 
因为 $B$ 是开集，故若每一个包含 $x$ 的开集都与 $A$ 相交$\implies$每一个包含 $x$ 的基元素 $B$ 也与 $A$ 相交
若每一个包含 $x$ 的基元素都与 $A$ 相交，则 $A$ 包含一个含有 $x$ 的基元素，故每一个包含 $x$ 的开集 $U$ 与 $A$ 相交

---
> [!NOTE] 邻域（neighborhood）
>$U$ 是 $X$ 的一个**邻域(neighborhood)** 若 $U$  是包含  $x$  的一个开集

使用这个术语，上面定理的前半段就可写成
若 $A$ 是拓扑空间 $X$ 的一子集，则 $x \in \overline{A}\iff x$ 的每一个邻域与 $A$ 相交

有些数学家在不同意义上使用“邻域”一词。他们称  $A$  为  $x$  的一个邻域，仅仅指 $A$ 包含一个含 $x$ 的开集。我们不用这种说法
> [!QUOTE] 例
> $X=\mathbb{R}$，子空间  $Y = (0, 1]$，$A = \displaystyle\left(0, \frac{1}{2}\right)\subseteq Y$
> $A$ 在 $\mathbb{R}$ 中的闭包是  $\displaystyle\left[0, \frac{1}{2}\right]$ ，$A$ 在 $Y$ 中的闭包是  $\displaystyle\left[0, \frac{1}{2}\right] \cap Y = \left(0, \frac{1}{2}\right]$ 

## 练习
1. 设  $\mathcal{C}$  是集合  $X$  的子集的一个族．假定  $\varnothing$  与  $X$  在  $\mathcal{C}$  中，并且  $\mathcal{C}$  中元素的有限并及任意交也在 $\mathcal{C}$  中．证明集族  $\mathcal{T} = \{X - C \mid C \in \mathcal{C}\}$  是  $X$  的一个拓扑
2. 证明：若  $A$  是  $Y$  的闭集并且  $Y$  是  $X$  的闭集，则  $A$  是  $X$  的闭集.  
3. 证明：若  $A$  是  $X$  的闭集并且  $B$  是  $Y$  的闭集，则  $A \times B$  是  $X \times Y$  的闭集。  
4. 证明：若  $U$  是  $X$  的开集并且  $A$  是  $X$  的闭集，则  $U - A$  是  $X$  的开集，并且  $A - U$  是  $X$  的闭集。  
5. 设  $X$  是具有序拓扑的全序集．证明：  $(a,b)\subset [a,b]$  ，等号在什么条件下成立？  
6. 设  $A, B$  和  $A_{\alpha}$  都是空间  $X$  的子集．证明：

(a) 若  $A \subset B$ ，则  $\overline{A} \subset \overline{B}$ .  
(b)  $\overline{A\bigcup B} = \overline{A}\bigcup \overline{B}.$  
(c)  $\overline{\bigcup A_{\alpha}} \supset \bigcup \overline{A}_{\alpha}$ . 举出等号不成立的例子.

7. 评述以下对于  $\overline{\bigcup A_{\alpha}} \subset \bigcup \overline{A}_{\alpha}$  的证明：若  $\{A_{\alpha}\}$  是  $X$  中的集合的一个族， $x \in \overline{\bigcup A_{\alpha}}$ ，则  $x$  的任意邻域  $U$  与  $\bigcup A_{\alpha}$  相交，因此  $U$  必与某一个  $A_{\alpha}$  相交，所以  $x$  必定属于某一个  $A_{\alpha}$  的闭包。从而  $x \in \bigcup \overline{A}_{\alpha}$ 。

8. 设  $A, B$  和  $A_{\alpha}$  都是空间  $X$  的子集，判断下面哪些等号成立．如果等号不成立，判断哪一种包含关系(二或二)成立.

(a)  $\overline{A\cap B} = \overline{A}\cap \overline{B}.$  
(b)  $\overline{\bigcap A_{\alpha}} = \bigcap \overline{A}_{\alpha}$  
(c)  $\overline{A - B} = \overline{A} -\overline{B},$

9. 设  $A \subset X$  并且  $B \subset Y$ . 证明：在空间  $X \times Y$  中  $\overline{A \times B} = \overline{A} \times \overline{B}$ .

10. 证明：任何序拓扑都是Hausdorff的。  
11. 证明：两个Hausdorff空间的积是Hausdorff的。  
12. 证明：Hausdorff 空间的子空间是 Hausdorff 的。  
13. 证明： $X$  是一个Hausdorff空间当且仅当其对角线(diagonal)  $\Delta = \{x \times x \mid x \in X\}$  是  $X \times X$  中的一个闭集。  
14. 在  $\mathbb{R}$  的有限补拓扑空间中，序列  $x_{n} = \frac{1}{n}$  收敛到哪一点或哪些点？  
15. 证明  $T_{1}$  公理等价于： $X$  中的每两个不同的点各自有一个邻域不包含另一点。  
16. 考虑在第 13 节习题 7 中所给的  $\mathbb{R}$  的 5 个拓扑.

(a)对于每一个拓扑，确定集合  $K = \{1 / n\mid n\in \mathbb{Z}_{+}\}$  的闭包  
(b)其中的哪些拓扑满足Hausdorff公理，哪些满足  $T_{1}$  公理？

17. 考虑  $\mathbb{R}$  的下限拓扑及由第 13 节习题 8 中的基  $\mathcal{C}$  所给出的拓扑。对于上述两种拓扑确定区间  $A = (0, \sqrt{2})$  及  $B = (\sqrt{2}, 3)$  的闭包。  
18. 确定有序矩形中下列子集的闭包：

$$
A = \{(1 / n) \times 0 \mid n \in \mathbf {Z} _ {+} \},
$$

$$
B = \left\{(1 - 1 / n) \times \frac {1}{2} \mid n \in \mathbb {Z} _ {+} \right\},
$$

$$
C = \{x \times 0 \mid 0 <   x <   1 \},
$$

$$
D = \left\{x \times \frac {1}{2} \mid 0 <   x <   1 \right\},
$$

$$
E = \left\{\frac {1}{2} \times y \mid 0 <   y <   1 \right\}.
$$

19. 设  $A \subset X$ ,  $A$  的边界(boundary)定义为

$$
\mathrm {B d} A = \bar {A} \cap (\overline {{X - A}}).
$$

(a)证明：IntA与BdA无交，并且  $\overline{A} = \operatorname {Int}A\bigcup \operatorname {Bd}A.$  
(b) 证明:  $\mathrm{Bd}A = \varnothing \Longleftrightarrow A$  既开又闭.  
(c)证明：  $U$  是开集  $\Longleftrightarrow \mathrm{Bd}U = \overline{U} - U.$  
(d) 若  $U$  是开集，那么  $U = \operatorname{Int}(\bar{U})$  成立吗？验证你的结论.

20. 求出  $\mathbb{R}^2$  的下列子集的每一个的边界及内部：

(a)  $A = \{x\times y\mid y = 0\}$  
(b)  $B = \{x\times y\mid x > 0$  并且  $y\neq 0\}$  
(c)  $C = A\bigcup B$  
(d)  $D = \{x\times y\mid x$  是有理数}.  
(e)  $E = \{x \times y \mid 0 < x^2 - y^2 \leqslant 1\}$ .  
(f)  $F = \{x\times y\mid x\neq 0$  并且  $y\leqslant 1 / x\}$

*21. (Kuratowski) 考虑拓扑空间  $X$  的所有子集  $A$  的族。闭包运算  $A \to \overline{A}$  与取补运算  $A \to X - A$  是从这个族到它自身的两个函数。

(a)证明：逐次进行这两种运算，对于给定的集合  $A$  ，最多可以组成14个不同的集合.  
(b)对于具有通常拓扑的  $\mathbb{R}$  ，举出它的一个子集  $A$  ，由它恰好得到14个不同的集合.


## 7-2 极限点与极限

还有一种描述集合闭包的方法，它要用到我们下面将要讨论的极限点这样一个重要的概念
> [! ] 极限点（limit point）（聚点（cluster point，point of accumulation）），导集
> $X$ 是拓扑空间，$A\subseteq X$， $x\in X$，称 $x$ 为 $A$ 的一个**极限点（limit point）（聚点（cluster point，point of accumulation））** 若 $x$ 的任意邻域与 $A$ 的交含有异于 $x$ 的点
> 极限点的集合称为 **导集**，记作 $A'$

换言之 $x$ 是 $A$ 的一个极限点若 $x\in\overline{A\backslash\{x\}}$
$x$ 可以在 $A$ 中也可以不在 $A$ 中
> [!quote] 例
>  $X=\mathbb{R}$
>  - $A = (0,1]\implies\overline{A} = [0,1]$(事实上 $0$ 的每一个邻域都与 $A$ 相交，而 $[0,1]$ 以外的任意点都有不与 $A$ 相交的邻域)，$A'=[0,1]$
> - $B = \left\{\displaystyle\frac{1}{n} \mid n \in \mathbb{Z}_{+}\right\}\implies\overline{B} = \{0\} \cup B$，$B'=\{0\}$($\mathbb{R}$ 中除 $0$ 之外的任何点都有一邻域与 $B$ 无交或只交于 $x$)
> - $C = \{0\} \cup (1, 2)\implies\overline{C} = \{0\} \cup [1, 2]$，$C'=[1,2]$
> - $\overline{\mathbb{Q}} = \mathbb{R}$，$\mathbb{Q}' = \mathbb{R}$
> - $\overline{\mathbb{Z}}_{+} = \mathbb{Z}_{+}$，$\mathbb{Z}_{+} ' = \varnothing$
> - $\overline{\mathbb{R}}_{+}=\mathbb{R}_{+} \cup \{0\}$， $\mathbb{R}_{+}'=\mathbb{R}_{+} \cup \{0\}$ 

参照这些例子，可发现一个集合的闭包与导集之间的关系
> [!quote] 定理
> $A$ 是拓扑空间 $X$ 的一个子集，则$\bar {A} = A \cup A ^ {\prime}$

$\subseteq)$
$x \in A'$ 说明 $x$ 是 $A$ 的一个极限点，故任意 $x$ 的邻域都与 $A$ 交于不同于 $x$ 的一点，由前面的定理得 $x\in\overline{A}$，因此  $A' \subset \overline{A}$ 
由定义 $A \subset \overline{A}$，故 $A \cup A' \subset \overline{A}$ 
$\supseteq)$
任取 $x\in\overline{A}$，
若 $x\in A$，则 $x \in A \cup A'$
若 $x\notin A$，因为 $x \in \overline{A}$ ，那么 $x$ 的每一个邻域 $U$ 都与 $A$ 有交（设交集中一点 $y$），由 $x \notin A$ ，$x\neq y$，故 $x$ 是 $A$ 的极限点，即 $x \in A'$ 
故 $x \in A \cup A'$ 

---
> [!quote] 推论
> $A$ 是闭集$\iff$ $A=A'$

$A$ 是闭集 $\iff A = \overline{A}\iff A' \subseteq A$ 

---
> [!NOTE] 极限(limit)，收敛(converge)，发散(divergent)
> 对 $X$ 中的无穷序列 $\{x_n\}=(x_1,x_2,\cdots),x_i\in X, a\in X$ 称 $X$ 的 **极限(limit)** 若对于所有 $a\in U$，存在 $N\in\mathbb{N}$ 使得对任意 $n>N$，都有 $x_n\in U$，此时我们称这个序列 **收敛(converge) 于 $a$**，记作 $x_n\to a$ 或 $\lim x_n =a$，否则称 **发散(divergent)**

换句话说，一个序列收敛于 $a$ 若任意邻域都包含他的无穷多项
> [!quote] 例1
> $X$ 带有离散拓扑，其中的序列收敛于 $a$ 若他的尾巴恒为 $a$
> $x_n\to a\iff \exists N\in \mathbb{N},\forall n>N,x_n=a$

> [!quote] 例2
> $X=\mathbb{Q}$ 带有通常度量拓扑，$3.1,3.14,3.141,3.1415,3.14159,\cdots$ 不收敛！

> [!quote] 例3
> 下限拓扑 $\mathbb{R}_l$
> 一个序列在 $\mathbb{R}_l$ 中收敛$\iff$它在  $\mathbb{R}$ 中收敛+额外条件
> 在 $\mathbb{R}_l$ 中，$\displaystyle\frac{(-1)^n}{n}$ 不收敛于 $0$，这表明 $0\in[0,1)$ 不满足极限的条件
> 
> $\mathcal{T}'$ 比 $\mathcal{T}$ 细$\iff\forall x\in B\in\mathcal{B},\exists x\in B'\subseteq B$
> $x_n$ 在 $\mathcal{T}'$ 中收敛$\implies x_n$ 在 $\mathcal{T}$ 中收敛
> 我们取 $\mathcal{T}'=\mathbb{R}_l$，$\mathcal{T}=\mathbb{R}$
> $x_n$ 在 $\mathcal{T}'$ 中收敛$\implies x_n$ 在 $\mathcal{T}$ 中收敛
> 
> 问：为什么这个推断是正确的？
> 
> 若 $\mathbb{R}$ 更细$\implies\forall x\in [a,b)\in\mathcal{B},\exists x\in (a',b')\subseteq [a,b)$，这是不对的，如果 $x=a$
> 故 $\mathbb{R}$ 不比 $\mathbb{R}_l$ 细
> 反之，$\forall x\in (a,b)\in\mathcal{B},\exists x\in [x,b')\subseteq (a,b)$
> 这说明 $\mathcal{T}'$ 比 $\mathcal{T}$ 细
> 

> [!quote] 例4
> $X=\mathbb{N},U_m=\{0,\cdots,m\},\mathcal{J}=\{U_m:m\in\mathbb{N}\}\cap\{\varnothing,\mathbb{N}\}$
> $x_n\to a\iff \forall U_m,m\ge a,\exists N\in\mathbb{N},\forall n>N,x_n\in U_m$
> 等价：$x_n\le a$ 对无穷多个 $n$
> $\iff a$ 是 $x_n$ 的上界
> 收敛 $\iff$ 有界
> 若 $x_n\to a$，则 $x_n\to b\forall b\ge a$
> 我们发现极限不唯一（而且有无穷多个）！

> [!quote] 例4
> $\mathbb{R}$ 带有有限补拓扑
> 若 $\exists N,\forall n>N,x_n =a$，则 $x_n\to a$
> $b\in U=\mathbb{R}\backslash a$，$U$ 包含有限项，$b$ 不是极限
> $x_n=(-1)^n$ 不收敛
> $\forall a,\exists U\ge a,\{\pm 1\}\nsubseteq U$
> 若 $x_n =a$ 对无穷多项 $n$，$x_n=b$，故 $x_n$ 不收敛
> $x_n=\displaystyle\frac{(-1)^n}{n}\to a\forall a\in\mathbb{R}$
> 1. 若 $\exists N,\forall n>N,x_n =a$，则 $x_n\to a$
> 2. 若 $x_n$ 无穷次，则不存在极限
> 3. 若 $x_n$ 有限次，则 $x_n$ 收敛于 $\forall a\in \mathbb{R}$
>
> 即如果序列最终恒等于 $a$，则只收敛于 $a$
>   - 如果序列的值集合是无限的，则收敛于 every $a \in \mathbb{R}$
>   - 如果序列的值集合有限但不最终恒定，则不收敛于任何点

在研究更为一般的拓扑空间的时候，如果仅凭有关 $\mathbb{R}$ 和 $\mathbb{R}^2$ 上的开集、闭集、极限点的经验，就会出现错误
在 $\mathbb{R}$ 和 $\mathbb{R}^2$ 中，每一个单点集  $\{x_0\}$  都是闭集。这个事实是容易证明的，事实上，每一个异于  $x_0$  的点都有一个邻域不与  $\{x_0\}$  相交。因此  $\{x_0\}$  的闭包就是  $\{x_0\}$ 。但是这一点对于任意拓扑空间却不成立。如如下图所示拓扑空间 $\{a, b, c\}$ 的拓扑
 单点集  $\{b\}$  不是闭集，因为它的补不是开集
<img src="555ee59a8df8f5089aa1d2d955cbc94e3440bb8d17d94b8c522c583528ba2b75.jpg" width =150>
处理更为一般的拓扑空间时，如果仅凭有关 $\mathbb{R}$ 和 $\mathbb{R}^2$ 中收敛序列的经验，也可能会导致错误：一个序列可能收敛到多个点！比如例2，还有刚才的拓扑空间中，序列 $x_{n} = b$ 不仅收敛到点 $b$ ，它也收敛到点 $a$ 和 $c$

## 7-3 Hausdorff空间
单点集不是闭集的拓扑、使一个序列可收敛到多点的拓扑，被许多数学家认为是不正常的拓扑。这些并不能引起数学家们多大的兴趣，因为它们在数学的其他分支中很少出现。如果这种例子被容许的话，那对于拓扑空间能够证明的定理就是很有限的。因此常常需要一些附加条件，使得上述例子相应的情况不会出现，从而使我们所讨论的空间更接近几何直观。这个条件是数学家Felix Hausdorff给出的
> [!NOTE]  $T_{2}$  公理（  $T_{2}$  axiom）
> **$T_{2}$  公理($T_{2}$  axiom)**：任两不同的点  $x_{1}$  和  $x_{2}$ , 分别存在  $x_{1}$  和  $x_{2}$  的无交邻域  $U_{1}$  和  $U_{2}$ 

> [! ] Hausdorff空间/T2空间/ $T_2$ 空间(Hausdorff space)
> 满足 $T_{2}$ 公理的拓扑空间 $X$ 称一个 **Hausdorff空间/T2空间/ $T_2$ 空间(Hausdorff space)**

> [!quote] 命题
> 拓扑空间 $X$ 是度量空间则是Hausdorff空间

令 $d=d(x,y)$，则 $U_{\frac{d}{2}}(x)\cap U_{\frac{d}{2}}(y)=\varnothing$

---

> [!quote] 定理
> Hausdorff空间中任意有限集都是闭集

只要证任何一个单点集 $\{x_0\}$ 是闭集。设 $x\in X$ 异于 $x_0$，那么 $x$ 和 $x_0$ 分别有无交的邻域 $U$ 和 $V$。于是 $U$ 与 $\{x_0\}$ 无交， $x$ 就不属于 $\{x_0\}$ 的闭包，因此 $\{x_0\}$ 的闭包就是 $\{x_0\}$ ，所以 $\{x_0\}$ 是闭集

---

有限点集是闭集这一条件实际上是比Hausdorff条件更弱的条件，若任意有限集都是闭集不一定Hausdorff

> [!quote] 例
> $\mathbb{R}$ 关于有限补拓扑并不是一个Hausdorff空间，但在此空间中有限集是闭集

> [!NOTE]  $T_{1}$  公理（  $T_{1}$  axiom）
> **$T_{1}$  公理($T_{1}$  axiom)**：有限集是闭集

> [!NOTE]  Fréchet空间/T1空间/ $T_1$ 空间(Fréchet space)
>满足 $T_{1}$ 公理的拓扑空间 $X$ 称一个 **Fréchet空间/T1空间/ $T_1$ 空间(Fréchet space)**

以上讨论说明 T1 一定 T2，T2 不一定 T1
我们将在第3部分对其做进一步说明

> [!quote] 命题
> $X$ 是T1空间$\iff\forall x\neq y\in X,\exists$ 开集 $U, x\in U,y\notin U$ 

证明留作练习

---

> [!quote] 问题
> 
> $X$ 使得 $\forall x,y\in X,x\neq y，\exists$ 开集 $U, (x\in U,y\notin U)\lor(y\in U,x\notin U)$ 
> 问 $X$ 是T1空间吗？

留作练习

---

> [!quote] 定理
> 拓扑空间 $X$ 满足 $T_{1}$  公理， $A$ 是 $X$ 的一个子集，则 $x$ 是 $A$ 的极限点$\iff x$  的任意邻域交 $A$ 无限

$\Leftarrow)$
设 $x$ 的任意邻域交 $A$ 无限，则必交于异于 $x$ 的一点，故 $x$ 是 $A$ 的一极限点

$\Rightarrow)$
（反证）设 $x$ 是 $A$ 的一个极限点， $x$  的某邻域 $U$ 交 $A$ 有限，故  $U$ 交 $A - \{x\}$ 有限，设其为 $\{x_1, \dots, x_m\}$
 ，因为有限集  $\{x_1, \dots, x_m\}$  是闭集，所以  $X - \{x_1, \dots, x_m\}$  是  $X$  的一个开集。因此 $U \cap (X - \{x _ {1}, \dots , x _ {m} \})$ 就是与  $A - \{x\}$  无交的  $x$  的一个邻域，与 $x$ 是 $A$ 的极限点矛盾

---

我们对  $T_{1}$ 公理不是很感兴趣，因为拓扑的许多有趣的定理需要强于他的  $T_{2}$ 公理
此外对拓扑学家而言重要的空间大多都是Hausdorff空间。下面的两个定理是以上说法的佐证

> [!quote] 定理
>  $X$ 是一个Hausdorff空间，则 $X$ 中的一个序列最多收敛到一个点

设 $X$ 中点的序列 $x_{n}$ 收敛到  $x$ 
（反证）设还收敛到 $y \neq x$ , 记 $U$ 和 $V$ 分别是 $x$ 和 $y$ 的两无交邻域
由 $U$ 包含着除有限个之外所有的 $x_{n}$ , 所以 $V$ 至多包含有限个 $x_{n}$，与收敛到 $y$ 矛盾

---

> [!NOTE] Hausdorff 空间中序列的极限 (limit)
> Hausdorff 空间 $X$ 中的序列 $x_{n}$ 收敛到 $X$ 中的点 $x$, 我们通常记为 $x_{n} \to x$ , 并称 $x$ 为序列  $x_{n}$ 的**极限 (limit)**

下述定理的证明留给读者
> [!quote] 定理
> 每一个具有序拓扑的全序集是一个Hausdorff空间
> 两个Hausdorff空间的积是一个Hausdorff空间
> Hausdorff空间的子空间是一个Hausdorff空间

Hausdorff条件一般被认为是加到拓扑空间上的一个很合适的附加条件。事实上，在拓扑学基本教程中，有些数学家甚至在一开始就加上这个条件，而对不满足Hausdorff条件的空间不加研究。我们不准备这么办，但是在证明需要的时候，总是假定有Hausdorff条件，除非它对于结果的应用范围产生了令人不能满意的苛刻限制

Hausdorff条件是能够加到拓扑空间上的许多条件中的一个．人们每加上这样一个条件，就可以证明更强的定理，但也限制了适用这些定理的空间类．从拓扑学创立以来，相当一部分研究工作就是在寻求这样一些条件，这些条件比较强，但能使人们在满足这些条件的空间上证明一些有意义的定理；然而这些条件又不能太强，以免导致其结论的应用受到苛刻的限制

我们将在后面两章研究这样一些条件，$T_{1}，T_{2}$  公理只不过是我们熟悉的通称为分离性公理的一个系列条件中的两个。其他的条件包括可数性公理、紧致性以及连通性等，你将会发现，它们中的一些确实是相当强的限制
# 第8节 连续映射
## 8-1 连续性
本节将给出连续函数的定义（以上述各种连续函数为特例），我们还要研究连续函数的一些性质，其中的大部分内容都是我们在微积分和分析中所给出的连续函数的性质的直接推广。
> [!连续映射(continuous function)]
>  $X$ 和 $Y$ 是拓扑空间，函数  $f: X \to Y$  称为**连续的(continuous)**，若 $\forall$ 开集 $V\subseteq Y$， $f^{-1}(V)$  是 $X$ 中的一个开子集

注 $f^{-1}(V)$  是 $X$ 中所有使得 $f(x) \in V$ 的点  $x$  的集合。如果 $V$ 与 $f(X)$ 无交，那么 $f^{-1}(V) = \emptyset$ 

函数的连续性不仅依赖于  $f$  本身，也依赖于它的定义域和值域确定的拓扑。要想强调指出这一点，就说  $f$  相对于  $X$  的某拓扑和  $Y$  的某拓扑而言是连续的

注意若的拓扑是由基  $\mathcal{B}$  给出的，那么证  $f$  连续就只要证每个基元素的原像是开的

> [!quote] 定理
> 若值域  $Y$  上的拓扑由 $\mathcal B$ 给出，则 $f$ 连续$\iff f^{-1}(B)$ 是开集，$\forall B\in\mathcal B$

$Y$ 的任意开集 $V$ 可以写成基元素的并，即
$$V = \bigcup_ {\alpha \in J} B _ {\alpha}$$
因此$$f ^ {- 1} (V) = \bigcup_ {a \in J} f ^ {- 1} \left(B _ {a}\right)$$
如果每一个  $f^{-1}(B_{\alpha})$  是开的，那么  $f^{-1}(V)$  就是开的

如果  $Y$  的拓扑是由子基  $\mathcal{S}$  给出的，那么为了证明  $f$  的连续性，只要证明每一个子基元素的原像是开的就可以了。这是因为  $Y$  的任意基元素  $B$  可以写成子基元素的有限交  $S_{1} \cap \cdots \cap S_{n}$ 。由于
$$
f ^ {- 1} (B) = f ^ {- 1} \left(S _ {1}\right) \cap \dots \cap f ^ {- 1} \left(S _ {n}\right)
$$

因此每一个基元素的原像是开的

---

> [!quote] 命题
> 对 $f: \mathbb {R} \to \mathbb {R}$，$\varepsilon-\delta$  定义$\iff$连续映射的定义
> 

$\Leftarrow)$

对 $x_0\in\mathbb{R}$，给定 $\varepsilon > 0$，$V = (f(x_0) - \varepsilon, f(x_0) + \varepsilon)$  是值域 $\mathbb{R}$ 的开集，故 $f^{-1}(V)$ 是定义域空间  $\mathbb{R}$  的开集

因为 $f^{-1}(V)$ 包含 $x_0$，所以包含 $x_0$ 的某一个基元素  $(a, b)$

取 $\delta=\min\{x_0 - a,b - x_0\}$，则若 $|x - x_0| < \delta$，则点 $x$ 必定在  $(a, b)$ 之中，故 $f(x) \in V$，从而  $|f(x) - f(x_0)| < \varepsilon$

$\Rightarrow)$
留给读者

---

> [!quote] EX
> 在微积分中要研究很多种函数的连续性质，如函数
> $f: \mathbb{R} \longrightarrow \mathbb{R}^2$  （平面曲线），
> $f: \mathbb{R} \longrightarrow \mathbb{R}^3$  （空间曲线），
> $f: \mathbb{R}^2 \longrightarrow \mathbb{R}$  （两个实变量的函数  $f(x, y)$ ）
> $f: \mathbb{R}^3 \longrightarrow \mathbb{R}$  （三个实变量的函数  $f(x, y, z)$ ）
> $f: \mathbb{R}^2 \longrightarrow \mathbb{R}^2$  （平面上的向量场  $\pmb{v}(x, y)$ ）
> 都可以定义连续性
> 
> 我们所给的连续性的一般定义包括了所有这些特殊情形，这不过是将要证明的有关积空间及度量空间上连续函数的一些一般性定理的一个推论

> [!quote] 例
>$\mathbb{R}$  为具有通常拓扑的实数集，  $\mathbb{R}_t$  为具有下限拓扑的实数集
> 恒等映射 $f: \mathbb {R} \longrightarrow \mathbb {R} _ {\ell}$ 不连续，因为  $\mathbb{R}_t$  的开集  $[a,b)$  的原像还是  $[a,b)$  ，不是 $\mathbb{R}$ 的开集
> 恒等映射 $g: \mathbb {R} _ {\ell} \longrightarrow \mathbb {R}$ 连续，因为 $(a,b)$ 的原像是 $(a,b)$，是 $\mathbb{R}_t$ 中的开集

我们把上例提炼成以下定理

> [!quote] 定理
> $\mathcal T,\mathcal T'$ 是 $X$ 上的拓扑空间，$\mathcal T\subsetneq\mathcal T'$，则
> 单位映射 $f:(X,\mathcal T)\to (X,\mathcal T')$ 不连续
> 单位映射 $g:(X,\mathcal T')\to (X,\mathcal T)$ 不连续

分析中研究过连续函数的许多不同但又等价的定义。它们中的一些可以推广到任意空间上去，下面的定理就研究这个问题。但是，大家熟悉的“ $\varepsilon-\delta$  定义”及“收敛序列定义”却不能推广到任意空间。研究度量空间时，将要处理这些问题

> [!quote] 定理
> $X$ 和 $Y$ 是拓扑空间，$f: X \to Y$，以下等价：
> (1)  $f$  连续
> (2) $\forall A\subseteq X，f(\overline{A}) \subseteq \overline{f(A)}$
> (3) $\forall B\subseteq Y，f^{-1}(B)$  是  $X$  中的一个闭集
> (4) $\forall x\in X$ 和 $f(x)$ 的邻域  $V$，$\exists x$ 的一个邻域 $U，f(U)\subseteq V$
> 

$(1) \Rightarrow (2)$

设 $f$ 连续，$A\subseteq X$

下证 $x \in \overline{A}\Rightarrow f(x) \in \overline{f(A)}$

设 $V$ 是 $f(x)$ 的一个邻域，则  $f^{-1}(V)$  是  $X$  中包含  $x$  的一个开集，它必与 $A$ 交于某点  $y$ ，故  $V$  与  $f(A)$  有交点  $f(y)$ ，故 $f(x) \in \overline{f(A)}$

$(2) \Rightarrow (3)$

设  $B$  是  $Y$  的一个闭集，$A = f^{-1}(B)$ 

下证  $A$  是  $X$  的一个闭集，即证  $\overline{A} \subseteq A$

由集合论  $f(A) \subseteq B$，故对  $x \in \overline{A}$
$$
f (x) \in f (\overline {A}) \subset \overline {{f (A)}} \subset \overline {B} = B
$$

故  $x \in f^{-1}(B) = A$ ，所以得到  $\overline{A} \subseteq A$

$(3) \Rightarrow (1)$

设  $V$  是  $Y$  的一个开集，$B = Y - V$，则$$f ^ {- 1} (B) = f ^ {- 1} (Y) - f ^ {- 1} (V) = X - f ^ {- 1} (V)$$
易见  $B$  是  $Y$  中的一个闭集。根据假设 $f^{-1}(B)$  是  $X$  的一个闭集，故  $f^{-1}(V)$  是开的

$(1) \Rightarrow (4)$

设  $x \in X, V$  是  $f(x)$  的一个邻域. 则  $U = f^{-1}(V)$  是  $x$  的一个邻域，满足  $f(U) \subseteq V$ 

$(4) \Rightarrow (1)$

设  $V$  是  $Y$  的一个开集，$x$  是  $f^{-1}(V)$  的一个点. 则  $f(x) \in V$ , 由假设存在 $x$ 的一个邻域  $U_x$  使得  $f(U_x) \subseteq V$

故 $U_x \subset f^{-1}(V)$，故 $f^{-1}(V)$ 可表示为所有这些开集  $U_x$  之并，故它是开的

---

> [!NOTE] 在点  $x$ 连续
> $\forall x\in X$ ，如果(4)成立，称  $f$  在点  $x$  **连续**
## 练习

> [!quote] 问题
> 证明：函数  $f: \mathbb{R} \to \mathbb{R}$  连续性的  $\epsilon-\delta$  定义蕴涵开集定义。  

> [!quote] 问题
> 设  $f: X \to Y$  连续,  $x$  是  $X$  的子集  $A$  的一个极限点, 那么  $f(x)$  一定是  $f(A)$  的极限点吗?  

> [!quote] 问题
> 设  $X$  和  $X'$  分别表示具有拓扑  $\mathcal{T}$  和  $\mathcal{T}'$  的同一个集合， $i: X' \to X$  为恒等函数。
> (a)证明：  $i$  连续  $\Longleftrightarrow \mathcal{T}'$  细于  $\mathcal{T}$  
> (b)证明：  $i$  是同胚  $\Longleftrightarrow \mathcal{T}' = \mathcal{T}$

> [!quote] 问题
> 给定  $x_0 \in X$  和  $y_0 \in Y$ ，证明：分别由
> $$
> f (x) = x \times y _ {0} \quad {\text {和}} \quad g (y) = x _ {0} \times y
> $$
> 所定义的映射  $f: X \to X \times Y$  与  $g: Y \to X \times Y$  都是嵌入

> [!quote] 问题
> 证明： $\mathbb{R}$  的子空间  $(a, b)$  与  $(0, 1)$  同胚； $\mathbb{R}$  的子空间  $[a, b]$  与  $[0, 1]$  同胚 

> [!quote] 问题
> 找出一个只在一点连续的函数  $f: \mathbb{R} \to \mathbb{R}$  

> [!quote] 问题
>  (a) 假定  $f: \mathbb{R} \rightarrow \mathbb{R}$  “右连续”，即对于每一个  $a \in \mathbb{R}$ ，
> 
> $$
> \lim  _ {x \to a ^ {+}} f (x) = f (a)
> $$
> 
> 证明：将  $f$  看成从  $\mathbb{R}_l$  到  $\mathbb{R}$  的一个函数时它是连续的.
> 
> (b) 如果把函数  $f: \mathbb{R} \rightarrow \mathbb{R}$  看成从  $\mathbb{R}$  到  $\mathbb{R}_{\ell}$  的映射时，什么样的  $f$  是连续的？如果看成从  $\mathbb{R}_{\ell}$  到  $\mathbb{R}_{\ell}$  的映射呢？我们将在第3章中讨论这个问题

> [!quote] 问题
> 设  $Y$  为具有序拓扑的全序集， $f, g: X \to Y$  是连续的
> (a) 证明:  $\{x \mid f(x) \leqslant g(x)\}$  在  $X$  中是闭的
> (b)证明：由下式
> $$
> h (x) = \min  \left\{f (x), g (x) \right\}
> $$
> 所定义的函数  $h: X \to Y$  是连续的（提示：应用黏结引理）

设  $\{A_{\alpha}\}$  是  $X$  的一个子集族， $X = \bigcup_{\alpha} A_{\alpha}$ . 设  $f: X \to Y$ ，对于每一个  $\alpha$ ， $f \mid A_{\alpha}$  连续.
(a) 若  $\{A_{\alpha}\}$  为有限族，并且每一个  $A_{\alpha}$  都是闭集，则  $f$  连续.  
(b) 找出一个可数族  $\{A_{\alpha}\}$ ，其中每一个  $A_{\alpha}$  都是闭集，但  $f$  不连续的例子.  
(c) 3一个加标集族  $\{A_{\alpha}\}$  称为局部有限的(locally finite)，如果  $X$  的每一个点  $\pmb{x}$  都有一个邻域，仅与有限多个  $A_{\alpha}$  相交．证明：若族  $\{A_{\alpha}\}$  是局部有限的，并且每一个  $A_{\alpha}$  都是闭集，则  $f$  连续.

10. 设  $f: A \to B$  和  $g: C \to D$  都是连续函数．证明：由公式

$$
(f \times g) (a \times c) = f (a) \times g (c)
$$

所定义的映射  $f \times g: A \times C \to B \times D$  是连续的.

11. 设  $F: X \times Y \to Z$ . 我们把  $F$  分别关于每一个变量连续 (continuous in each variable separately) 定义为: 对于  $Y$  中每一个  $y_0$ , 用  $h(x) = F(x \times y_0)$  定义的映射  $h: X \to Z$  连续, 并且对于  $X$  中每一个  $x_0$ , 用  $k(y) = F(x_0 \times y)$  所定义的映射  $k: Y \to Z$  连续. 证明: 若  $F$  连续, 则  $F$  分别关于每一个变量连续.

12. 设  $F: \mathbb{R} \times \mathbb{R} \to \mathbb{R}$  定义为：

$$
F (x \times y) = {\left\{ \begin{array}{l l} {x y / (x ^ {2} + y ^ {2})} & {{\text {如 果}} x \times y \neq 0 \times 0,} \\ {0} & {{\text {如 果}} x \times y = 0 \times 0.} \end{array} \right.}
$$

(a)证明：  $F$  分别关于每一个变量连续  
(b)计算出由  $g(x) = F(x\times x)$  所定义的函数  $\pmb{g}$  ：  $\mathbb{R}\to \mathbb{R}$  
(c) 证明  $F$  不连续.

13. 设  $A \subset X$ ， $f: A \to Y$  连续， $Y$  是一个Hausdorff空间。证明：若  $f$  能扩充为一个连续函数  $g: \overline{A} \to Y$ ，则  $g$  由  $f$  唯一决定。

## 8-2 同胚
> [!NOTE] 同胚（homeomorphism），同胚的(homeomorphic)
>  $X$ 和 $Y$ 都是拓扑空间，若 
> - $f: X \to Y$ 连续可逆双射
> - $f ^ {- 1}: Y \to X$ 连续
> 
> 则称 $f$ 为一个**同胚（homeomorphism）**，$X$ 和 $Y$ 称 **同胚的(homeomorphic)**，记作 $X\simeq  Y$

> [!warning] RMK
> 同胚即拓扑学中的等价。事实上，同胚保证了 $X$ 和 $\tau$ 都是双射

$f^{-1}$  连续这个条件是说，对于  $X$  的每一个开集  $U$  ，在  $f^{-1}: Y \to X$  下它的原像是  $Y$  中的开集．但是， $U$  在映射  $f^{-1}$  下的原像就是  $U$  在映射  $f$  下的像，于是可用另一种方式将同胚定义为一一映射  $f: X \to Y$  ，使得  $f(U)$  是一个开集的充分必要条件是  $U$  是一个开集
<img src ="c9f8ec6028004c4e29cfd42b4f39b5a8a768988b5d2b4b8ac7cdd0859829deb2.jpg" width = 400>

这个附注说明，一个同胚  $f: X \to Y$ ，不仅仅给出了  $X$  和  $Y$  之间的一个一一映射，还给出了  $X$  与  $Y$  的开集族之间的一个一一映射。因此

> [! ] 拓扑性质(topological property)
> 完全藉助于 $X$ 的拓扑（即藉助于 $X$ 的开集）所得出的  $X$  的任何一条性质，通过对应  $f$  就可以推出空间 $Y$ 的相应性质。 $X$ 的这种性质称为  $X$  的一个**拓扑性质(topological property)**

读者可能已在近世代数中学过代数对象之间同构的概念，比如群与群之间，环与环之间。一个同构是一个保持代数结构的一一映射。拓扑学中与此类似的概念就是同胚，它是保持拓扑结构的一一映射

> [!NOTE] 拓扑嵌入（topological imbedding），嵌入(imbedding)
>  $f: X \to Y$ 是一个连续的单射， $X$  和  $Y$  是拓扑空间。像集  $f(X)$ 看成  $Y$  的一个子空间。若  $f'$  正好是 $X$ 与 $f(X)$ 之间的一个同胚，则称映射  $f: X \to Y$  是一个**拓扑嵌入（topological imbedding）**，或者称为从  $X$  到  $Y$  中的一个**嵌入(imbedding)**

> [!quote] EX
> 函数 $f: \mathbb{R} \to \mathbb{R}，f(x) = 3x + 1$ 是一个同胚
> <img src = "0bc6aabd300532327c00cf5a9cb6e6409d6f9f59aa6040f40172dc305810f9db.jpg" width = 200>
> 考虑用$g (y) = \frac {1}{3} (y - 1)$ 定义的函数  $g: \mathbb{R} \to \mathbb{R}$ ，易验对于所有实数 $x$ 和 $y$ 有 $f(g(y)) = y$  和  $g(f(x)) = x$ ，因此 $f$ 是双射且 $g = f^{-1}$ 。至于 $f$ 与 $g$ 的连续性则是微积分中熟知的结论

> [!quote] EX
> 函数  $F: (-1, 1) \to \mathbb{R},F (x) = \displaystyle\frac {x}{1 - x ^ {2}}$ 是一个同胚
> 我们已知 $F$ 是一个保序双射，它的反函数$$G (y) = \frac {2 y}{1 + (1 + 4 y ^ {2}) ^ {1 / 2}}$$
> <img src = "bf2a56240825782f9d27d6ba40c5077b9da4af3b111d3e1fd333a1a05abd0c90.jpg" width = 200> 
> 
> 可以用两种方法证明  $F$  是一个同胚．第一个方法应用  $F$  是一个保序双射，从而把  $(-1, 1)$  中序拓扑的一个基元素变成  $\mathbb{R}$  中序拓扑的一个基元素，反之亦然．这样  $F$  自然就是  $(-1, 1)$  与  $\mathbb{R}$  之间(相对于各自的序拓扑而言)的一个同胚．因为$(-1, 1)$  上的序拓扑就是通常的(子空间)拓扑，所以  $F$  是  $(-1, 1)$  与  $\mathbb{R}$  的一个同胚。证 $F$ 是同胚的第二个方法是应用微积分中熟悉的结果，即代数函数和根式函数的连续性来证 $F$ 和 $G$ 都连续

双射 $f$  ： $X\to Y$ 可以是连续的而不是同胚
我们研究过的恒等映射  $g:\mathbb{R}_t\rightarrow \mathbb{R}$  就是这样一个函数
其他例子：
> [!quote] EX
> 设 **单位圆周(unit circle)** $S ^ {1} = \{x \times y \mid x ^ {2} + y ^ {2} = 1 \}$，将其作为平面  $\mathbb{R}^2$  的一个子空间．映射 $f: [ 0, 1) \longrightarrow S ^ {1}$ 定义为 $f(t) = (\cos 2\pi t, \sin 2\pi t)$
> 应用三角函数的性质， $f$ 是连续双射，但 $f^{-1}$ 不连续
> 如定义域中的开集  $U = \displaystyle\left[0, \frac{1}{4}\right)$  在 $f$ 下的像不是 $S^1$ 中的开集, 这是由于不存在 $\mathbb{R}^2$ 中包含  $p = f(0)$ 的开集 $V$, 使 $V \cap S^1 \subset f(U)$
> <img src="ea32353438ad578d46ceb5b41c3c8263f76e0121673807ca45539b44300b6d60.jpg" width  =320>
> 

> [!quote] EX
> 函数 $g: [ 0, 1) \rightarrow \mathbb {R} ^ {2}$ 由上例中函数 $f$ 的值域扩大得。 $g$ 是连续单射，但不是嵌入

## 8-3 构造连续函数

如何构造从一个拓扑空间到另一个拓扑空间的连续函数？

分析中使用过的方法，有些可推广到拓扑空间，有些则不行。我们首先研究某些对于一般拓扑空间成立的构造法，其余的留到后面再讲

> [!quote] 定理 构造连续函数的法则（rules for constructing continuous functions）
> $X, Y,Z$ 是拓扑空间
> 
> ==(a)(常值函数 Constant function)== $f: X \to Y$  将整个  $X$  映成  $Y$  的一个点  $y_0$ ，则  $f$  连续
> 
> ==(b)(内射/嵌入 Inclusion/Embedding)== $A$  为  $X$  的一个子空间，则内射  $j: A \to X$  连续
> 
> ==(c)(复合 Composition)== $f: X \to Y$  与  $g: Y \to Z$  连续，则映射  $g \circ f: X \to Z$  连续
> 
> ==(d)(限制定义域 Restrict the domain)== $f: X \to Y$  连续,  $A$  为  $X$  的一个子空间, 则限制映射  $f|_{A}: A \to Y$  连续 
> 
> ==(e)(限制或扩大值域 Restricting or expanding the range)== $f: X \to Y$  连续,  $Z$  为  $Y$  中包含像集  $f(X)$  的一个子空间，则限制 $f$ 的值域而得到的函数  $g: X \to Z$  也连续。若  $Z$  以  $Y$  为其子空间，则扩大  $f$  的值域而得到的函数  $h: X \to Z$  也连续
> 
> ==(f)(连续性的局部表示 Local formulation of continuity)== 如果  $X$  可以写成开集  $U_{\alpha}$  的并，使得对于每一个  $\alpha$  ，  $f|U_{\alpha}$  连续，则 $f:X\to Y$  连续
> 
> ==(g)(定义域的任意并)== $X=\displaystyle\bigcup U_{\alpha},f\Big|_{U_{\alpha}}:U_{\alpha}\to Y$ 连续，则 $f:X\to Y$  连续

==(a)== 对 $X$ 的任意一点  $x$ ，设  $f(x) = y_0$，设  $V$  是  $Y$  中一开集

若  $y_0\in V$，则 $f^{-1}(V) = X$
若  $y_0\notin V$，则  $f^{-1}(V) = \emptyset$

无论哪一种情形 $f^{-1}(V)$ 都是开的

==(b)== 若 $U$ 是 $X$ 的一个开集，由子空间拓扑的定义  $j^{-1}(U) = U \cap A$  是  $A$  的一个开集

==(c)== 若  $U$  是  $Z$  的一个开集，则  $g^{-1}(U)$  是  $Y$  的一个开集， $f^{-1}(g^{-1}(U))$  是  $X$  的一个开集，而根据集合论 $f ^ {- 1} (g ^ {- 1} (U)) = (g \circ f) ^ {- 1} (U)$

==(d)== 函数  $f\mid A$  是内射  $j:A\to X$  与映射  $f:X\rightarrow Y$  的复合，而这两者都是连续函数

==(e)== 设  $f: X \to Y$  连续。若  $f(x) \subseteq Z \subseteq Y$ ，我们来证明由  $f$  得到的函数  $g: X \to Z$  连续。设  $B$  是  $Z$  的一个开集，则存在  $Y$  的某一个开集  $U$ ，使得  $B = Z \cap U$ 。因为  $Z$  包含整个像集  $f(X)$ ，根据集合论 $f ^ {- 1} (U) = g ^ {- 1} (B)$，因为  $f^{-1}(U)$  是开的，所以  $g^{-1}(B)$  也是开的

如果  $Z$  以  $Y$  为子空间，我们证明  $h: X \to Z$  连续。而这只要注意到  $h$  是映射  $f: X \to Y$  与内射  $j: Y \to Z$  的复合就行了

==(f)== 根据假设，  $X$  可以写成开集  $U_{\alpha}$  的并，并且对于每一个  $\alpha$  ，  $f|U_{\alpha}$  连续．设  $V$  是  $Y$  的一个开集，则 $f ^ {- 1} (V) \cap U _ {\alpha} = (f \mid U _ {\alpha}) ^ {- 1} (V)$，这是因为上式两边表示的都是  $U_{\alpha}$  中满足  $f(x)\in V$  的点 $x$ 的集合．因为  $f|U_{\alpha}$  连续，所以上述集合是  $U_{\alpha}$  中的开集，因此是  $X$  中的开集．而$$f ^ {- 1} (V) = \bigcup_ {a} (f ^ {- 1} (V) \cap U _ {a})$$于是，  $f^{-1}(V)$  也是  $X$  的一个开集

==(g)==
$V\subseteq Y$，$f^{-1}(V)=\displaystyle\bigcup_{\alpha}(f^{-1}(V)\cap U_{\alpha})$

---
> [!quote] 定理 黏结引理 pasting lemma
> $X = A \cup B$，$A、B$ 都是 $X$ 中闭集，$f: A \to Y、g: B \to Y$ 连续
> 
> 若 $\forall x \in A \cap B,f(x) = g(x)$ ，则 $f$ 和 $g$ 可以组成一个连续函数 $h: X \to Y$， $$h(x) = \begin{cases}f(x)&x \in A\\\\ g(x)&x \in B\end{cases}$$

设  $C$  为  $Y$  的一个闭集，根据集合论
$$h ^ {- 1} (C) = f ^ {- 1} (C) \cup g ^ {- 1} (C)$$
因为  $f$  连续，所以  $f^{-1}(C)$  是  $A$  的一个闭集．类似地， $g^{-1}(C)$  是  $B$  的一个闭集，从而也是  $X$  的一个闭集．于是它们的并  $h^{-1}(C)$  是  $X$  的一个闭集
若  $A$  和  $B$  都是  $X$  的开集，这个定理仍然成立．这正是“连续性的局部表示”法则（见前一个定理)的一个特例

---

> [!quote] EX
> 函数  $h: \mathbb{R} \rightarrow \mathbb{R}$，$h (x) = \begin{cases} x &x \leqslant 0\\ x / 2 &x \geqslant 0 \end{cases}$ 在每一“区间段”都是连续函数，并且它们在定义域的公共部分，即单点集  $\{0\}$  上的函数值相同。由于两者的定义域都是  $\mathbb{R}$  的闭集，所以  $h$  连续
> 为能定义这种函数，就要求对于各个“区间段”来说，函数在其定义域的重合处相等。如
> $$k (x) = \left\{ \begin{array}{l l} x - 2 &x \leqslant 0\\ x + 2 &x \geqslant 0\end{array} \right.$$
> 就不能定义一个函数。另一方面，对于集合  $A$  和  $B$  也要进行某些限制以保证函数的连续性，如 $l (x) =\begin{cases}x - 2 &x <   0\\ x + 2 &x \geqslant 0\end{cases}$ 定义了从  $\mathbb{R}$  到  $\mathbb{R}$  的一个函数，它的两个部分虽然是连续的，但是  $l$  却不是连续函数。因为开集$(1，3)$的原像$[0，1)$不是开集
> <img src ="274f5f06269afb5601fc317aab348dadcc0ad3bd53a67ae6ed7190c519c6a1db.jpg" width = 400>
> 

> [!quote] THM 到积空间的映射(maps into products)
> $f: A \to X \times Y，f (a) = \left(f _ {1} (a), f _ {2} (a)\right)$，则
> $f$  连续 $\iff$ 函数$f _ {1}: A \longrightarrow X \quad {\text {与}} \quad f _ {2}: A \longrightarrow Y$ 都连续

设  $\pi_1: X \times Y \to X$  与  $\pi_2: X \times Y \to Y$  分别是到第一个和第二个坐标空间上的投射，它们是连续的。这是因为若设  $U$  和  $V$  分别是  $X$  和  $Y$  中的开集，则  $\pi_1^{-1}(U) = U \times Y$  和  $\pi_2^{-1}(V) = X \times V$  都是开集。注意，对于每一个  $a \in A$ ，
$$
f _ {1} (a) = \pi_ {1} (f (a)), \quad f _ {2} (a) = \pi_ {2} (f (a)).
$$
若  $f$  是连续函数，则  $f_{1}$  和  $f_{2}$  是连续函数的复合，因而都是连续的。反之，设  $f_{1}$  和  $f_{2}$  连续，我们证明：对于  $X \times Y$  的拓扑的每一个基元素  $U \times V$ ，其原像  $f^{-1}(U \times V)$  是开集。点  $a$  在  $f^{-1}(U \times V)$  中当且仅当  $f(a) \in U \times V$ ，也就是当且仅当  $f_{1}(a) \in U$  并且  $f_{2}(a) \in V$，故$$f ^ {- 1} (U \times V) = f _ {1} ^ {- 1} (U) \cap f _ {2} ^ {- 1} (V)$$
由  $f_{1}^{-1}(U)$  和  $f_{2}^{-1}(V)$  都是开集，它们的交也是开的

---
> [! ] 坐标函数(coordinate function)
> 映射  $f_{1}$  和  $f_{2}$  称为  $f$  的**坐标函数(coordinate function)**

对于定义域是积空间的映射  $f: A \times B \to X$ ，没有一个常用的方法来判断其连续性。有这样的一种猜想：如果  $f$  “分别关于每一个变量”连续，则 $f$ 连续。但它是不对的 (见习题12)

> [!quote] EX
> 微积分中，平面上一条参数曲线被定义为一个连续映射  $f: [a, b] \to \mathbb{R}^2$ ，通常写成  $f(t) = (x(t), y(t))$ 。我们常常要用到这样的结论：若  $x$  和  $y$  都是  $t$  的连续函数，则  $f$  是  $t$  的一个连续函数。类似地，平面向量场$$\boldsymbol {v} (x, y) = P (x, y) \boldsymbol {i} + Q (x, y) \boldsymbol {j} = (P (x, y), Q (x, y))$$
> 称为连续的，如果  $P$  和  $Q$  都是连续函数；或者等价地说， $\pmb{v}$  作为  $\mathbb{R}^2$  到  $\mathbb{R}^2$  的映射是连续的。这两种说法都是上面定理的特殊情形

在分析中大量使用的构造连续函数的方法是取连续实值函数的和、差、积、商．有一个标准定理：若  $f, g: X \to \mathbb{R}$  连续，则  $f + g$  、 $f - g$  、 $f \cdot g$  都连续，并且对于所有使  $g(x) \neq 0$  的  $x$  ， $f / g$  连续．我们将在第21节研究这个定理

在分析中我们所熟悉的构造连续函数的另一个办法，是取函数的无穷序列的极限。有这样一个定理，其大意是说，如果一个实变量连续实值函数的序列一致收敛于一个极限函数，那么极限函数必为连续函数。这个定理称为一致极限定理。如当正弦、余弦函数的定义严格地用无穷级数给出时，用这个定理可证明三角函数的连续性。这个定理能够推广为关于从任意拓扑空间  $X$  到度量空间  $Y$  中映射的定理，我们将在第21节予以证明


# 第9节 任意积拓扑与箱拓扑
## 9-1 有限积拓扑与任意积拓扑

本章余下部分将继续讨论如何在集合上给出拓扑的方法

此前我们定义了二元积拓扑，本节将这个定义推广到任意笛卡儿积
考虑笛卡儿积
$$X _ {1} \times \dots \times X _ {n} \quad {\text {和}} \quad X _ {1} \times X _ {2} \times \dots$$
其中  $X_{i}$  都是拓扑空间

定义笛卡儿积的拓扑有两种方式

1. 分别以 $U_{1} \times \dots \times U_{n}$ 和 $U_{1} \times U_{2} \times \dots$  作为上述相应笛卡儿积的拓扑的基元素， $U_{i}$  表示  $X_{i}$  中的一个开集，称箱拓扑，看上去美观但不好用

2. 推广用子基定义拓扑的方式，即以  $\pi_i^{-1}(U_i)$  构成子基，（$i$  是任意指标），$U_i$  是  $X_i$  中的一开集。称积拓扑，看上去丑但好用

两种拓扑有什么不同？

考虑第二种拓扑的典型基元素 $B$ 。它是子基元素  $\pi_i^{-1}(U_i)$  的有限交，如  $i = i_1, \dots, i_k$ 

则点 $x\in B\iff$对于  $i = i_1, \dots, i_k$  时 $\pi_i(x)$ 属于 $U_i$ ，而当 $i$ 为其余值时，对 $\pi_i(x)$ 没有任何限制

故两种拓扑对有限笛卡儿积相同，对无限笛卡儿积不同。为何更偏爱第二种拓扑？这是我们本节将要说明的问题

先引入广义笛卡尔积：此前仅就指标集为  $\{1, \dots, n\}$  或者为 $\mathbb{Z}_{+}$ 的情形定义了加标族的笛卡儿积。下考虑指标集为任意集合的情形

> [!广义笛卡尔积]
> $J$  是一个指标集，集合 $X$ 元素的 ** $J$-串  $(J$-tuple) ** 定义为映射  $x: J \to X$
> 
>$\alpha\in J$，$x_{\alpha}:=x(\alpha)$ 称 $x$ 的第 $\alpha$ 个**坐标(coordinate)**
>
>用记号$\left(x _ {\alpha}\right) _ {\alpha \in J}$表示函数  $x$  本身
>
>
> 
> $\{A_{\alpha}\}_{\alpha \in J}$  是一个加标集族， $X =\displaystyle\bigcup_{\alpha \in J} A_{\alpha}$ ，加标集族  $\{A_{\alpha}\}_{\alpha \in J}$  的 **笛卡儿积(Cartesian product)** $$\displaystyle\prod_ {\alpha \in J} A _ {\alpha}:=\{(x_{\alpha})_{\alpha \in J}:\forall \alpha \in J,x_{\alpha} \in A_{\alpha}\}$$
> 
> 即所有满足 $\forall\alpha \in J,x(\alpha) \in A_{\alpha}$ 的函数 $x: J \longrightarrow \displaystyle\bigcup_ {\alpha \in J} A _ {\alpha}$ 的集合
> 不强调指标集时也用  $\displaystyle\prod A_{\alpha}$  表示上述笛卡儿积，其元素则记为  $(x_{\alpha})$

注 由集合论，$X$ 中元素的 $J$-串的全体记作 $X^{J}$

当所有的 $A_{\alpha}$ 都等于同一个集合 $X$ 时，笛卡儿积  $\displaystyle\prod_{\alpha \in J} A_{\alpha}$  恰为所有  $X$  的元素的  $J-$  串的集合  $X^{J}$
对于  $X^{J}$  的元素，我们有时使用“串记法”表示，有时使用函数表示，依方便而定

> [! ] 箱拓扑(box topology)
> $\{X_{\alpha}\}_{\alpha \in J}$  是拓扑空间的一个加标族，积空间$\displaystyle\prod_ {\alpha \in J} X _ {\alpha}$上的某一个拓扑的基取为所有形如$\displaystyle\prod_ {\alpha \in J} U _ {\alpha}$的集合的族，其中对于每一个  $\alpha \in J$  ，  $U_{\alpha}$  在  $X_{\alpha}$  中是开的
> 由这个基生成的拓扑叫做**箱拓扑(box topology)**

> [!quote] 命题 箱拓扑良定义
> 箱拓扑是一个拓扑

因为  $\displaystyle\prod X_{\alpha}$  本身是一个基元素，所以  $\left\{\displaystyle\prod U_{\alpha}\right\}$  满足基定义中的第一个条件

又因为任意两个基元素的交是另一个基元素$$\left(\prod_ {\alpha \in J} U _ {\alpha}\right) \cap \left(\prod_ {\alpha \in J} V _ {\alpha}\right) = \prod_ {\alpha \in J} \left(U _ {\alpha} \cap V _ {\alpha}\right)$$所以它满足基定义中的第二个条件

下面的方法是用子基定义拓扑的推广

> [!NOTE] 关于指标  $\beta$  的投射(projection mapping)
> 函数 $\displaystyle\pi_ {\beta}: \prod_ {\alpha \in J} X _ {\alpha} \longrightarrow X _ {\beta}$ 将笛卡儿积空间的每一个元素对应其第  $\beta$  个坐标，即$\pi_ {\beta} \left(\left(x _ {a}\right) _ {a \in J}\right) = x _ {\beta}$
> $\pi_{\beta}$  称为**关于指标  $\beta$  的投射(projection mapping)**

> [!NOTE] 积拓扑 (product topology)，积空间 (product space)
> 令$\mathcal {S} _ {\beta} = \left\{\pi_ {\beta} ^ {- 1} \left(U _ {\beta}\right) \mid U _ {\beta} \text { 在 }X _ {\beta}\text { 中是开的} \right\}，\mathcal {S} = \displaystyle\bigcup_ {\beta \in J} \mathcal {S} _ {\beta}$
> 子基  $\mathcal{S}$  生成的拓扑称为**积拓扑 (product topology)**，给定了这个拓扑的  $\displaystyle\prod_{\alpha \in J} X_{\alpha}$  称为**积空间 (product space)**

> [!quote] 定理 箱拓扑与积拓扑的比较（comparison of the box and product topologies）
> $\displaystyle\prod X_{\alpha}$  的箱拓扑以形如  $\displaystyle\prod U_{\alpha}$  的集合作为基元素，其中，对于每一个  $\alpha, U_{\alpha}$  在  $X_{\alpha}$  中是开的
> $\displaystyle\prod X_{\alpha}$  的积拓扑以形如  $\displaystyle\prod U_{\alpha}$  的集合作为基元素，其中  $U_{\alpha}$  在  $X_{\alpha}$  中是开，并且除去有限多个  $\alpha$  外， $$\forall\alpha,U_{\alpha} = X_{\alpha}$$ 

考虑由 $S$ 生成的基  $\mathcal{B}$ 。族  $\mathcal{B}$  是由  $S$  中元素的所有有限交组成的。但如果取属于同一个 $S_{\beta}$ 中的元素进行交，不能得到什么新东西，因为
$$\pi_ {\beta} ^ {- 1} \left(U _ {\beta}\right) \cap \pi_ {\beta} ^ {- 1} \left(V _ {\beta}\right) = \pi_ {\beta} ^ {- 1} \left(U _ {\beta} \cap V _ {\beta}\right)$$
$\mathcal{S}_{\beta}$  中的两个或有限多个元素的交，还是  $\mathcal{S}_{\beta}$  的一个元素．只有取不属于同一个  $\mathcal{S}_{\beta}$  的元素进行交，才能得到一些新东西．因此，基  $\mathcal{B}$  的典型元素可以这样描述：令  $\beta_{1},\dots ,\beta_{n}$  为指标集  $J$  中不同指标的一个有限集， $U_{\beta_i}$  为  $X_{\beta_i}$  中的一个开集  $(i = 1,\dots ,n)$ ．则
$$
B = \pi_ {\beta_ {1}} ^ {- 1} \left(U _ {\beta_ {1}}\right) \cap \pi_ {\beta_ {2}} ^ {- 1} \left(U _ {\beta_ {2}}\right) \cap \dots \cap \pi_ {\beta_ {n}} ^ {- 1} \left(U _ {\beta_ {n}}\right)
$$
是  $\mathcal{B}$  的一个典型的元素

因此点  $x = (x_{\alpha})$  在  $B$  中当且仅当  $x$  的第  $\beta_{1}$  个坐标在  $U_{\beta_1}$  中，第  $\beta_{2}$  个坐标在  $U_{\beta_2}$  中等等.如果指标  $\alpha$  不是  $\beta_{1}$  ，…，  $\beta_{n}$  中的一个，那么  $x$  的第  $\alpha$  个坐标就没有任何限制，于是可以将  $B$  写成积的形式
$$B = \prod_ {a \in J} U _ {a}$$
其中当  $\alpha \neq \beta_{1},\cdots,\beta_{n}$ 时， $U_{\alpha}$ 表示空间 $X_{\alpha}$

---

有两件事是清楚的
- 对有限积  $\displaystyle\prod X_{\alpha}$ , 两种拓扑是一样的
- 一般箱拓扑细于积拓扑

为何常用积拓扑而不是箱拓扑? 答案要从我们对拓扑学的研究中去找。如果用积拓扑，关于有限积空间的一些重要定理对于任意积空间也成立；而用箱拓扑则不然。因此积拓扑更为重要。但箱拓扑可用来构造反例

约定：讨论积空间  $\displaystyle\prod  X_{\alpha}$ 时，除非特别申明，总是假定所给的就是积拓扑

在有关积空间  $X \times Y$  的已经证明过的定理之中, 有一些对于积空间  $\displaystyle\prod  X_{\alpha}$  不论采用箱拓扑或积拓扑都成立
下面列出一些这样的定理

> [!quote] 定理
> 设每一个空间  $X_{\alpha}$  的拓扑由基  $\mathcal{B}_{\alpha}$  给出．则形如$\displaystyle\prod_ {\alpha \in J} B _ {\alpha}$的集族是  $\displaystyle\prod_{\alpha \in J} X_{\alpha}$  的箱拓扑的一个基，其中对于每一个  $\alpha, B_{\alpha} \in \mathcal{B}_{\alpha}$ 

对如上形式的集族，如果仅对有限多个指标  $\alpha$  要求  $B_{\alpha} \in \mathcal{B}_{\alpha}$ ，而对余下的指标有  $B_{\alpha} = X_{\alpha}$ ，则这个集族便是  $\prod_{\alpha \in J} X_{\alpha}$  的积拓扑的一个基

> [!quote] 例
> 考虑 $n$  维欧氏空间 $\mathbb{R}^n$ 
> 
> $\mathbb{R}$ 中所有开区间组成  $\mathbb{R}$  的一个基，因此所有形如
> $$
> \left(a _ {1}, b _ {1}\right) \times \left(a _ {2}, b _ {2}\right) \times \dots \times \left(a _ {n}, b _ {n}\right)
> $$
> 的积组成了  $\mathbb{R}^n$  的一个拓扑基。因为  $\mathbb{R}^n$  是有限积，箱拓扑与积拓扑是一样的

所以在讨论  $\mathbb{R}^n$  的时候，除非特别申明，都采用上面给出的这种拓扑
## 9-2 积拓扑和箱拓扑的性质
> [!quote] 定理
>$\forall\alpha \in J, A_{\alpha}$  是  $X_{\alpha}$  的一个子空间，则当两者都用箱拓扑或者两者都用积拓扑时， $\displaystyle\prod A_{\alpha}$  是  $\displaystyle\prod X_{\alpha}$  的一个子空间

> [!quote] 定理
> 若每一个空间  $X_{\alpha}$  都是Hausdorff的，则无论是箱拓扑还是积拓扑，  $\displaystyle\prod X_{\alpha}$  都是Hausdorff的

> [!quote] 定理
>  $\{X_{\alpha}\}$  是一个加标空间族，对每一个  $\alpha$  有  $A_{\alpha} \subset X_{\alpha}$。若对  $\displaystyle\prod X_{\alpha}$  赋予积拓扑或者赋予箱拓扑，则有$$\prod \overline {A} _ {\alpha} = \overline {{\prod A _ {\alpha}}}$$

设  $x = (x_{\alpha})$  为  $\displaystyle\prod\overline{A}_{\alpha}$  的一个点. 我们来证明  $x \in \overline{\displaystyle\prod A_{\alpha}}$ . 设  $U =\displaystyle\prod U_{\alpha}$  为箱拓扑或是积拓扑空间中含有  $x$  的一个基元素. 由于  $x_{\alpha} \in \overline{A}_{\alpha}$ , 对于每一个  $\alpha$ , 可以选取点  $y_{\alpha} \in U_{\alpha} \cap A_{\alpha}$ . 于是  $y = (y_{\alpha})$  既属于  $U$  又属于  $\displaystyle\prod A_{\alpha}$ . 由于  $U$  的任意性,  $x$  属于  $\displaystyle\prod A_{\alpha}$  的闭包
反之，设对于两个拓扑中的任何一个， $x = (x_{\alpha})$  属于  $\displaystyle\prod A_{\alpha}$  的闭包.我们来证明对于任何一个指标  $\beta$  ，有  $x_{\beta} \in \overline{A}_{\alpha}$ . 设  $V_{\beta}$  为包含  $x_{\beta}$  的  $X_{\beta}$  中的开集.由于对于两个拓扑中的无论哪一个来说， $\pi_{\beta}^{-1}(V_{\beta})$  是  $\displaystyle\prod X_{\alpha}$  中的开集，所以它含有  $\displaystyle\prod A_{\alpha}$  中的点  $y = (y_{\alpha})$  .于是  $y_{\beta}$  属于  $V_{\beta} \cap A_{\beta}$ . 从而  $x_{\beta} \in \overline{A}_{\beta}$

---

目前为止，我们仍然没有理由只喜欢积拓扑，而不要箱拓扑；但当我们试图推广前面关于映到积空间的映射的连续性的那个定理时，这种区别就出现了。当赋予  $\displaystyle\prod X_{\alpha}$  箱拓扑时，下面定理不成立

> [!quote] 定理
> 映射  $f: A \to \displaystyle\prod_{\alpha \in J} X_{\alpha}$  定义为
> $$
> f (a) = \left(f _ {a} (a)\right) _ {a \in J}
> $$
> 其中对每一个  $\alpha, f_{\alpha}: A \to X_{\alpha}$ . 设  $\Pi X_{\alpha}$  具有积拓扑，则  $f$  连续$\iff$每一个函数  $f_{\alpha}$  连续

$\Rightarrow)$

设  $\pi_{\beta}$  是积空间到其第  $\beta$  个坐标空间上的投射

$\pi_{\beta}$  连续，因为如果  $U_{\beta}$  是  $X_{\beta}$  的一个开集，集合  $\pi_{\beta}^{-1}(U_{\beta})$  就是  $\Pi X_{\alpha}$  的积拓扑的一个子基元素

设 $f:A\to\displaystyle\prod X_{\alpha}$  连续，则  $f_{\beta}$  是两个连续函数的复合，即  $f_{\beta} = \pi_{\beta}\circ f$  ，所以  $f_{\beta}$  连续

$\Leftarrow)$

设每一个坐标函数  $f_{\alpha}$  都连续。 要证 $f$ 连续，只需证每一子基元素在  $f$  下的原像是  $A$  的开集

定义连续函数时已提过这一点：对 $\displaystyle\prod X_{\alpha}$ 的积拓扑，其典型子基元素是  $\pi_{\beta}^{-1}(U_{\beta})$  ，其中  $\beta$  是某一个指标， $U_{\beta}$  是  $X_{\beta}$  的开集

因为  $f_{\beta} = \pi_{\beta}\circ f$  ，所以  $f^{-1}(\pi_{\beta}^{-1}(U_{\beta})) = f_{\beta}^{-1}(U_{\beta})$  ，又因  $f_{\beta}$  连续，这个集合是 $A$ 的一开集

---

为什么这个定理对于箱拓扑不成立呢？或许最令人信服的办法就是考察一个例子

> [!quote] 例
> 考虑 $\mathbb{R}$ 的可数无限积 $\displaystyle\mathbb {R} ^ {\omega} = \prod_ {n \in \mathbb {Z} _ {+}} X _ {n}$
> 
> 对于每一个 $n \in \mathbb{Z}_{+}$ ,  $X_{n} = \mathbb{R}$ . 函数  $f: \mathbb{R} \to \mathbb{R}^{n}$  定义为
> $$f (t) = (t, t, \dots)$$
> 其第 $n$ 个坐标函数是 $f_{n}(t) = t$，每一个坐标函数 $f_{n}\colon \mathbb{R}\to \mathbb{R}$ 都连续，所以当赋予  $\mathbb{R}^{\omega}$  积拓扑时， $f$  是连续的．而当 $\mathbb{R}^{\omega}$ 给的是箱拓扑时，$f$ 不连续
> 
> 如取箱拓扑的基元素
> $$
> B = (- 1, 1) \times \left(- \frac {1}{2}, \frac {1}{2}\right) \times \left(- \frac {1}{3}, \frac {1}{3}\right) \times \dots
> $$
> 我们断言： $f^{-1}(B)$  不是  $\mathbb{R}$  中开集
> （反证）设 $f^{-1}(B)$  是  $\mathbb{R}$  中开集，它必定包含 0 旁边的某一个区间  $(- \delta, \delta)$ ，也就是说  $f((-\delta, \delta)) \subset B$ 。将  $\pi_n$  作用于这个包含关系的两边，可见对于所有  $n$ ，$$f _ {n} ((- \delta , \delta)) = (- \delta , \delta) \subset \left(- \frac {1}{n}, \frac {1}{n}\right)$$
>矛盾



## 练习

1. 证明定理 19.2.  
2. 证明定理19.3.  
3. 证明定理19.4.  
4. 证明： $(X_{1} \times \dots \times X_{n-1}) \times X_{n}$  与  $X_{1} \times \dots \times X_{n}$  同胚  
5. 定理 19.6 的陈述中, 有一个蕴涵关系对于箱拓扑也成立, 是哪一个蕴涵关系?  
6. 设  $x_{1}, x_{2}, \cdots$  是积空间  $\Pi X_{\alpha}$  的点的一个序列. 证明: 这个序列收敛到点  $x$  当且仅当对于每一个  $\alpha$ , 序列  $\pi_{\alpha}(x_{1}), \pi_{\alpha}(x_{2}), \cdots$  收敛到  $\pi_{\alpha}(x)$ . 若用箱拓扑代替积拓扑相应结论还成立吗?  
7. 设  $\mathbb{R}^{\infty}$  是  $\mathbb{R}^{\omega}$  中所有“终端为0”的序列(即，使得仅有有限多个  $i$  ，  $x_{i}\neq 0)$  的所有序列  $(x_{1},x_{2},\dots)$  的子集.在箱拓扑与积拓扑下，  $\mathbb{R}^{\infty}$  在  $\mathbb{R}^{\omega}$  中的闭包是什么？验证你的结论.  
8. 给定实数序列  $(a_{1}, a_{2}, \cdots)$  和  $(b_{1}, b_{2}, \cdots)$ ，其中对于所有的  $i$ ， $a_{i} > 0$ ，用

$$
h \left(\left(x _ {1}, x _ {2}, \dots\right)\right) = \left(a _ {1} x _ {1} + b _ {1}, a _ {2} x _ {2} + b _ {2}, \dots\right)
$$

定义一个函数  $h: \mathbb{R}^{\omega} \to \mathbb{R}^{\omega}$ 。证明：若赋予  $\mathbb{R}^{\omega}$  积拓扑，则  $h$  是  $\mathbb{R}^{\omega}$  的一个自同胚。若赋予  $\mathbb{R}^{\omega}$  箱拓扑，结论会怎样？

9. 证明选择公理等价于以下条件：对于每一由非空集合组成的加标集族  $\{A_{\alpha}\}_{\alpha \in J}, J \neq \emptyset^{(1)}$ ，其笛卡儿积

$$
\prod_ {a \in J} A _ {a}
$$

非空.

10. 设  $A$  是一个集合， $\{X_{\alpha}\}_{\alpha \in J}$  是空间的一个加标族， $\{f_{\alpha}\}_{\alpha \in J}$  是函数  $f_{\alpha}: A \to X_{\alpha}$  的一个加标族.

(a)证明：  $A$  有唯一的一个使得每一个  $f_{a}$  都连续的最粗拓扑  $\mathcal{T}$

(b)设

$$
\mathcal {S} _ {\beta} = \left\{f _ {\beta} ^ {- 1} \left(U _ {\beta}\right) \mid U _ {\beta} \text {在} X _ {\beta} \text {中 是 开 的} \right\},
$$

并且  $\mathcal{S} = \bigcup \mathcal{S}_{\beta}$  证明：  $\mathcal{S}$  是  $\mathcal{T}$  的一个子基

(c)证明：映射  $g:Y\to A$  关于  $\mathcal{T}$  连续当且仅当每一个映射  $f_{\alpha}\circ g$  都连续.

(d) 用

$$
f (a) = \left(f _ {\alpha} (a)\right) _ {\alpha \in J}
$$

定义映射  $f: A \to \Pi X_{\alpha}$ . 设  $Z$  表示积空间  $\Pi X_{\alpha}$  的子空间  $f(A)$ . 证明  $\mathcal{T}$  中每一个元素在  $f$  下的像是  $Z$  中的一个开集.
# 第10节 商拓扑
## 10-1 商映射

商拓扑与本章中研究过的几种拓扑不同，它并不是分析中讨论过的某些东西的自然推广。尽管如此，得到它也并不困难，一个办法就是从几何上引入，我们常常采用“切割与黏合”的手段来做出诸如曲面这样的几何对象。例如，环面(轮胎的表面)可以通过适当地“黏合”矩形的对边而得到
<img src ="0547a650c7200da0148e008fad77f3e7e63b96438e1af8a97bb68a443141c29a.jpg" width = 400>
球面(球体的表面)可以通过把圆盘的整个边界捏成一点做出来
<img src = "4712a53fb0dcf64c993dedbf3b9bc51f457255973fe56a7387c0fbef25d2340d.jpg" width = 200>
将这些做法正式写出来，就包含了商拓扑的概念

> [!商映射]
> $X$  和  $Y$  都是拓扑空间， $p: X \to Y$  是一个满射。如果  $U\subseteq Y$ 是  $Y$  的开集$\iff p^{-1}(U)$  是  $X$  的一个开集，则称  $p$  是一个**商映射(quotient map)**

> [!warning] RMK
> 这个条件比连续性强，有的数学家称之为“强连续性”

> [!quote] PROP
> $p$ 是一商映射$\iff$   $A\subseteq Y$ 是  $Y$ 的闭集当且仅当  $p^{-1}(A)$  是  $X$  中的闭集

since$$f ^ {- 1} (Y - B) = X - f ^ {- 1} (B)$$

---

描述商映射的另一个方法是

> [!NOTE] 饱和的(saturated)，饱和集
> $X$  的一个子集  $C$  称为(关于满映射  $p:X\to Y)$  是**饱和的(saturated)**，若 $C$ 包含每一个与之相交的  $p^{-1}(\{y\})$  
> 或称 $C$ **饱和集**，若 $C = p^{-1}(p(C))$ 

> [!quote] PROP
> $p$ 是一商映射$\iff$ $p$ cont，且 $p$ 将 $X$ 的饱和开集映成 $Y$ 的开集( $p$ 将 $X$ 的饱和闭集映成 $Y$ 的闭集)

两种特殊的商映射是开映射和闭映射
以前说过，一个映射  $f: X \to Y$  称为
开映射(open map)，若对  $X$  中每一个开集  $U$ ， $f(U)$  是  $Y$  中的开集
闭映射(closed map)，若对  $X$  的每一个闭集  $A$ ， $f(A)$  是  $Y$  中的闭集

> [!quote] PROP
> $p: X \to Y$  是满的连续开映射或满的连续闭映射$\Rightarrow p$ 是一商映射

由定义得

---

此外存在既不是开映射又不是闭映射的商映射（见习题3）

例1 设 $X$ 是  $\mathbb{R}$  的子空间$[0，1]U[2，3]$，  $Y$  是  $\mathbb{R}$  的子空间$[0，2]$ 由下式
$$p (x) = \left\{ \begin{array}{l l} x, &x \in [ 0, 1 ]\\ x - 1, &x \in [ 2, 3 ] \end{array} \right.$$
定义的映射  $p: X \to Y$  是连续的满的闭映射，但它不是开映射。因为  $X$  中开集  $[0, 1]$  的像不是  $Y$  中的开集

注意，若取  $X$  的子集  $A$  为  $[0,1) \cup [2,3]$ ，则由  $p$  的限制所得的映射  $q: A \to Y$  是一个连续的满射，但它不是商映射。这是由于$[2，3]$是一个开集并且相对于  $q$  而言是一个饱和集，但它的像不是  $Y$  的开集。
例2设  $\pi_1$  ：  $\mathbb{R}\times \mathbb{R}\to \mathbb{R}$  为到第一个坐标空间的投射，  $\pi_1$  是一个连续的满射．此外  $\pi_1$  也是一个开映射．事实上，若  $U\times V$  是  $\mathbb{R}\times \mathbb{R}$  的一个基元素，则  $\pi_1(U\times V) = U$  是  $\mathbb{R}$  的一个开集.于是得到，  $\pi_1$  将  $\mathbb{R}\times \mathbb{R}$  的开集映为  $\mathbb{R}$  的开集．但是  $\pi_1$  不是一个闭映射．例如，  $\mathbb{R}$  的子集

$$
C = \{x \times y \mid x y = 1 \}
$$

是一个闭集，但是  $\pi_1(C) = \mathbb{R} - \{0\}$  不是  $\mathbb{R}$  的闭集
## 10-2 商拓扑

下面我们来说明如何用一个商映射来构造一个集合上的拓扑
> [!NOTE] 商拓扑(quotient topology)
> 设 $X$ 是一个空间，$A$ 是一个集合。 $p: X \to A$  是一个满射，则  $A$  上恰好存在一个拓扑  $\mathcal{T}$ ，使  $p$  为商映射。 $\mathcal{T}$  称为由  $p$  导出的**商拓扑(quotient topology)**

显然这个拓扑  $\mathcal{T}$  由  $A$  中那些子集  $U$  组成，这些  $U$  满足条件： $p^{-1}(U)$  在  $X$  中是开的
易验证 $\mathcal{T}$ 是一个拓扑．因为  $p^{-1}(\varnothing) = \varnothing$  ， $p^{-1}(A) = X$  ，所以  $\varnothing$  与  $A$  是开集．拓扑的另外两个条件可由下式推出$$p ^ {- 1} \left(\bigcup_ {\alpha \in J} U _ {\alpha}\right) = \bigcup_ {\alpha \in J} p ^ {- 1} \left(U _ {\alpha}\right)$$$$p ^ {- 1} \left(\bigcap_ {i = 1} ^ {n} U _ {i}\right) = \bigcap_ {i = 1} ^ {n} p ^ {- 1} \left(U _ {i}\right)$$

> [!quote] EX
>  $p (x) = \left\{ \begin{array}{l l} a &x > 0\\ b &x <   0 \\ c &x = 0 \end{array} \right.$ 定义的从实直线  $\mathbb{R}$  到三点集 $A = \{a, b, c\}$ 的映射所导出的 $A$ 的商拓扑
> 
> <img src="d0894d7f7ce0f703b26291262777b9efa05716ecf6834d31c9c7eab07a92e5b8.jpg" width=250>  
> 

有一种经常要用到商拓扑的特殊情形如下
> [!quote] 商拓扑下的商空间(quotient space)
> $X$ 是一拓扑空间， $X^{*}$  是  $X$  的一个分拆，其成员是  $X$  的两两无交的子集并且其成员的并为  $X$ 。设  $p: X \to X^{*}$  是一个满射，其定义是将  $X$  的每一点映到  $X^{*}$  中包含这个点的唯一的一个元素。在用  $p$  诱导出的商拓扑下，空间  $X^{*}$  称为  $X$  的一个**商空间(quotient space)**

当给定了  $X^{*}$ ，就有了一个  $X$  上的等价关系，其等价类为  $X^{*}$  的元素。人们可以把  $X^{*}$  设想成“将每一个等价类中的所有元素黏合成一点”而得到的。因此，商空间  $X^{*}$  也常称为  $X$  的“黏合空间”或者“分解空间”
可以用另一种方式来描述  $X^{*}$  的拓扑． $X^{*}$  的一个子集  $U$  是一个等价类的集合， $p^{-1}(U)$  恰好是属于  $U$  的等价类的并．因此  $X^{*}$  中的典型开集是一个等价类的族，它的并是  $X$  中的开集
例4 设  $X$  为  $\mathbb{R}^2$  中的闭单位球：
$$\{x \times y \mid x ^ {2} + y ^ {2} \leqslant 1 \}$$
设  $X^{*}$  为  $X$  的一个分拆，它由所有满足  $x^{2} + y^{2} < 1$  的单点集  $\{x \times y\}$ ，以及集合  $S^{1} = \{x \times y \mid x^{2} + y^{2} = 1\}$  组成。 $X$  中典型饱和开集如图22.4中的阴影部分所示。可以证明： $X^{*}$  同胚于  $\mathbb{R}^{3}$  的一个叫做2-维单位球面(unit 2-sphere)的子空间，定义为
![](27038ad7b99d8a25efbb94d125894ad3366c48b28a435eda6e0c7d083cdf3d08.jpg)  
图22.4
$$S ^ {2} = \{(x, y, z) \mid x ^ {2} + y ^ {2} + z ^ {2} = 1 \}$$
例5设  $X$  为矩形  $[0,1]\times [0,1]$  ，定义  $X$  的一个分拆  $X^{*}$  为：由所有单点集  $\{x\times y\}$  （其中  $0 < x < 1$  ，  $0 < y < 1)$  、以下类型的两点集$$\{x \times 0, x \times 1 \}, \quad 0 <   x <   1$$$$\{0 \times y, 1 \times y \}, \quad 0 < y <1$$
和四点集$$\{0 \times 0, 0 \times 1, 1 \times 0, 1 \times 1 \}$$

组成。 $X$ 中形如  $p^{-1}(U)$  的几个典型饱和开集如图22.5中的阴影部分所示．其中每一个都是  $X$  的开集，并且等于等价类的并
![](6461fe8f26a26a02ac86a740ea5cc0a22cf22584bf9367cd75a2614cd8dd1701.jpg)  
图22.5
这些集合中的每一个在  $p$  下的像都是  $X^{*}$  的开集，如图22.6所示．对于  $X^{*}$  的这种描述法，恰好就是用图示说明黏合矩形的边组成环面的一种数学表达

![](c23754a1997755ead479184791dbcd03af11c5911ba5cb8221833a7a1640df4d.jpg)  
图 22.6

现在研究一下商拓扑和商空间这两个概念与以前引进的一些概念之间的关系。值得注意的是，这关系不像我们所希望的那样简单
我们已经发觉子空间的性质不够理想：若  $p: X \to Y$  是一个商映射， $A$  是  $X$  的一个子空间，则由限制  $p$  的定义域及值域而得到的映射  $q: A \to p(A)$  就不一定还是商映射。然而，我们有以下定理

> [!quote] THM
> $p: X \to Y$  是一个商映射,  $A$  是  $X$  的一个子空间, 相对于  $p$  饱和,  $q: A \to p(A)$  是  $p$  的限制
> (1) 若  $A$  是  $X$  的一个开集或闭集，则  $q$  是一个商映射
> $(2)$  若  $p$  是一个开映射或闭映射，则  $q$  是一个商映射

第一步．我们首先验证以下两个等式：
$q^{-1}(V) = p^{-1}(V)$  如果  $V\subset p(A)$
$p(U \cap A) = p(U) \cap p(A)$  如果  $U \subset X$
为验证第一个等式，注意由于  $V \subset p(A)$  和  $A$  都是饱和集， $p^{-1}(V)$  包含于  $A$ 。因此  $p^{-1}(V)$  和  $q^{-1}(V)$  都等于  $A$  中经  $p$  映入  $V$  的点的集合。为验证第二个等式，注意对于  $X$  的任何子集  $U$  和  $A$ ，有以下包含关系$$p (U \cap A) \subset p (U) \cap p (A)$$
为了证明相反的包含关系，设  $y = p(u) = p(a)$ ，其中  $u \in U$  且  $a \in A$ 。因为  $A$  是一个饱和集， $A$  包含集合  $p^{-1}(p(a))$ ，因此  $A$  包含点  $u$ 。所以对  $u \in U \cup A$ ，有  $y = p(u)$
第二步．现假设  $A$  是一个开集或者  $\pmb{p}$  为开映射．对于  $p(A)$  的给定的子集  $V$  ，我们来证明：若  $q^{-1}(V)$  在  $A$  中是开的，则  $V$  在  $p(A)$  中是开的.

首先设  $A$  是一个开集．由于  $q^{-1}(V)$  在  $A$  中是开的，并且  $A$  在  $X$  中是开的，所以  $q^{-1}(V)$  在  $X$  中是开的．由于  $q^{-1}(V) = p^{-1}(V)$ ，而后者在  $X$  中是开的，根据  $p$  是一个商映射可见  $V$

在  $Y$  中是开的．从而，  $V$  在  $\pmb {p}(A)$  中是开的
再设  $p$  是一个开映射．由于  $q^{-1}(V) = p^{-1}(V)$  和  $q^{-1}(V)$  是  $A$  的开集，所以对于  $X$  的某一个开集  $U$  有  $p^{-1}(V) = U \cap A$ ．由于  $p$  是一个满射， $p(p^{-1}(V)) = V$ ．所以

$$
V = p \left(p ^ {- 1} (V)\right) = p (U \cap A) = p (U) \cap p (A).
$$

由于  $p$  是一个开映射，所以  $p(U)$  是  $Y$  的一个开集．因此  $V$  在  $p(A)$  中是开的
第三步．  $A$  或者  $\pmb{p}$  是闭的这种情形的证明可以通过在第二步中将“开”通通替换成“闭”而得到

---

现在我们考虑先前引入的几个概念。映射复合的性质较为理想。由 $p ^ {- 1} \left(q ^ {- 1} (U)\right) = \left(q \circ p\right) ^ {- 1} (U)$ 易验证两个商映射的复合还是一个商映射
此外，映射乘积的相关性质未如人意。两个商映射的笛卡儿积未必是一个商映射。见下面的例7。为了得到相应的结论，需要对空间或者映射附加某些条件。对于空间所附加的一种条件是“局部紧致性”的概念，以后我们将会研究它。对于映射所附加的一种条件是：两个映射  $p$  和  $q$  都是商映射。容易验证此时  $p \times q$  也是一个开映射，从而它也是一个商映射
最后，Hausdorff条件也不够理想．即便空间  $X$  是Hausdorff的，我们却没有任何理由说商空间  $X^{*}$  必须是Hausdorff的．有一个简单的条件能使得  $X^{*}$  满足  $T_{1}$  公理，这就是要求分拆 $X^{*}$  中每一元素为  $X$  的一个闭子集．保证  $X^{*}$  成为Hausdorff空间的条件难于找到．这是一个有关商空间的较为棘手的问题．我们在本书中以后将多次回到这个问题
有关商空间的研究中, 或许最为重要的问题当属构造定义在商空间上的连续函数. 现在我们就着手处理这一问题. 我们曾有过一个判别法则, 以确定一个到积空间中的映射  $f: Z \to \Pi X_{\alpha}$  的连续性. 商空间理论中与之相应的判别法则便是确定一个定义从商空间出发的映射  $f: X^{*} \to Z$  的连续性. 我们有以下定理

> [!quote] THM
> $p: X \to Y$  是一个商映射。 $Z$  是一个空间， $g: X \to Z$  是一个映射，对于每一个  $y \in Y$ ， $g$  在每一个集合  $p^{-1}(\{y\})$  上取常值。则  $g$  诱导一个映射  $f: Y \to Z$ ，满足条件： $f \circ p = g$ 。映射  $f$  是连续的当且仅当  $g$  是连续的。 $f$  是一个商映射当且仅当  $g$  是一个商映射
><img src="88186ad0c1a1aa7fb98fafee311b1be71a23e39020ac349ad22ecb92ec397c89.jpg" width=100>

对于每一个  $y \in Y$ ，集合  $g(p^{-1}(\{y\}))$  是  $Z$  中的一个单点集（因为  $g$  在  $p^{-1}(\{y\})$  上是常值）。如果用  $f(y)$  表示这个点，那么我们便定义了一个映射  $f: Y \to Z$ ，使得对于每一个  $x \in X$ ， $f(p(x)) = g(x)$ 。如果 $f$ 连续，那么  $g = f \circ p$  是连续的
反之，假定 $g$ 连续。令  $V$  是  $Z$  的一个开集，则  $g^{-1}(V)$  是  $X$  中的一个开集。然而  $g^{-1}(V) = p^{-1}(f^{-1}(V))$ ，由于  $p$  是一个商映射，所以  $f^{-1}(V)$  是  $Y$  的一个开集。因此 $f$ 连续
若 $f$ 为商映射，则  $g$  作为两个商映射的复合也是一个商映射．反之，设  $g$  为商映射．由于  $g$  是一个满射，所以  $f$  也是满的
设  $V$  是  $Z$  的一个子集，证明：如果  $f^{-1}(V)$  在  $Y$  中是开的，则  $V$  在  $Z$  中也是开的．由于  $p$  是连续的，  $p^{-1}(f^{-1}(V))$  是  $X$  中的一个开集．又由于 $p^{-1}(f^{-1}(V)) = g^{-1}(V)$  ，所以  $g^{-1}(V)$  是  $X$  的一个开集．由于 $g$ 是一个商映射，所以  $V$  在  $Z$  中是开的

推论22.3 设  $g: X \to Z$  是一个连续的满射。 $X^{*}$  为由下式

$$
X ^ {*} = \left\{g ^ {- 1} (\{z \}) \mid z \in Z \right\}
$$

定义的  $X$  的子集族. 在  $X^{*}$  上取商拓扑
(a)则由映射  $g$  诱导的映射  $f: X^{*} \to Z$  是一一的连续映射，并且  $f$  是同胚当且仅当  $g$  是商映射

![](68af240c76331dbe89d77f5f587f72aed3a73e3c6e4be196b4e5f9701577f4bd.jpg)

(b) 若  $Z$  是一个Hausdorff空间，则  $X^{*}$  也是一个Hausdorff空间
证 由前一个定理， $g$  诱导了一个连续映射  $f: X^{*} \to Z$ 。显然  $f$  是一一的。假设  $f$  是一个同胚，则  $f$  和投射  $p: X \to X^{*}$  都是商映射，从而它们的复合  $g$  也是商映射。反之，设  $g$  是一个商映射，则根据前一个定理可见  $f$  是商映射。由于  $f$  是一一的，所以  $f$  是一个同胚
设  $Z$  为Hausdorff空间．  $X^{*}$  中不同的点在  $f$  下的像是不同的．因此存在无交的邻域  $U$  和 $V$  ，于是  $f^{-1}(U)$  与  $f^{-1}(V)$  就是  $X^{*}$  中给定两点的无交的邻域
例6 设  $X$  是由线段  $[0, 1] \times \{n\}$  （其中  $n \in \mathbb{Z}_{+}$ ）之并构成的  $\mathbb{R}^2$  的那个子空间， $Z$  是由所有形如  $x \times (x / n)$  的点构成的  $\mathbb{R}^2$  的子空间，其中， $x \in [0, 1]$ ， $n \in \mathbb{Z}_{+}$ 。这时， $X$  是可数多个无交线段之并， $Z$  是有一公共端点的可数多个线段之并。参见图22.7

![](c75a438707fc7cc1e4ea8c35bb9324ad6a46540b169bbcdcea1807c2af61ade6.jpg)  
图22.7

用公式  $g(x \times n) = x \times (x / n)$  定义一个映射  $g: X \to Z$ .  $g$  是一个满射, 并且是连续的. 以  $g^{-1}(\{z\})$  为元素的商空间  $X^{*}$  便是将  $X$  的子集  $\{0\} \times \mathbb{Z}_{+}$  黏合成一点所得到的空间. 映射  $g$  诱导出一个一一连续映射  $f: X^{*} \to Z$ . 但  $f$  不是同胚
为验证这一事实，我们只要证明  $g$  不是商映射．考虑  $X$  中点的序列  $x_{n} = (1 / n)\times n$  由于集合  $A = \{x_{n}\}$  没有极限点，因此它是  $X$  中的一个闭集．它也是相对于  $g$  而言的一个饱和集.另一方面，由于  $g(A)$  是由所有形如  $z_{n} = (1 / n)\times (1 / n^{2})$  的点所构成，所以  $g(A)$  不是  $Z$  的闭集，原点就是它的一个极限点
例7 两个商映射的积未必还是商映射
在本节的习题中我们将给出一个涉及非Hausdorff空间的例子．我们在这里给出的例子所涉及空间都比较好
令  $X = \mathbb{R}$  ，  $X^{*}$  是将  $X$  的子集  $\mathbb{Z}_{+}$  黏合成一点  $b$  所形成的商空间．又令  $p: X \to X^{*}$  为商映射．以  $\mathbb{Q}$  表示  $\mathbb{R}$  的所有有理数构成的子空间，设  $i: \mathbb{Q} \to \mathbb{Q}$  为恒等映射．我们证明
$$
p \times i: X \times \mathbb {Q} \longrightarrow X ^ {*} \times \mathbb {Q}
$$

不是商映射
对于每一个  $n$  ，令  $c_{n} = \sqrt{2} / n$  ，并且考虑  $\mathbb{R}^2$  中所有经过点  $n \times c_{n}$  、斜率分别为1和-1的直线．设  $U_{n}$  为  $X \times \mathbb{Q}$  中位于两条直线上方或者两条直线下方并且位于两条垂线  $x = n - 1/4$  与  $x = n + 1/4$  之间的所有点的集合．则  $U_{n}$  在  $X \times \mathbb{Q}$  中是开的．由于  $c_{n}$  不是有理数， $U_{n}$  包含着集合  $\{n\} \times \mathbb{Q}$  ．参见图22.8.

![](1db1cf0c923e3e07487177301f017ca0b7e1e1f23bce7c14cd80b8c06dd82be4.jpg)  
图 22.8

令  $U$  为所有  $U_{n}$  之并，则  $U$  在  $X\times \mathbb{Q}$  中是开的．对于每一个  $q\in \mathbb{Q}$  ，由于  $U$  包含集合 $\mathbb{Z}_{+}\times \{q\}$  ，所以它是关于  $p\times i$  的一个饱和集．我们假定  $U^{\prime} = (p\times i)(U)$  在  $X^{*}\times \mathbb{Q}$  中是开的，并且由此导出矛盾
特别地，由于  $U$  包含着集合  $\mathbb{Z}_{+} \times 0$  ，所以集合  $U'$  包含点  $b \times 0$  。因此  $U'$  包含着一个开集  $W \times I_{\delta}$ ，其中  $W$  是  $b$  在  $X^{*}$  中的一个邻域， $I_{\delta}$  由使得  $|y| < \delta$  成立的所有有理数  $y$  组成。这时便有 $\mathbf {p} ^ {- 1} (W) \times I _ {\delta} \subset U$
选取充分大的  $n$  使得  $c_{n} < \delta$ . 由于  $p^{-1}(W)$  在  $X$  中是开的并且包含着  $Z_{+}$ , 我们可以选取  $\varepsilon < 1 / 4$  使得区间  $(n - \varepsilon, n + \varepsilon)$  包含于  $p^{-1}(W)$ . 那么  $U$  便包含着  $X \times \mathbb{Q}$  的子集  $V = (n - \varepsilon, n + \varepsilon) \times I_{\delta}$ . 然而图形清晰地显示出:  $V$  的许多点  $x \times y$  不在  $U$  中! (这些点之一便是  $x \times y$ , 其中  $x = n + \frac{1}{2} \varepsilon$ ,$y$  为满足  $\left| y - c_{n} \right| < \frac{1}{2} \varepsilon$  的某一个有理数.)
## 习题

1. 详细验证例3.

2. (a) 设  $p: X \to Y$  是一个连续映射。证明：若存在一个连续映射  $f: Y \to X$  使得  $p \circ f$  等于  $Y$  上的恒等映射，则  $p$  为商映射。  
(b) 如果  $A \subset X$ ,  $X$  到  $A$  上的一个收缩(retraction)是一个连续映射  $r: X \to A$ , 并满足条件: 对于每一个  $a \in A$ ,  $r(a) = a$ . 证明: 收缩是一个商映射.

3. 设  $\pi_1: \mathbb{R} \times \mathbb{R} \rightarrow \mathbb{R}$  是到第一个坐标空间的投射。令  $A$  是由所有满足条件或者  $x \geqslant 0$  或者  $y = 0$  （或者二者同时成立）的点  $x \times y$  所构成的  $\mathbb{R} \times \mathbb{R}$  的那个子空间。 $q: A \rightarrow \mathbb{R}$  是  $\pi_1$  的限制。证明： $q$  是非开非闭的商映射。

4. (a) 在平面  $X = \mathbb{R}^2$  中定义等价关系如下：

$$
x _ {0} \times y _ {0} \sim x _ {1} \times y _ {1} \quad {\text {如 果}}   x _ {0} + y _ {0} ^ {2} = x _ {1} + y _ {1} ^ {2}.
$$

令  $X^{*}$  为相应的商空间，则  $X^{*}$  同胚于一个你所熟悉的空间，它是什么空间？[提示：令 $g(x\times y) = x + y^2$  .]

(b)对于等价关系

$$
x _ {0} \times y _ {0} \sim x _ {1} \times y _ {1} \quad {\text {如 果}}   x _ {0} ^ {2} + y _ {0} ^ {2} = x _ {1} ^ {2} + y _ {1} ^ {2},
$$

讨论(a)小题中的问题

5. 设  $p: X \to Y$  是一个开映射。证明：若  $A$  为  $X$  的一个开集，则  $p$  的限制  $q: A \to p(A)$  为开映射。  
6. 设  $\mathbb{R}_K$  表示具有  $K$  - 拓扑的实直线(见第13节). 令  $Y$  是将集合  $K$  黏合成一点所得到的  $\mathbb{R}_K$  的商空间,  $p: \mathbb{R}_K \to Y$  为商映射.

(a) 证明  $Y$  满足  $T_{1}$  公理，但不是一个Hausdorff空间.  
(b) 证明  $p \times p: \mathbb{R}_K \times \mathbb{R}_K \to Y \times Y$  不是商映射. [提示: 对角线不是  $Y \times Y$  的闭集, 但它的原像在  $\mathbb{R}_K \times \mathbb{R}_K$  中是闭的.]

## 附加习题：拓扑群

在这些习题中，我们研究拓扑群及其某些性质。商拓扑的名称便是由构造拓扑群关于其子群的商群而来。

拓扑群(topological group)  $G$  既是一个群又是一个满足  $T_{1}$  公理的拓扑空间，并且将  $x \times y$  映为  $x \cdot y$  的从  $G \times G$  到  $G$  的映射以及将  $x$  映为  $x^{-1}$  的从  $G$  到  $G$  的映射都是连续的．在下面的题目中，用  $G$  表示拓扑群.

1. 设  $H$  是一个群，同时也是一个满足  $T_{1}$  公理的拓扑空间．证明： $H$  是一个拓扑群当且仅当将  $x \times y$  映成  $x \cdot y^{-1}$  的从  $H \times H$  到  $H$  的映射是连续的.  
2. 证明以下都是拓扑群：

(a)  $(\mathbb{Z}, +)$ .

(b)  $(\mathbb{R}, +)$ .  
(c)  $(\mathbb{R}_{+},\bullet)$  
(d)  $(S^1, \cdot)$ ，其中  $S^1$  是使得  $|z| = 1$  的所有复数  $z$  组成的空间.  
(e) 在矩阵乘法运算下的一般线性群  $GL(n)$ .  $(GL(n)$  是所有非蜕化  $n \times n$  阶矩阵的集合, 其拓扑是作为  $n^2$  维欧氏空间的子集按显然的方式给出的.)

3. 设  $H$  是  $G$  的一个子空间。证明：如果  $H$  又是  $G$  的一个子群，那么  $H$  和  $\overline{H}$  两者都是拓扑群。

4. 设  $\alpha$  是  $G$  的一个元素．证明：用

$$
f _ {\alpha} (x) = \alpha \cdot x \quad \text {以 及} \quad g _ {\alpha} (x) = x \cdot \alpha
$$

定义的映射  $f_{\alpha}$  ，  $g_{\alpha}\colon G\to G$  是  $G$  的一个同胚．证明  $G$  是一个齐性空间．（即对于  $G$  的任意两个点  $\pmb{x}$  和  $_y$  ，存在一个从  $G$  到  $G$  上的同胚将  $\pmb{x}$  映成  $_{y}$  ）

5. 设  $H$  是  $G$  的一个子群。若  $x \in G$ ，定义  $xH = \{x \cdot h \mid h \in H\}$ ，称之为  $H$  在  $G$  中的一个左陪集(left coset)。设  $G / H$  表示  $G$  中  $H$  的左陪集族，它是  $G$  的一个分拆。在  $G / H$  上赋予商拓扑。

(a) 证明：若  $\alpha \in G$ ，前一题中的映射  $f_{\alpha}$  诱导出  $G / H$  的一个同胚，它将  $xH$  映为  $(\alpha \cdot x)H$ 。证明  $G / H$  是一个齐性空间。  
(b) 证明：若  $H$  关于  $G$  的拓扑是一个闭集，则单点集在  $G / H$  中都是闭的.  
(c) 证明：商映射  $p: G \to G / H$  是开的。  
(d)证明：若  $H$  关于  $G$  的拓扑是一个闭集，并且是  $G$  的一个正规子群，则  $G / H$  是拓扑群.

6. 整数集  $\mathbb{Z}$  是  $(\mathbb{R}, +)$  的正规子群。商  $\mathbb{R} / \mathbb{Z}$  是一个你所熟悉的拓扑群，它是哪个拓扑群？

7. 若  $A$  和  $B$  都是  $G$  的子集，用  $A \cdot B$  表示所有点  $a \cdot b$  的集合，其中  $a \in A, b \in B$ 。用  $A^{-1}$  表示所有点  $a^{-1}$  的集合，其中  $a \in A$ 。

(a) 单位元  $e$  的一个邻域  $V$  称为对称的 (symmetric)，若  $V = V^{-1}$ 。若  $U$  为  $e$  的一个邻域，证明：存在一个  $e$  的对称邻域  $V$ ，使得  $V \cdot V \subset U$ 。[提示：若  $W$  为  $e$  的一个邻域，则  $W \cdot W^{-1}$  便是对称的。]  
(b) 证明  $G$  是一个Hausdorff空间．事实上，只要证明：若  $x \neq y$  ，则存在  $e$  的邻域  $V$  ，使得  $V \cdot x$  与  $V \cdot y$  无交.  
(c) 证明:  $G$  满足以下称为正则性公理(regularity axiom)的分离公理: 对于任意给定的闭子集  $A$  和  $A'$  外的一个点  $x$ , 存在分别包含  $A$  和  $x$  的无交的两个开集. [提示: 存在  $e$  的一个邻域  $V$ , 使得  $V \cdot x$  与  $V \cdot A$  无交.  
(d) 设  $H$  是  $G$  的一个子群并且关于  $G$  的拓扑是闭的。 $p: G \to G / H$  为商映射。证明  $G / H$  满足正则性公理。[提示：当  $A$  为饱和集时，考察(c)小题的证明。]

