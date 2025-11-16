# 第31节 完备度量空间
## 31-1  完备度量空间
度量空间的完备性概念，读者可能早就知道了，它是分析学各方面的基础。虽然完备性只是一种度量性质，而非拓扑性质，但仍然有许多涉及完备度量空间的定理具有拓扑的色彩。本章中，我们将研究一些重要的完备度量空间，并且证明若干相关的定理。

完备度量空间的最常见的例子是通常度量下的欧氏空间．另一个重要例子是把一个空间  $X$  映入一个度量空间  $Y$  的所有连续函数构成的集合  $\mathcal{C}(X,Y)$  ．这个集合上有一个度量称之为一致度量，它和第20节中给  $\mathbb{R}^J$  定义的那种一致度量类似．如果  $Y$  是一个完备度量空间，那么 $\mathcal{C}(X,Y)$  在一致度量下也是完备的．这一点我们将在第43节中予以证明．作为一个应用，我们在第44节中构造了著名的充满空间的Peano曲线.

涉及完备度量空间的拓扑特性的定理之一便是关于空间的紧致性与完备性关系的定理，我们在第45节中证明它。这个定理的一个直接的推论是函数空间  $\mathcal{C}(X,\mathbb{R}^n)$  中关于紧致子空间的一个定理，这就是著名的Ascoli定理的一种经典形式。

在函数空间  $\mathcal{C}(X, Y)$  上，除了由一致度量所诱导的拓扑之外，还有其他有用的拓扑。在第46节中，我们将对其中的某些拓扑予以研究，并在第47节中证明Ascoli定理的一般形式。

这一节我们定义完备性的概念，并且证明若 $Y$ 是完备度量空间，则函数空间  $\mathcal{C}(X, Y)$  在一致度量下也是完备的。此外还要证明每一个度量空间能被等距地嵌入到一个完备度量空间中。

> [!NOTE] Cauchy 序列 (Cauchy sequence)
> $(X, d)$  为度量空间。 $X$  的点的序列  $\left(x_{n}\right)$  称为  $(X, d)$  中的一个 **Cauchy 序列 (Cauchy sequence)**，若任意给定  $\varepsilon > 0$ ，存在一个整数  $N$ ，使得 $\forall n,m\ge N$ 
> $$d \left(x _ {n}, x _ {m}\right) <   \varepsilon$$

> [!NOTE] 完备(complete)度量空间
> 度量空间  $(X,d)$  称为**完备的(complete)**，若  $X$  中的每一个Cauchy序列收敛

当然，  $X$  中任何一个收敛序列必定是一个Cauchy列，完备性是要求其逆命题也成立

注意，完备度量空间 $(X, d)$ 的闭子集 $A$，在限制度量下必定是完备的．因为 $A$ 中Cauchy列也是 $X$ 中的Cauchy列，所以在 $X$ 中收敛；又因为 $A$ 是 $X$ 的闭子集，所以其极限必定在 $A$ 中

另外，如果 $X$ 关于度量 $d$ 是完备的，那么 $X$ 在相应于 $d$ 的标准有界度量 $\bar {d} (x, y) = \min  \{d (x, y), 1 \}$ 下也是完备的，反之也对。因为一个序列  $(x_{n})$  对于 $\bar{d}$ 是Cauchy列当且仅当它对 $d$ 是Cauchy列，并且一个序列对 $\bar{d}$ 收敛当且仅当它对 $d$ 收敛

以下引理是可以用来判别度量空间是否完备的一个有用的准则

> [!quote] 引理
> 如果度量空间  $X$  中每一个Cauchy序列有一个收敛的子序列，那么  $X$  是完备的

证 设  $(x_{n})$  是  $(X, d)$  中的一个 Cauchy 序列。我们证明，如果  $(x_{n})$  有一个子序列  $\left(x_{n_{i}}\right)$  收敛于一点  $x$ ，则序列  $(x_{n})$  本身也收敛于  $x$ 。

给定  $\varepsilon > 0$ ，首先选取足够大的  $N$ ，使得对于所有的  $n, m \geq N$ ，有$$d \left(x _ {n}, x _ {m}\right) <\frac{\varepsilon}{2}$$
（因为  $(x_{n})$  是一个Cauchy序列)然后选取足够大的整数 $i$，使 $n_i\geqslant N$ 并且
$$d \left(x _ {n _ {i}}, x\right) <\frac{\varepsilon}{2}$$

（因为  $n_1 < n_2 < \cdots$  是一个递增的整数序列，并且  $(x_{n_i})$  收敛于  $x$ .）综合上述事实，就可以得到所要证的结果：对于  $n \geqslant N$ ，
$$d \left(x _ {n}, x\right) \leqslant d \left(x _ {n}, x _ {n _ {i}}\right) + d \left(x _ {n _ {i}}, x\right) <   \varepsilon$$

---

> [!quote] 定理
> 对于通常度量，即欧氏度量 $d$ 和平方度量 $\rho$，欧氏空间 $\mathbb{R}^k$ 都是完备的

为证明度量空间 $(\mathbb{R}^k,\rho)$ 是完备的，令 $(x_{n})$ 为 $(\mathbb{R}^k,\rho)$ 中的一个Cauchy序列．集合 $\{x_{n}\}$  是  $(\mathbb{R}^k,\rho)$  的有界子集．因为如果选择  $N$  ，使得对于所有的  $n,m\geqslant N$，$\rho \left(x _ {n}, x _ {m}\right) \leqslant 1$，那么数$$M = \max  \left\{\rho \left(x _ {1}, \mathbf {0}\right), \dots , \rho \left(x _ {N - 1}, \mathbf {0}\right), \rho \left(x _ {N}, \mathbf {0}\right) + 1 \right\}$$
是 $\rho(x_{n}, \mathbf{0})$ 的一个上界。于是，序列  $(x_{n})$  中的点都在立方体  $[-M, M]^{k}$  中。因为这个立方体是紧致的，根据定理28.2，序列  $(x_{n})$  有一个收敛子序列，于是  $(\mathbb{R}^{k}, \rho)$  是完备的

为了证明  $(\mathbb{R}^k, d)$  是完备的，注意一个序列关于  $d$  是 Cauchy 序列当且仅当它关于  $\rho$  是 Cauchy 序列，并且一个序列相对于  $d$  收敛当且仅当它相对于  $\rho$  收敛

---

现在我们来处理积空间  $\mathbb{R}^n$  的问题．为此我们需要下面这个关于积空间中的序列的引理

> [!quote] 引理
> $X = \Pi X_{\alpha}$  是积空间， $x_{n}$  是  $X$  的一个点的序列，则  $x_{n} \to x$  当且仅当对于每一个  $\alpha$ ， $\pi_{\alpha}(x_{n}) \to \pi_{\alpha}(x)$

这一结论曾在第19节中作为习题给出，在此我们给出它的证明。因为投射  $\pi_{\alpha}: X \to X_{\alpha}$  是连续的，所以收敛序列像还是收敛序列，所以命题的“必要性”成立。下面来证明充分性。设对于每一个  $\alpha \in J$ ，有  $\pi_{\alpha}(x_n) \to \pi_{\alpha}(x)$ 。设  $U = \Pi U_{\alpha}$  是  $X$  的包含  $x$  的一个基元素。对于  $\alpha$ ，如果  $U_{\alpha}$  不等于整个空间  $X_{\alpha}$ ，选取  $N_{\alpha}$  使得当  $n \geqslant N_{\alpha}$  时  $\pi_{\alpha}(x_n) \in U_{\alpha}$ 。设  $N$  是  $N_{\alpha}$  中最大的，那么当  $n \geqslant N$  时  $x_n \in U$

---

> [!quote] 定理
> 对积空间  $\mathbb{R}^n$，总存在一个度量，使得相对这个度量而言  $\mathbb{R}^n$  是完备的

设  $\bar{d} (a,b) = \min \{|a - b|,1\}$  是  $\mathbb{R}$  的标准有界度量．设  $D$  是  $\mathbb{R}^{\infty}$  的一个度量，定义为
$$D (\boldsymbol {x}, \boldsymbol {y}) = \sup  \left\{\frac{\bar {d} (x _ {i}, y _ {i})}{i} \right\}$$
那么  $D$  诱导了  $\mathbb{R}^{\omega}$  的积拓扑．下面将证明  $\mathbb{R}^{\omega}$  关于  $D$  是完备的．设  $\pmb{x}_{n}$  是  $(\mathbb{R}^{\omega}, D)$  的一个Cauchy序列．由于

$$
\bar {d} \left(\pi_ {i} (\boldsymbol {x}), \pi_ {i} (\boldsymbol {y})\right) \leqslant i D (\boldsymbol {x}, \boldsymbol {y}),
$$

对于固定的  $i$  ，序列  $\pi_i(x_n)$  是  $\mathbb{R}$  中的一个Cauchy序列，因此它收敛，不妨设其收敛于  $a_{i}$  ．于是

序列  $\pmb{x}_{n}$  收敛到  $\mathbb{R}^{\infty}$  中的点  $\pmb {a} = \{a_{1},a_{2},\dots \}$

例1 一个非完备的度量空间的例子就是关于通常度量  $d(x, y) = |x - y|$  的有理数空间  $\mathbb{Q}$ . 例如，（在  $\mathbb{R}$  中）收敛于  $\sqrt{2}$  的有限小数序列

$$
1. 4, 1. 4 1, 1. 4 1 4, 1. 4 1 4 2, 1. 4 1 4 2 1, \dots
$$

是  $\mathbb{Q}$  中的一个Cauchy序列，但(在  $\mathbb{Q}$  中)不收敛.

例2另一个非完备的空间是关于度量  $d(x,y) = |x - y|$  的  $\mathbb{R}$  中的开区间（-1，1）．在这个空间中，定义为

$$
x _ {n} = 1 - 1 / n
$$

的序列  $(x_{n})$  是一个Cauchy序列，但不收敛．这个例子表明，完备性不是拓扑性质．也就是说，它不是在同胚下保持不变的性质．因为(-1，1)同胚于实直线R，而R在通常度量下是完备的.

虽然积空间  $\mathbb{R}^n$  和  $\mathbb{R}^m$  都有度量使之成为完备空间，但对于积空间  $\mathbb{R}^J$  来说，未必能有这样的结果．因为如果  $J$  不可数，则  $\mathbb{R}^J$  甚至不能度量化(见第21节)．但是，在集合  $\mathbb{R}^J$  上存在不同的拓扑，其一便是由一致度量诱导的．我们将看到，在这一度量下， $\mathbb{R}^J$  是完备的.

我们定义一致度量如下：

定义 设  $(Y, d)$  是一个度量空间， $\overline{d}(a, b) = \min \{d(a, b), 1\}$  是  $Y$  上相应于  $d$  的标准有界度量。若  $x = (x_{a})_{a \in J}$  与  $y = (y_{a})_{a \in J}$  是笛卡儿积  $Y^{j}$  的两个点，令

$$
\bar {\rho} (x, y) = \sup  \left\{\bar {d} \left(x _ {\alpha}, y _ {\alpha}\right) \mid \alpha \in J \right\}.
$$

容易验证， $\bar{\rho}$  是一个度量①．称其为  $Y^{J}$  的相应于  $Y$  的度量  $d$  的一致度量（uniform metric).

我们在这里对  $Y^{J}$  中的元素使用了标准“串”记号。因为  $Y^{J}$  中的元素是从  $J$  到  $Y$  的函数，我们也可以使用函数记号表示它们。在这一章中，函数记号会比串记号更方便些，因此我们全部使用函数记号。在此定义中一致度量的定义具有以下形式：若  $f, g: J \to Y$ ，则

$$
\bar {\rho} (f, g) = \sup  \{\bar {d} (f (\alpha), g (\alpha)) \mid \alpha \in J \}.
$$

定理43.5如果空间  $Y$  关于度量  $\pmb{d}$  是完备的，则空间  $Y^{j}$  在相应于  $\pmb{d}$  的一致度量  $\bar{\rho}$  下也是完备的.

证 我们曾经说过，如果  $(Y, d)$  是完备的，那么  $(Y, \overline{d})$  也是完备的，其中  $\overline{d}$  是相应于  $d$  的有界度量。现在假定  $f_{1}, f_{2}, \cdots$  是  $Y^{J}$  中点的一个序列，它相对于  $\bar{\rho}$  是一个Cauchy序列。给定  $\alpha \in J$ ，对于所有  $m$  和  $n$  有

$$
\bar {d} \left(f _ {n} (\alpha), f _ {m} (\alpha)\right) \leqslant \bar {\rho} \left(f _ {n}, f _ {m}\right),
$$

这说明  $f_{1}(\alpha), f_{2}(\alpha), \cdots$  是  $(Y, \bar{d})$  中的一个Cauchy序列．因此，这个序列收敛，设它收敛于点  $y_{\alpha}$  ．设函数  $f: J \to Y$  定义为  $f(\alpha) = y_{\alpha}$  ，我们断言：序列  $(f_{n})$  关于度量  $\bar{\rho}$  收敛于  $f$

给定  $\epsilon > 0$ ，首先选取充分大的  $N$ ，使得  $\bar{\rho}(f_n, f_m) < \epsilon / 2$ ，其中  $n, m \geq N$ 。于是，特别是对于  $n, m \geq N$  及  $\alpha \in J$ ，

$$
\bar {d} \left(f _ {n} (\alpha), f _ {m} (\alpha)\right) <   \varepsilon / 2.
$$

固定  $n$  和  $\alpha$  ，让  $m$  变得任意大，则只要  $n\geqslant N$  ，对任意  $\alpha \in J$  有

$$
\bar {d} \left(f _ {n} (\alpha), f (\alpha)\right) \leqslant \varepsilon / 2.
$$

因此，当  $n\geqslant N$  时，有

$$
\bar {\rho} (f _ {n}, f) \leqslant \varepsilon / 2 <   \varepsilon .
$$

定理证毕.

现在，我们可以考虑集合  $Y^{X}$ ，其中  $X$  是一个拓扑空间，而不单单是一个集合了。当然，这并不会对前面所作的讨论有所影响。当我们考虑所有函数  $f: X \to Y$  构成的集合时， $X$  的拓扑是无所谓的。但是，假定我们考虑的是由所有连续函数  $f: X \to Y$  构成的  $Y^{X}$  的子集  $\mathcal{C}(X, Y)$  时，就与  $X$  的拓扑有关了。这时，我们得出，若  $Y$  是完备的，则在一致度量下  $\mathcal{C}(X, Y)$  也是完备的。这一结论对于所有有界函数  $f: X \to Y$  构成的集合  $\mathcal{B}(X, Y)$  也成立。（一个函数  $f$  称为有界的（bounded），若它的像集  $f(X)$  是度量空间  $(Y, d)$  的一个有界子集。）

定理43.6 设  $X$  是一个拓扑空间， $(Y, d)$  是一个度量空间．则连续函数集  $\mathcal{C}(X, Y)$  和有界函数集  $\mathcal{B}(X, Y)$  在一致度量下都是  $Y^X$  中的闭集．因此，如果  $Y$  是完备的，那么这两个空间在一致度量下都是完备的.

证 这个定理的前半部分就是一致极限定理(定理21.6)的一个翻版．首先，我们证明，如果  $Y^{X}$  中的序列  $(f_n)$  相对于  $Y^{X}$  中的度量  $\bar{\rho}$  收敛于  $Y^{X}$  的元素  $f$  ，那么在第21节中所给的定义下相对于  $Y$  上的度量  $\bar{d}$  ，它也一致收敛于  $f$  ．因为，给定  $\varepsilon >0$  ，选取整数  $N$  ，使得对于所有  $n > N$

$$
\bar {\rho} (f, f _ {n}) <   \varepsilon .
$$

于是，对于所有  $x \in X$  及所有的  $n \geqslant N$  ，有

$$
\bar {d} (f _ {n} (x), f (x)) \leqslant \bar {\rho} (f _ {n}, f) <   \epsilon .
$$

所以  $(f_{n})$  一致收敛于  $f$

现在，我们证明  $\mathcal{C}(X, Y)$  相对于度量  $\bar{\rho}$  是  $Y^X$  的闭集。设  $f$  为  $Y^X$  的一个元素，同时也是  $\mathcal{C}(X, Y)$  的一个极限点。于是存在  $\mathcal{C}(X, Y)$  中一个元素序列  $(f_n)$  关于度量  $\bar{\rho}$  收敛于  $f$ 。根据一致极限定理， $f$  连续，所以  $f$  属于  $\mathcal{C}(X, Y)$ 。

最后，我们要证明  $\mathcal{B}(X,Y)$  是  $Y^{X}$  的一个闭集。 $f$  是  $\mathcal{B}(X,Y)$  的一个极限点，存在  $\mathcal{B}(X,Y)$  中一个元素序列  $(f_n)$  收敛于  $f$ 。选取  $N$  足够大，使得  $\bar{\rho}(f_N,f) < 1/2$ 。从而对于  $x\in X$ ，我们有  $\overline{d}(f_N(x),f(x)) < 1/2$ 。由此可见  $d(f_N(x),f(x)) < 1/2$ 。所以，如果  $f_N(X)$  的直径为  $M$ ，那么  $f(X)$  的直径最多为  $M + 1$ 。因此， $f\in \mathcal{B}(X,Y)$ 。

综上所述，我们有：若  $Y$  关于度量  $d$  是完备的，则  $\mathcal{C}(X, Y)$  和  $\mathcal{B}(X, Y)$  在度量  $\bar{\rho}$  下都是完备的.

定义 设  $(Y, d)$  是一个度量空间。可以在由  $X$  到  $Y$  的有界函数构成的集合  $\mathcal{B}(X, Y)$  上定义另一度量如下：

$$
\rho (f, g) = \sup  \left\{d (f (x), g (x)) \mid x \in X \right\}.
$$

易见  $\rho$  的定义是确切的，因为当  $f(X)$  和  $g(X)$  都有界时，集合  $f(X) \cup g(X)$  也是有界的。这个度量就被称为上确界度量（sup metric）。

在上确界度量和一致度量之间有一些简单的联系．事实上，若  $f$  ，  $g\in \mathcal{B}(X,Y)$  ，则有

$$
\bar {\rho} (f, g) = \min  \{\rho (f, g), 1 \}.
$$

因为如果  $\rho(f, g) > 1$ ，那么至少存在一点  $x_0 \in X$ ，有  $d(f(x_0), g(x_0)) > 1$ ，因此  $\overline{d}(f(x_0))$

$g(x_0)) = 1$  ，并且  $\bar{\rho} (f,g) = 1$  ，反之，如果  $\rho (f,g)\leqslant 1$  ，那么对任意  $x\in X$  ，有  $\overline{d} (f(x),$ $g(x)) = d(f(x),g(x))\leqslant 1$  ，从而  $\bar{\rho} (f,g) = \rho (f,g)$  ，因此在  $\mathcal{B}(X,Y)$  上，度量  $\bar{\rho}$  正是相对于度量  $\rho$  的标准有界度量．这就是我们引用记号  $\bar{\rho}$  表示一致度量的原因，参见第20节.

如果  $X$  是紧致的，那么每一个连续函数  $f: X \to Y$  都是有界的。因此上确界度量就定义在  $\mathcal{C}(X, Y)$  上。如果  $Y$  在度量  $d$  下是完备的，那么  $\mathcal{C}(X, Y)$  在相应的一致度量  $\bar{\rho}$  下也是完备的，因此在上确界度量  $\rho$  下也是完备的。在这种情况下，我们常使用上确界度量而不是一致度量。

现在我们要证明一个经典定理，得到的结论是：每一个度量空间都可以等距地嵌入到一个完备度量空间中．（还有一种证明方式更为直接些，参见习题9.)尽管我们并不会用到这个定理，但它在数学的其他方面很有用.

定理43.7 设  $(X, d)$  是一个度量空间．则存在一个从  $X$  到某个完备度量空间中的等距嵌入.

证 设  $\mathcal{B}(X, \mathbb{R})$  是将  $X$  映入  $\mathbb{R}$  中的所有有界函数构成的集合。令  $x_0$  为  $X$  中取定的一个点，给定  $a \in X$ ，定义  $\phi_a: X \to \mathbb{R}$  为

$$
\phi_ {a} (x) = d (x, a) - d (x, x _ {0}).
$$

我们断言  $\phi_{a}$  是有界的．因为根据不等式

$$
d (x, a) \leqslant d (x, b) + d (a, b),
$$

$$
d (x, b) \leqslant d (x, a) + d (a, b),
$$

可见

$$
\mid d (x, a) - d (x, b) \mid \leqslant d (a, b).
$$

令  $b = x_0$  ，我们得出结论，对于所有  $x\in X$  有  $\mid \phi_a(x)\mid \leqslant d(a,x_0)$

定义  $\Phi: X \to \mathcal{B}(X, \mathbb{R})$  为

$$
\Phi (a) = \phi_ {a}.
$$

我们证明  $\Phi$  是从  $(X, d)$  到完备度量空间  $(\mathcal{B}(X, \mathbb{R}), \rho)$  中的一个等距嵌入，也就是说，证明对于点的任意偶对  $a, b \in X$ ，有

$$
\rho \left(\phi_ {a}, \phi_ {b}\right) = d (a, b).
$$

根据定义

$$
\begin{array}{l} \rho \left(\phi_ {a}, \phi_ {b}\right) = \sup  \left\{\mid \phi_ {a} (x) - \phi_ {b} (x) \mid ; x \in X \right\} \\ = \sup  \left\{\mid d (x, a) - d (x, b) \mid ; x \in X \right\} \\ \end{array}
$$

可见

$$
\rho \left(\phi_ {a}, \phi_ {b}\right) \leqslant d (a, b).
$$

另一方面，这个不等式可能是不严格的 ①．因为当  $x = a$  时，有

$$
\mid d (x, a) - d (x, b) \mid = d (a, b).
$$

定义 设  $X$  是一个度量空间．如果  $h: X \to Y$  是从  $X$  到完备度量空间  $Y$  中的一个等距嵌入，则  $Y$  的子空间  $\overline{h(X)}$  是一个完备度量空间．它称为  $X$  的一个完备化（completion）.

$X$  的完备化在等距的意义上说是唯一确定的．见习题10.


## 练习


1. 设  $X$  是一个度量空间.

(a) 假定对某一个  $\varepsilon > 0$ ， $X$  中的每一个  $\varepsilon-$  球都有紧致闭包。证明  $X$  是完备的。  
(b) 假定对于每一个  $x \in X$ ，存在  $\varepsilon > 0$ ，使得球  $B(x, \varepsilon)$  有紧致闭包。举例说明， $X$  未必是完备的。

2. 设  $(X, d_X)$  和  $(Y, d_Y)$  都是度量空间， $Y$  是完备的。设  $A \subset X$ 。证明：如果  $f: A \to Y$  一致连续，则  $f$  可以唯一地扩张成一个连续函数  $g: \overline{A} \to Y$ ，并且  $g$  是一致连续的。

3.  $X$  的两个度量  $d$  和  $d'$  称为度量等价的 (metrically equivalent), 如果恒等映射  $i: (X, d) \to (X, d')$  及其逆映射都是一致连续的.

(a)证明：  $d$  度量等价于相对于  $d$  的标准有界度量  $\bar{d}$  
(b)证明：若  $d$  和  $d'$  是度量等价的，则  $X$  在度量  $d$  下是完备的，当且仅当它关于度量  $d'$  是完备的.

4. 证明：度量空间  $(X, d)$  是完备的，当且仅当对  $X$  中满足  $|A_{n}| \to 0$  的任意一个非空闭集套序列  $A_{1} \supset A_{2} \supset \cdots$ ，有  $\bigcap A_{n} \neq \emptyset$ .  
5. 设  $(X, d)$  是一个度量空间．以前说过，一个连续映射  $f: X \to X$  称为一个压缩映射，指的是如果存在一个数  $\alpha < 1$  ，使得对于所有的  $x, y \in X$  ，有

$$
d (f (x), f (y)) \leqslant \alpha d (x, y).
$$

证明：如果  $f$  是一个完备度量空间上的压缩映射，则存在唯一的一个点  $x \in X$ ，使得  $f(x) = x$ 。与第28节中的习题7比较。

6. 空间  $X$  称为拓扑完备的(topologically complete)，如果存在着诱导出  $X$  的拓扑的一个度量，使得在这一度量下  $X$  是完备的。

(a)证明：一个拓扑完备空间的闭子空间也是拓扑完备的.  
(b) 证明：拓扑完备空间的可数积空间（关于积拓扑）仍然是拓扑完备的.  
(c) 证明：拓扑完备空间的开子空间是拓扑完备的。[提示：如果  $U \subset X$ ，并且  $X$  关于度量  $d$  是完备的，定义  $\phi: U \to \mathbb{R}$  为

$$
\phi (x) = 1 / d (x, X - U).
$$

通过  $f(x) = x \times \phi(x)$  将  $U$  嵌入到  $X \times \mathbb{R}$  中.

(d)证明：如果  $A$  是拓扑完备空间中的一个  $G_{\delta}$  集，则  $A$  是拓扑完备的．[提示：设  $A$  是开集  $U_{n}$  的交，  $n\in Z_{+}$  ，考虑  $A$  到  $\Pi U_n$  的对角线嵌入  $f(a) = (a,a,\dots)$  ]证明：无理数集是拓扑完备的.

7. 证明所有使得  $\sum x_{i}^{2}$  收敛的序列  $(x_{1}, x_{2}, \cdots)$  的集合在  $\ell^{2}$ -度量下是完备的(参见第20节习题8).  
8. 设  $X$  和  $Y$  是两个空间，定义

$$
e: X \times \mathcal {C} (X, Y) \longrightarrow Y
$$

为  $e(x, f) = f(x)$ ，映射  $e$  称为一个赋值映射 (evaluation map). 证明：如果  $d$  是  $Y$  上的度量， $\mathcal{C}(X, Y)$  有相应的一致拓扑，那么  $e$  是连续的. 在第 46 节中我们将推广这一结论.

9. 设  $(X, d)$  是一个度量空间．证明：存在从  $X$  到完备度量空间  $(Y, D)$  的一个等距嵌入  $h$  如

下：令  $\widetilde{X}$  表示  $X$  中点的所有Cauchy序列

$$
\boldsymbol {x} = \left(x _ {1}, x _ {2}, \dots\right)
$$

的集合．若

$$
d \left(x _ {n}, y _ {n}\right) \longrightarrow 0.
$$

则定义  $x \sim y$ 。用  $[x]$  表示  $x$  的等价类， $Y$  表示这些等价类构成的集合。定义  $Y$  上的度量  $D$  为

$$
D ([ x ], [ y ]) = \lim  _ {n \rightarrow \infty} d (x _ {n}, y _ {n}).
$$

(a)证明：～是一个等价关系，  $D$  是一个定义确切的度量.

(b)定义  $h$  ：  $X\to Y$  为  $h(x)$  是常值序列  $(x,x,\dots)$  的等价类：

$$
h (x) = [ (x, x, \dots) ].
$$

证明  $h$  是一个等距嵌入.

(c) 证明  $h(X)$  在  $Y$  中稠密。事实上，给定  $\pmb{x} = (x_{1}, x_{2}, \dots) \in \widetilde{X}$ ，证明  $Y$  中点的序列  $h(x_{n})$  收敛于  $Y$  中的点  $[x]$ 。  
(d)证明：如果  $A$  是度量空间  $(Z,\rho)$  的一个稠密子集，并且  $A$  中任意一个Cauchy序列在  $Z$  中收敛，则  $Z$  是完备的.  
(e) 证明  $(Y, D)$  是完备的.

10. 定理（完备化的唯一性）设  $h: X \to Y$  和  $h': X \to Y'$  分别是从度量空间  $(X, d)$  到完备度量空间  $(Y, D)$  和  $(Y', D')$  的两个等距嵌入。则有一个  $(\overline{h(X)}, D)$  与  $(\overline{h'(X)}, D')$  之间的等距同构在子空间  $h(X)$  上等于  $h'h^{-1}$ 。

# 第32节 充满空间的曲线
## 32-1 充满空间的曲线

当  $Y$  是完备度量空间时， $\mathcal{C}(X, Y)$  在一致度量下是完备的。作为这一完备性的应用，我们将要构造著名的“充满空间的 Peano 曲线”。

定理44.1 设  $I = [0, 1]$ 。则存在一个连续映射  $f: I \to I^2$ ，它的像填满整个正方形  $I^2$ 。

这种道路的存在性，如同无处可微的连续函数(后面将要讲到)的存在性一样，违反了人们朴素的集合直觉.

证 第一步。我们将构造一个映射  $f$ ，使得它是一个连续函数序列  $f_{n}$  的极限。为了给出序列  $f_{n}$ ，我们首先来描述关于道路的一种特殊运算。

我们从实直线上任意闭区间  $[a, b]$  和平面上其边平行于坐标轴的任意正方形入手，考虑如图44.1所示的三角形道路  $g$ ，它是  $[a, b]$  到这个正方形的一个连续映射。我们要描述的运算就是用图44.2所示的道路  $g'$  代替道路  $g$ ，它由四条三角形道路组成，其中的每一个只有  $g$  的

![](2380e45ca480406d5fbe332208c4b49663b2f53c58bad50f70494c85de248ee0.jpg)  
图44.1

![](941da72a5884e7ead6bcdadfbe96a03fcb6532c8ba6b7c00ab13d87b49bb3947.jpg)  
图44.2

一半那么大．注意  $g$  与  $g^{\prime}$  有相同的起点和终点．如果愿意的话，你可以写出  $\pmb{g}$  和  $g^{\prime}$  的方程.

对于连接正方形两个相邻顶点的任意三角形道路，都可以施行上面所说的运算。例如，对于图44.3所示的道路  $h$ ，重复上述运算就得出道路  $h'$ 。

![](49f2f2755a95466ec694104171b008986a543299684d938730fee90b86e395d2.jpg)  
图 44.3

第二步．现在定义函数序列  $f_{n}$  ：  $I\to I^2$  ，为方便起见，第一个函数  $f_{0}$  就是图44.1所示的三角形道路，其中  $a = 0$  ，  $b = 1$  ，下一个函数  $f_{1}$  是对函数  $f_{0}$  施行第一步中所述运算而得到的函数，如图44.2所示．第三个函数  $f_{2}$  是对组成  $f_{1}$  的四条三角形道路中的每一个施行同样的运算而得出的函数，如图44.4所示.

![](4d1f37141a4b29f943cd4e8773549cfd91537db3108a2baf7fed07d335e75cd8.jpg)  
图 44.4

第四个函数  $f_{3}$  则是对组成  $f_{2}$  的十六条三角形道路中的每一个施行上述运算而得到的函数，如图44.5所示．依此类推．一般地， $f_{n}$  是由在第一步中考虑过的  $4^{n}$  条三角形道路组成的道路，其中的每一个都落在边长为  $1 / 2^{n}$  的一个正方形中．对这些三角形道路施行第一步所描述的运算，每一个用四条较小的三角形道路来代替，就得到函数  $f_{n + 1}$

![](f817ee8f490a2928726e795656028c66559210c394a62896222b54125543d62a.jpg)  
图 44.5

第三步．出于证明的需要，用  $d(x,y)$  表示  $\mathbb{R}^2$  中的平方度量，

$$
d (x, y) = \max  \left\{\mid x _ {1} - y _ {1} \mid , \mid x _ {2} - y _ {2} \mid \right\}.
$$

于是，我们令  $\rho$  表示相应的  $\mathcal{C}(I, I^2)$  上的上确界度量，

$$
\rho (f, g) = \sup  \left\{d (f (t), g (t)) \mid t \in I \right\}.
$$

因为  $I^2$  在  $\mathbb{R}^2$  中是闭集，所以它在平方度量下是完备的，于是  $\mathcal{C}(I, I^2)$  关于度量  $\rho$  是完备的.

我们断言，第二步所定义的函数序列  $(f_n)$  是度量  $\rho$  下的一个Cauchy序列．为此，我们考察从  $f_{n}$  到  $f_{n + 1}$  时会发生什么变化．构成  $f_{n}$  的每一个小三角形道路都落在边长为  $1 / 2^{n}$  的某一个正方形中．而从  $f_{n}$  得出  $f_{n + 1}$  的运算就是用同一正方形中的四条三角形道路来代替一条三角形道路．因此，在  $I^2$  的平方度量下，  $f_{n}(t)$  和  $f_{n + 1}(t)$  之间的距离最多为  $1 / 2^n$  ，于是有 $\rho (f_n,f_{n + 1})\leqslant 1 / 2^n$  ，由此推出  $(f_n)$  是一个Cauchy序列，因为对于所有的  $n$  和  $m$  ，有

$$
\rho \left(f _ {n}, f _ {n + m}\right) \leqslant 1 / 2 ^ {n} + 1 / 2 ^ {n + 1} + \dots + 1 / 2 ^ {n + m - 1} <   2 / 2 ^ {n}.
$$

第四步．因为  $\mathcal{C}(I, I^2)$  是完备的，所以序列  $f_n$  收敛于一个连续函数  $f: I \to I^2$ ．下面我们证明  $f$  是一个满射.

设  $\pmb{x}$  是  $I^2$  的一个点，我们证明  $\pmb {x}\in f(I)$  ，首先，我们注意，对于给定的  $_n$  ，道路  $f_{n}$  能够到达距离点  $\pmb{x}$  为  $1 / 2^{n}$  的范围以内，因为把  $I^2$  分割为边长是  $1 / 2^{n}$  的小正方形，道路  $f_{n}$  会碰到每一个这样的小方块.

利用这一点，我们证明，对任意  $\varepsilon > 0$  ， $\pmb{x}$  的  $\varepsilon$ -邻域都与  $f(I)$  相交．选取充分大的  $N$  ，使得

$$
\rho (f _ {N}, f) <   \varepsilon / 2 \quad \text {且} \quad 1 / 2 ^ {N} <   \varepsilon / 2.
$$

根据前一段的结果，存在一个点  $t_0 \in I$ ，使得  $d(\pmb{x}, f_N(t_0)) \leqslant 1/2^N$ 。因为对于所有的  $t$ ，有  $d(f_N(t), f(t)) < \varepsilon/2$ ，所以

$$
d (x, f (t _ {0})) <   \varepsilon ,
$$

从而  $\pmb{x}$  的  $\epsilon$ -邻域与  $f(I)$  相交.

由此可见  $\pmb{x}$  属于  $f(I)$  的闭包．但由于  $I$  是紧致的，所以  $f(I)$  是紧致的，从而是闭的．于是证明了  $\pmb{x}$  属于  $f(I)$

## 练习


1. 给定  $n$ ，证明存在一个连续的满射  $g: I \to I^n$ 。[提示：考虑  $f \times f: I \times I \to I^2 \times I^2$ .]

2. 证明存在连续满射  $f: \mathbb{R} \rightarrow \mathbb{R}^n$ .

3. (a) 若  $\mathbb{R}^n$  被赋予积拓扑，证明不存在连续的满射  $f: \mathbb{R} \to \mathbb{R}^n$ . [提示：证明  $\mathbb{R}^n$  不能表示成可数个紧致子空间的并.]

(b) 若  $\mathbb{R}^n$  被赋予积拓扑，确定是否存在连续满射  $f: \mathbb{R} \to \mathbb{R}^{\infty}$ .

(c)若  $\mathbb{R}^n$  被赋予一致拓扑或箱拓扑，对于小题(a)和(b)会有怎样的结论呢？

4. (a) 设  $X$  是一个Hausdorff空间．证明：若存在连续满射  $f: I \to X$ ，则  $X$  是紧致的、连通的、弱局部连通的，并且可以度量化．[提示：证明  $f$  是完备映射.]

(b)上面小题(a)的逆命题也成立，它是点集拓扑学中著名的Hahn-Mazurkiewicz定理（见[H-Y]p.129).假设我们已知这个定理，然后证明存在一个连续满射  $f$  ：  $I\to I^{\omega}$

如果某一个Hausdorff空间是单位闭区间的连续像，通常称之为一个Peano空间（Peanospace).


# 第33节 度量空间中的紧致性
## 33-1 度量空间中的紧致性

我们已经证明了对于度量空间来说，紧致性、极限点紧致性以及列紧性都是等价的。度量空间中的紧致性也有其他的描述方法，其中有一种就涉及到完备性的概念。这一节我们就来研究它。作为应用，我们再证明一个刻划  $\mathcal{C}(X, \mathbb{R}^n)$  中（关于一致度量）紧致子集的定理。

度量空间  $X$  的紧致性与它的完备性有什么关系呢？根据引理43.1可见，每一个紧致度量空间必定是完备的。反之未必成立，也就是说，完备度量空间未必是紧致的。那么下面一个很自然的问题就是，完备空间需附加什么条件才能得出紧致性呢？这个条件就是所谓的完全有界性。

定义 度量空间  $(X, d)$  称为完全有界的 (totally bounded), 如果对任意  $\epsilon > 0$ , 存在一个由  $\epsilon$ -球构成的  $X$  的有限覆盖.

例1 显然，度量空间的完全有界性蕴涵有界性．因为若  $B(x_{1}, 1/2), \cdots, B(x_{n}, 1/2)$  是  $X$  的一个由半径为  $1/2$  的开球构成的有限覆盖，则  $X$  的直径最多为  $1 + \max \{d(x_{i}, x_{j})\}$  但反之未必成立．例如，在度量  $\bar{d}(a, b) = \min \{1, |a - b|\}$  之下，实直线  $\mathbb{R}$  是有界的但不是完全有界的.

例2 关于度量  $d(a, b) = |a - b|$ ，实直线  $\mathbb{R}$  是完备的但不是完全有界的。子空间  $(-1, 1)$  是完全有界的，却不是完备的，而子空间  $[-1, 1]$  既是完备的，也是完全有界的。

定理45.1 度量空间  $(X,d)$  是紧致的，当且仅当它是完备和完全有界的。

证 如上所说，若  $X$  是一个紧致度量空间，则  $X$  自然是完备的。又因为所有的开  $\varepsilon$ -球做成的  $X$  的开覆盖必包含一个有限子覆盖，所以  $X$  是完全有界的。

反之，设  $X$  是完备的和完全有界的．下面只需证明  $X$  是列紧的便可以了.

设  $(x_{n})$  是  $X$  中点的一个序列，我们来选取它的一个子序列，要求这个子序列是一个Cauchy序列，因而一定收敛．首先，用有限多个半径为1的球覆盖  $X$  ，这时，至少有一个球，比如说 $B_{1}$  ，包含无限多个  $x_{n}$  ．设  $J_{1}$  是  $\mathbb{Z}_{+}$  的一个子集，使得对于每一个  $x_{n}$  ，若  $x_{n}\in B_{1}$  ，则  $n\in J_1$

其次，用有限多个半径为  $1 / 2$  的球覆盖  $X$  ，因为  $J_{1}$  是无限的，这些球中至少有一个，比如说  $B_{2}$  ，包含  $J_{1}$  中无限多个  $_n$  。取  $J_{2}$  为满足  $n\in J_1$  和  $x_{n}\in B_{2}$  的所有  $_n$  构成的集合。一般地，给定正整数的无穷集  $J_{k}$  ，取  $J_{k + 1}$  为  $J_{k}$  的一个无穷子集，使得存在一个半径为  $1 / (k + 1)$  的球 $B_{k + 1}$  ，对于所有的  $n\in J_{k + 1}$  ，有  $x_{n}\in B_{k + 1}$

选取  $n_1 \in J_1$ 。对于给定的  $n_k$ ，选取  $n_{k+1} \in J_{k+1}$ ，使得  $n_{k+1} > n_k$ 。因为  $J_{k+1}$  是无穷集，这一点是可以做得到的。现在，对于  $i$ ， $j \geq k$ ，指标  $n_i$ ， $n_j$  都属于  $J_k$ （因为  $J_1 \supset J_2 \supset \cdots$  是一个集合的套序列）。因此，对于所有的  $i$ ， $j \geq k$ ，点  $x_{n_i}$  和  $x_{n_j}$  都包含在半径为  $1/k$  的球  $B_k$  中。于是，序列  $(x_{n_i})$  是一个 Cauchy 序列。

我们现在应用这一结论来寻找  $\mathcal{C}(X, \mathbb{R}^n)$  在一致拓扑下的一个紧致子空间。我们已经知道  $\mathbb{R}^n$  的子空间是紧致的当且仅当它是闭的和有界的。大家可能希望对于  $\mathcal{C}(X, \mathbb{R}^n)$  也有相似的结论成立。但事实并非如此，即使在  $X$  紧致的情况下也不行。其实，这需要  $\mathcal{C}(X, \mathbb{R}^n)$  的子空间满足一个条件，即等度连续性。现在我们来看它的定义。

定义 设  $(Y, d)$  是一个度量空间． $\mathcal{F}$  是函数空间  $\mathcal{C}(X, Y)$  的一个子集．对于  $x_0 \in X$  ，函

数集  $\mathcal{F}$  称为在  $x_0$  处等度连续的 (equicontinuous at  $x_0$ ), 如果给定  $\varepsilon > 0$ , 存在  $x_0$  的一个邻域  $U$ , 使得对于所有的  $x \in U$  及所有  $f \in \mathcal{F}$  有

$$
d (f (x), f (x _ {0})) <   \varepsilon .
$$

如果对于每一个点  $x_0 \in X$ ，集合  $\mathcal{F}$  在  $x_0$  处等度连续，则称  $\mathcal{F}$  是等度连续的(equicontinuous).

函数  $f$  在点  $x_0$  处的连续性是指对给定的  $f$  及给定的  $\varepsilon > 0$ ，存在  $x_0$  的一个邻域  $U$ ，使对于所有  $x \in U$  有  $d(f(x), f(x_0)) < \varepsilon$ 。 $\mathcal{F}$  的等度连续性是指存在一个邻域  $U$ ，对于  $\mathcal{F}$  中的所有的函数  $f$ ，上式都成立。

注意，等度连续性依赖于具体的度量，而不仅仅是  $Y$  上的拓扑.

引理45.2 设  $X$  是一个空间， $(Y, d)$  是一个度量空间。设  $\mathcal{F}$  是  $\mathcal{C}(X, Y)$  的一个子集，并且关于度量  $d$  的一致度量是完全有界的，则  $\mathcal{F}$  关于  $d$  是等度连续的。

证 设  $\mathcal{F}$  是完全有界的。给定  $0 < \varepsilon < 1$ ，给定  $x_0$ ，以下证明存在  $x_0$  的一个邻域  $U$ ，对于所有  $f \in \mathcal{F}$  和  $x \in U$ ，有  $d(f(x), f(x_0)) < \varepsilon$ 。

设  $\delta = \varepsilon /3$  ，用  $\mathcal{C}(X,Y)$  中的有限多个开  $\delta$  -球

$$
B (f _ {1}, \delta), \dots , B (f _ {n}, \delta)
$$

覆盖  $\mathcal{F}$  ，因为每一个函数  $f_{i}$  是连续的，我们可以选取  $x_0$  的一个邻域  $U$  ，使得对于  $i = 1,\dots ,n$  和  $x\in U$  ，有

$$
d \left(f _ {i} (x), f _ {i} \left(x _ {0}\right)\right) <   \delta .
$$

设  $f$  是  $\mathcal{F}$  的任意一个元素，则  $f$  至少属于上述  $\delta-$  球中的某一个，不妨设为  $B(f_{i},\delta)$  ．于是对于  $x\in U$  ，有

$$
\vec {d} (f (x), f _ {i} (x)) <   \delta ,
$$

$$
d \left(f _ {i} (x), f _ {i} \left(x _ {0}\right)\right) <   \delta ,
$$

$$
\bar {d} \left(f _ {i} \left(x _ {0}\right), f \left(x _ {0}\right)\right) <   \delta .
$$

第一个和第三个不等式成立是因为  $\bar{\rho}(f, f_i) < \delta$ ，第二个不等式成立是因为  $x \in U$ 。由于  $\delta < 1$ ，所以用  $d$  代替  $\overline{d}$  时，第一个和第三个不等式依然成立。所以根据三角不等式可见对于所有的  $x \in U, d(f(x), f(x_0)) < \varepsilon$  成立。

现在我们来证明 Ascoli 定理的经典形式, 它所讨论的就是函数空间  $\mathcal{C}(X, \mathbb{R}^n)$  的紧致子空间. 这个定理的一个更广义形式, 其证明并不依赖这个经典形式 (将在第 47 节中给出). 广义形式的证明依赖于 Tychonoff 定理, 但在这里并不需要.

* 引理 45.3 设  $X$  是一个空间， $(Y, d)$  是一个度量空间。设  $X$  和  $Y$  是紧致的。如果  $\mathcal{F}$  关于  $d$  是  $\mathcal{C}(X, Y)$  的一个等度连续子集，那么关于度量  $d$  的一致度量和上确界度量， $\mathcal{F}$  是完全有界的。

证 由于  $X$  是紧致的，可以在  $\mathcal{C}(X, Y)$  上定义上确界度量  $\rho$ 。关于  $\rho$  完全有界等价于关于  $\bar{\rho}$  完全有界。因为对于  $\varepsilon < 1$ ，关于  $\rho$  的每一个  $\varepsilon-$  球也是关于  $\bar{\rho}$  的一个  $\varepsilon-$  球，反之亦成立。所以我们可以始终只用度量  $\rho$ 。

设  $\mathcal{F}$  是等度连续的．给定  $\varepsilon >0$  ，用关于度量  $\rho$  的有限多个开  $\varepsilon$ -球覆盖  $\mathcal{F}$

令  $\delta = \varepsilon /3$  ，任意给定  $a\in X$  ，存在  $a$  的相应邻域  $U_{a}$  使得对任意  $x\in U_{a}$  和任意  $f\in \mathcal{F}$  ，有

$d(f(x),f(a)) < \delta$  于是可以找到有限多个邻域  $U_{a}$  ，  $a = a_{1}$  ，…，  $a_{k}$  ，组成  $X$  的一个覆盖，用 $U_{i}$  表示  $U_{a_i}$  ．选取直径小于  $\delta$  的有限个开集  $V_{1}$  ，…，  $V_{m}$  覆盖  $Y$

设  $J$  是所有函数  $\alpha: \{1, \cdots, k\} \rightarrow \{1, \cdots, m\}$  的集合。给定  $\alpha \in J$ ，若存在  $\mathcal{F}$  中的一个函数  $f$ ，使得对于每一个  $i = 1, \cdots, k$ ， $f(a_i) \in V_{\alpha(i)}$ ，便选取一个这样的函数，记为  $f_\alpha$ 。集合  $\{f_\alpha\}$  是由集合  $J$  的一个子集  $J'$  加标的，所以是有限的。我们断言：开球  $B_\rho(f_\alpha, \varepsilon)$ ， $\alpha \in J'$ ，覆盖  $\mathcal{F}$ 。

设  $f$  是  $\mathcal{F}$  的一个元素．对于每一个  $i = 1,\dots ,k$  ，选取整数  $\alpha (i)$  使得  $f(a_{i})\in V_{\alpha (i)}$  ，则函数  $\alpha$  在  $J^{\prime}$  中．我们断言：  $f$  属于球  $B_{\rho}(f_{\alpha},\varepsilon)$

设  $x$  是  $X$  的一个点．选取  $i$  使得  $x \in U_i$  ，于是

$$
d (f (x), f (a _ {i})) <   \delta ,
$$

$$
d \left(f \left(a _ {i}\right), f _ {a} \left(a _ {i}\right)\right) <   \delta ,
$$

$$
d \left(f _ {\alpha} \left(a _ {i}\right), f _ {\alpha} (x)\right) <   \delta .
$$

第一个和第三个不等式成立是因为  $x \in U_i$ ，第二个不等式成立是因为  $f(a_i)$  和  $f_\alpha(a_i)$  都属于  $V_{\alpha(i)}$ 。综上可见， $d(f(x), f_\alpha(x)) < \varepsilon$ 。因对于所有的  $x \in X$ ，以上不等式成立，所以

$$
\rho (f, f _ {\alpha}) = \max  \{d (f (x), f _ {\alpha} (x)) \} <   \varepsilon .
$$

因此  $f$  属于开球  $B_{\rho}(f_{\sigma}, \varepsilon)$

定义 设  $(Y, d)$  是一个度量空间。 $\mathcal{C}(X, Y)$  的子集  $\mathcal{F}$  称为关于  $d$  是点态有界的 (pointwise bounded)，如果对于每一个  $a \in X^{\mathfrak{U}}$ ， $Y$  的子集

$$
\mathcal {F} _ {a} = \{f (a) \mid f \in \mathcal {F} \}
$$

关于  $d$  是有界的.

* 定理 45.4[(Ascoli 定理, 经典形式 (Ascoli theorem, classical version))] 设  $X$  是一个紧致空间,  $(\mathbb{R}^n, d)$  表示关于平方度量或欧氏度量的欧氏空间, 赋予  $\mathcal{C}(X, \mathbb{R}^n)$  相应的一致拓扑. 那么  $\mathcal{C}(X, \mathbb{R}^n)$  的子空间  $\mathcal{F}$  有紧致闭包当且仅当  $\mathcal{F}$  关于  $d$  是等度连续的和点态有界的.

证 因为  $X$  是紧致的，在  $\mathcal{C}(X, \mathbb{R}^n)$  上定义上确界度量  $\rho$ ，并赋予  $\mathcal{C}(X, \mathbb{R}^n)$  一致拓扑。并始终用  $\wp$  表示  $\mathcal{F}$  在  $\mathcal{C}(X, \mathbb{R}^n)$  中的闭包。

第一步．证明若  $\mathcal{G}$  是紧致的，则关于  $d$  ，是等度连续的并且是点态有界的．根据  $\mathcal{F} \subset \mathcal{G}$  可见  $\mathcal{F}$  也是等度连续的并且点态有界的．这就证明了定理的“必要性”

根据定理45.1，  $\mathcal{G}$  的紧致性蕴涵着  $\mathcal{G}$  关于  $\rho$  和关于  $\bar{\rho}$  都是完全有界的，再根据引理45.2， $\mathcal{G}$  关于  $d$  是等度连续的．  $\mathcal{G}$  的紧致还蕴涵着  $\mathcal{G}$  关于  $\rho$  是有界的．由此又可见  $\mathcal{G}$  在  $d$  下是点态有界的．因为如果对于任意  $f, g \in \mathcal{G}$  有  $\rho(f, g) \leqslant M$  ，那么，特别地， $d(f(a), g(a)) \leqslant M$  ，因此  $\mathcal{G}_a$  的直径最多为  $M$

第二步．证明若  $\mathcal{F}$  关于  $d$  是等度连续和点态有界的，则  $\mathcal{G}$  也是等度连续和点态有界的.

首先验证等度连续性．给定  $x_0\in X$  和  $\varepsilon >0$  ，选取  $x_0$  的一个邻域  $U$  ，使得对于所有的  $x\in$ $U$  和  $f\in \mathcal{F}$  ，有  $d(f(x),f(x_0)) <   \varepsilon /3$  ．任意给定  $g\in \mathcal{G}$  ，选取  $f\in \mathcal{F}$  ，使得  $\rho (f,g) <   \varepsilon /3.$  根据三角不等式可见，对于所有  $x\in U$  ，有  $d(g(x),g(x_0)) <   \varepsilon$  ，因为  $\pmb{g}$  是任意的，所以  $\mathcal{G}$  在 $x_0$  点等度连续.

其次再来证明点态有界性．给定  $a$  ，选取  $M$  ，使得  $\mathcal{F}_a$  的直径不大于  $M$  ．任意给定  $g$ $g^{\prime}\in \mathcal{G}$  ，选取  $f$  ，  $f^{\prime}\in \mathcal{F}$  ，使得  $\rho (f,g) < 1$  和  $\rho (f^{\prime},g^{\prime}) < 1$  ，因为  $d(f(a),f^{\prime}(a))\leqslant M$  ，所以  $d(g(a),g^{\prime}(a))\leqslant M + 2$  ，再由  $g$  和  $g^{\prime}$  是任意的可得  $\mathrm{diam}\mathcal{G}_a\leqslant M + 2.$

第三步．证明若  $\mathcal{G}$  是等度连续的并且点态有界的，则存在  $\mathbb{R}^n$  的紧致子空间  $Y$  ，它包含着所有集合  $g(X)$  的并，其中  $g\in \mathcal{G}$

对于每一个  $a \in X$ ，选取邻域  $U_{a}$ ，使得对于所有  $x \in U_{a}$  和  $g \in \mathcal{G}$ ，有  $d(g(x), g(a)) < 1$ 。因为  $X$  是紧致的，所以可以选取有限多个这种邻域覆盖  $X$ ，不妨设这些邻域的下标为  $a = a_{1}, \cdots, a_{k}$ 。因为  $\mathcal{G}_{a_{i}}$  是有界的，所以它们的并也是有界的，设它包含于  $\mathbb{R}^{n}$  中的以原点为球心、以  $N$  为半径的球中。于是对于所有的  $g \in \mathcal{G}$ ，集合  $g(X)$  包含于以原点为球心、以  $N + 1$  为半径的球中。令  $Y$  为这个球的闭包。

第四步．充分性的证明．设  $\mathcal{F}$  关于  $d$  是等度连续和点态有界的．我们证明关于  $\rho, \mathcal{G}$  是完备的和完全有界的．根据定理45.1可见， $\mathcal{G}$  是紧致的.

完备性容易证得．因为  $\pmb{\vartheta}$  是完备度量空间  $(\mathcal{C}(X,\mathbb{R}^n),\rho)$  的一个闭子空间.

我们来验证完全有界性．首先，根据第二步可见  $\wp$  在度量  $d$  下是等度连续的和点态有界的；再根据第三步可见，存在  $\mathbb{R}^n$  的紧致子空间  $Y$  ，使得  $\wp \subset \mathcal{C}(X,Y)$  ．根据引理45.3， $\wp$  的等度连续性蕴涵着  $\wp$  关于  $\rho$  是完全有界的.

* 推论 45.5 设  $X$  是紧致的,  $d$  为  $\mathbb{R}^n$  上的平方度量或欧氏度量, 赋予  $\mathcal{C}(X, \mathbb{R}^n)$  相应的一致拓扑. 则  $\mathcal{C}(X, \mathbb{R}^n)$  的一个子空间  $\mathcal{F}$  是紧致的, 当且仅当它关于上确界度量  $\rho$  是闭的和有界的, 关于  $d$  是等度连续的.

证 若  $\mathcal{F}$  是紧致的，则它必定是闭的和有界的。根据前一个定理易见它还是等度连续的。反之，若  $\mathcal{F}$  是闭的，则它就等于它的闭包  $\mathcal{G}$ 。若它关于  $\rho$  是有界的，则关于  $d$  是点态有界的。若它是等度连续的，则前一个定理蕴涵着它是紧致的。


## 练习


1. 若  $X_{n}$  是可度量化的，并且有度量  $d_{n}$ ，则

$$
D (\boldsymbol {x}, \boldsymbol {y}) = \sup  \left\{\bar {d} _ {i} \left(x _ {i}, y _ {i}\right) / i \right\}
$$

是积空间  $X = \Pi X_{n}$  的一个度量．证明若每一个  $X_{n}$  在  $d_{n}$  下都是完全有界的，则  $X$  在  $D$  下是完全有界的．在不使用Tychonoff定理的情况下，证明紧致可度量化空间的可数积空间是紧致的.

2. 设  $(Y, d)$  是一个度量空间， $\mathcal{F}$  是  $\mathcal{C}(X, Y)$  的一个子集。

(a)证明：若  $\mathcal{F}$  是有限的，则  $\mathcal{F}$  是等度连续的.  
(b) 证明：若  $f_{n}$  是  $\mathcal{C}(X, Y)$  中元素的一个序列，并且一致收敛，则集合  $\{f_{n}\}$  是等度连续的.  
(c) 设  $\mathcal{F}$  是可微函数  $f: \mathbb{R} \rightarrow \mathbb{R}$  的集合，其中这些可微函数满足条件：对于每一个  $x \in \mathbb{R}$ ，存在某一个邻域  $U$ ，使得  $\mathcal{F}$  的所有函数的导数在这个邻域  $U$  上是一致有界的。[即存在  $M$ ，使得对于所有  $y \in U$  和所有  $f \in \mathcal{F}$  有  $|f'(y)| \leqslant M$ .] 证明  $\mathcal{F}$  是等度连续的。

3. 证明：

定理（Arzela 定理）设  $X$  紧致的，并且  $f_n \in \mathcal{C}(X, \mathbb{R}^k)$ 。若族  $\{f_n\}$  是点态有界的和等度连续的，则序列  $f_n$  有一个一致收敛的子序列。

4. (a) 设函数  $f_{n} \colon I \to \mathbb{R}$  定义为  $f_{n}(x) = x^{n}$ . 集合  $\mathcal{F} = \{f_{n}\}$  是点态有界的, 但序列  $(f_{n})$  没有一致收敛的子序列, 在哪个或哪些点处  $\mathcal{F}$  不是等度连续的?

(b)针对第21节的习题9中定义的函数  $f_{n}$  再次讨论(a)的情况.

5. 设  $X$  是一个空间． $\mathcal{C}(X, \mathbb{R})$  的子集  $\mathcal{F}$  称为在无穷远处一致蜕化（vanish uniformly at infinity），如果给定  $\varepsilon > 0$ ，存在  $X$  的一个紧致子集  $C$ ，使得对于每一个  $x \in X - C$  及  $f \in \mathcal{F}$ ，有  $|f(x)| < \varepsilon$ 。如果  $\mathcal{F}$  仅由一个函数  $f$  组成，则称  $f$  在无穷远处蜕化（vanishes at infinity）。用  $\mathcal{C}_0(X, \mathbb{R})$  表示在无穷远处蜕化的连续函数  $f: X \to \mathbb{R}$  的族。

定理 设  $X$  是局部紧致的 Hausdorff 空间，赋予  $\mathcal{C}_0(X, \mathbb{R})$  一致拓扑。 $\mathcal{C}_0(X, \mathbb{R})$  的子集  $\mathcal{F}$  有紧致闭包，当且仅当它是点态有界的和等度连续的，并且在无穷远处一致蜕化。

[提示：用  $Y$  表示  $X$  的单点紧致化，证明若赋予  $\mathcal{C}_0(X, \mathbb{R})$  和  $\mathcal{C}(Y, \mathbb{R})$  上确界度量，则  $\mathcal{C}_0(X, \mathbb{R})$  等距于  $\mathcal{C}(Y, \mathbb{R})$  的一个闭子空间.]

6. 在 Ascoli 定理的证明中将  $\mathbb{R}^n$  统统换为任意一个度量空间，只要求它满足条件：其中的所有闭的有界子空间都是紧致的。证明结论依然成立。

*7. 设  $(X, d)$  是一个度量空间．如果  $A \subset X$  和  $\varepsilon > 0$  ，令  $U(A, \varepsilon)$  表示  $A$  的  $\varepsilon-$  邻域．令  $\mathcal{H}$  为  $X$  的所有(非空)有界闭子集的族．如果  $A, B \in \mathcal{H}$  ，定义

$$
D (A; B) = \inf  \{\varepsilon \mid A \subset U (B, \varepsilon) \text {并 且} B \subset U (A, \varepsilon) \}.
$$

(a) 证明:  $D$  是  $\mathcal{H}$  的一个度量, 称之为 Hausdorff 度量 (Hausdorff metric).

(b) 证明：如果  $(X, d)$  是完备的，则  $(\mathcal{H}, D)$  也是完备的。[提示：设  $A_{n}$  为  $\mathcal{H}$  中的一个Cauchy序列。用过渡到子序列的办法，假定  $D(A_{n}, A_{n+1}) < 1 / 2^{n}$ 。定义  $A$  为序列  $x_{1}, x_{2}, \cdots$  的极限点的集合，要求这些序列  $x_{1}, x_{2}, \cdots$  满足条件：对于每一个  $i$ ， $x_{i} \in A_{i}$ ，并且  $d(x_{i}, x_{i+1}) < 1 / 2^{i}$ 。证明  $A_{n} \rightarrow \overline{A}$ 。]  
(c) 证明：若  $(X, d)$  是完全有界的，则  $(\mathcal{H}, D)$  也是完全有界的。[提示：给定  $\varepsilon$ ，选取  $\delta < \varepsilon$ ，并且令  $S$  是  $X$  的一个有限子集，使得族  $\{B_d(x, \delta) \mid x \in S\}$  覆盖  $X$ 。设  $\mathcal{A}$  是  $S$  的所有非空子集构成的族。证明  $\{B_D(A, \varepsilon) \mid A \in \mathcal{A}\}$  覆盖  $\mathcal{H}$ 。]  
(d)定理 若  $X$  关于度量  $d$  是紧致的，则  $\mathcal{H}$  关于Hausdorff度量  $D$  也是紧致的.

*8. 设  $(X, d_X)$  和  $(Y, d_Y)$  都是度量空间，赋予  $X \times Y$  相应的平方度量，用  $\mathcal{H}$  表示  $X \times Y$  关于Hausdorff度量  $D$  的所有(非空)有界闭子集的族．关于一致度量，考虑空间  $\mathcal{C}(X, Y)$ ．设映射  $gr: \mathcal{C}(X, Y) \to \mathcal{H}$  是在每一个连续函数  $f: X \to Y$  上，取值为函数  $f$  的图像

$$
G _ {f} = \{x \times f (x) \mid x \in X \}
$$

的那个函数.

(a)证明映射  $gr$  是单射，并且一致连续  
(b)用  $\mathcal{H}_0$  表示映射  $gr$  的像集，设  $g: \mathcal{C}(X, Y) \to \mathcal{H}_0$  是由  $gr$  得到的一个满射。证明若  $f: X \to Y$  是一致连续的，则映射  $g^{-1}$  在点  $G_f$  处是连续的。

(c)举一个映射  $g^{-1}$  在点  $G_{f}$  处不连续的例子.  
(d)定理 若  $X$  是紧致的，则  $gr: \mathcal{C}(X, Y) \to \mathcal{H}$  是一个嵌入.

# 第34节 点态收敛和紧致收敛

## 34-1 点态收敛和紧致收敛

空间  $Y^{X}$  和  $\mathcal{C}(X, Y)$  除了一致拓扑之外，还有其他一些有用的拓扑。现在我们要讨论其中的三个：点态收敛拓扑、紧致收敛拓扑以及紧致开拓扑。

定义 给定集合  $X$  的一个点  $\pmb{x}$  以及空间  $Y$  的一个开集  $U$  ，令

$$
S (x, U) = \{f \mid f \in Y ^ {X}   \text {和}   f (x) \in U \}.
$$

所有集合  $S(x, U)$  构成  $Y^X$  的拓扑的一个子基，这个拓扑称为点态收敛拓扑（topology of pointwise convergence）或点开拓扑（point-open topology）。

这个拓扑的一般基元素是子基元素  $S(x, U)$  的有限交。因此，包含函数  $f$  的一个典型的基元素就是由所有在有限多点处“接近” $f$  的函数  $g$  组成。这样的邻域如图 46.1 所示，它由所有函数图像与所给三个垂直区间都相交的函数构成。

![](888b5361b00b4398b4320a89f35079bcb1236e842bb799ebbf61697404a5f303.jpg)  
图46.1

$Y^{X}$  上的点态收敛拓扑并非新鲜事物，它就是我们早已研究过的积拓扑．如果我们用  $J$  代替  $X$  将  $J$  的一般元素记为  $\alpha$  ，这样看起来就更加熟悉了．这时，使得  $x(\alpha)\in U$  的所有函数  $\pmb{x}$  ：  $J\rightarrow Y$  构成的集合  $S(\alpha ,U)$  恰好就是  $Y^{J}$  的子集  $\pi_{\alpha}^{-1}(U)$  ，而它也正好就是积拓扑的标准子基元素.

称其为点态收敛拓扑的理由缘于以下定理：

定理46.1 在点态收敛拓扑下，函数序列  $f_{n}$  收敛于函数  $f$  ，当且仅当对于每一个点  $x \in X$  ， $Y$  中点的序列  $f_{n}(x)$  收敛于点  $f(x)$  。

证这是引理43.3所证明的积拓扑中的一个一般性的事实，在这里只是使用函数空间记号重新陈述一遍.

例1考虑空间  $\mathbb{R}^l$  ，其中  $I = [0,1]$  ，定义为  $f_{n}(x) = x^{n}$  的连续函数序列  $(f_n)$  在点态收敛拓扑下收敛于函数  $f$  ，其中  $f$  的定义为

$$
f (x) = \left\{ \begin{array}{l l} 0 & \text {对 于} 0 \leqslant x <   1, \\ 1 & \text {对 于} x = 1. \end{array} \right.
$$

这个例子说明，在点态收敛拓扑下，连续函数的子空间  $\mathcal{C}(I, \mathbb{R})$  不是  $\mathbb{R}^I$  中的闭集.

我们知道，若一个连续函数序列  $(f_n)$  在一致拓扑下收敛，则极限必定是连续的。然而上面这个例子说明，一个序列仅在点态收敛拓扑下收敛，却未必有连续的极限。人们可能要问，是否存在某一个拓扑介于这两个拓扑之间，仍能保证连续函数的收敛序列有连续的极限呢？答案是肯定的。只要对空间  $X$  加一点限制，而且这个限制还相当宽泛，即要求  $X$  是紧致生成的。如果在以下定义的紧致收敛拓扑下， $(f_n)$  收敛于  $f$ ，就足以保证  $f$  是连续的了。

定义 设  $(Y, d)$  是一个度量空间， $X$  是一个拓扑空间。给定  $Y^X$  的一个元素  $f$ ， $X$  的一个紧致子空间  $C$  以及一个数  $\varepsilon > 0$ ，令  $B_C(f, \varepsilon)$  表示  $Y^X$  中所有满足下式的元素  $g$  构成的集合：

$$
\sup  \left\{d (f (x), g (x)) \mid x \in C \right\} <   \varepsilon .
$$

这些集合  $B_{C}(f,\varepsilon)$  组成了  $Y^{X}$  的一个拓扑基．我们称这个拓扑为紧致收敛拓扑(topology of compact convergence)(有时也称它为“紧致集合上的一致收敛拓扑").

易见这些集合  $B_{C}(f,\varepsilon)$  满足作为基的条件．最关键的一步是注意，若  $g\in B_C(f,\varepsilon)$  ，则对

$$
\delta = \epsilon - \sup  \left\{d (f (x), g (x)) \mid x \in C \right\},
$$

有  $B_{C}(g,\delta)\subset B_{C}(f,\varepsilon)$

这个拓扑与前面的拓扑不同，在这个拓扑中包含  $f$  的基元素由具有下述特点的函数组成：它不是仅在有限多个点上“接近”  $f$  ，而是在某一个紧致集的所有点上“接近”  $f$

采用这个术语的合理性来自以下定理. 这个定理的证明是直接的.

定理46.2 函数序列  $f_{n}$  ：  $X\rightarrow Y$  关于紧致收敛拓扑收敛于函数  $f$  ，当且仅当对  $X$  的每一个紧致子空间  $C$  ，序列  $f_{n}\mid C$  一致收敛于  $f\mid C.$

定义 空间  $X$  称为紧致生成的 (compactly generated), 如果  $X$  的一个子集  $A$  满足条件: 对于  $X$  的每一个紧致子空间  $C$ ,  $A \cap C$  是  $C$  中一个开集, 则  $A$  是  $X$  中的一个开集.

这个条件等价于：如果对于每一个紧致子集  $C$ ， $B \cap C$  是  $C$  中闭集，那么集合  $B$  是  $X$  中闭集。这是对空间的一种相当宽泛的限制，因为许多熟知的空间都是紧致生成的。例如以下引理。

引理46.3 若  $X$  是局部紧致的，或者  $X$  满足第一可数性公理，则  $X$  是紧致生成的。

证 设  $X$  是局部紧致的，对于  $X$  的每一个紧致子空间  $C$ ， $A \cap C$  是  $C$  的一个开集，我们证明  $A$  是  $X$  的一个开集。给定  $x \in A$ ，选取  $x$  的一个邻域  $U$ ，使它包含于  $X$  的某一个紧致子空间  $C$  中。根据假设，由于  $A \cap C$  是  $C$  的一个开集，所以  $A \cap U$  是  $U$  的一个开集，从而也是  $X$  的一个开集。于是  $A \cap U$  就是  $x$  的一个包含在  $A$  中的邻域，所以  $A$  是  $X$  的一个开集。

设  $X$  满足第一可数性公理，如果对于  $X$  的每一个紧致子集  $C$  ， $B \cap C$  是  $C$  的一个闭集，我们证明  $B$  也是  $X$  的一个闭集．设  $x$  是  $\overline{B}$  的一个点，下面证明  $x \in B$  ，因为  $X$  在点  $x$  处有可数基，所以存在  $B$  中点的一个序列  $(x_{n})$  收敛于  $x$  ，子空间

$$
C = \{x \} \cup \left\{x _ {n} \mid n \in \mathbf {Z} _ {+} \right\}
$$

是紧致的．因此根据假定  $B\cap C$  是  $C$  的一个闭集．又因为对于每一个  $\pmb{n}$  ，  $B\cap C$  包含  $\pmb{x}_{n}$  ，所以它也必包含  $\pmb{x}$  ，从而  $x\in B$

关于紧致生成空间的一个关键性的结论是：

引理46.4 若  $X$  是紧致生成的，则函数  $f: X \to Y$  只要对于  $X$  的每一个紧致子空间  $C$ ， $f|_{C}$  是连续的， $f$  便是连续的。

证 设  $V$  是  $Y$  的一个开子集，我们证明  $f^{-1}(V)$  是  $X$  中的开子集。给定  $X$  的任意一个子空间  $C$ ，

$$
f ^ {- 1} (V) \cap C = (f \mid C) ^ {- 1} (V).
$$

如果  $C$  是紧致的，由  $f \mid C$  是连续的，可见这个集合是  $C$  的一个开集．因为  $X$  是紧致生成的，所以  $f^{-1}(V)$  是  $X$  的一个开集.

定理46.5 设  $X$  是一个紧致生成的空间， $(Y, d)$  是一个度量空间，则  $\mathcal{C}(X, Y)$  关于紧致收敛拓扑是  $Y^X$  的一个闭集。

证 设  $f \in Y^{X}$  是  $\mathcal{C}(X, Y)$  的一个极限点，我们证明  $f$  连续。只需证明，对于  $X$  的每一个紧致子集  $C$ ， $f \mid C$  是连续的。对于每一个  $n$ ，考虑  $f$  的邻域  $B_{C}(f, 1/n)$ ，因为它和  $\mathcal{C}(X, Y)$  相交，所以可以选出一个函数  $f_{n} \in \mathcal{C}(X, Y)$  包含在这一邻域中。函数序列  $f_{n} \mid C: C \to Y$  一致收敛于函数  $f \mid C$ ，因而根据一致极限定理， $f \mid C$  连续。

推论46.6 设  $X$  是一个紧致生成的空间， $(Y, d)$  是一个度量空间。如果一个连续函数序列  $f_n \in \mathcal{C}(X, Y)$  在紧致收敛拓扑下收敛于函数  $f$ ，那么  $f$  是连续的。

当  $Y$  是一个度量空间时，我们在函数空间  $Y^X$  上有三个拓扑．这三者之间的关系可由下述定理来予以说明，它的证明是直接的.

定理46.7 设  $X$  是一个空间， $(Y, d)$  是一个度量空间。对于函数空间  $Y^X$  上的三种拓扑之间有以下包含关系：

（一致拓扑）  $\supset$  （紧致收敛拓扑）  $\supset$  （点态收敛拓扑）.

如果  $X$  是紧致的，则前两个拓扑是一致的．如果  $X$  是离散的，则后两个拓扑是一致的.

一致拓扑与紧致收敛拓扑的定义都涉及到空间  $Y$  上的度量  $d$ ，但点态收敛拓扑却不需要。事实上，它的定义是针对任意空间  $Y$  的。这样自然就会产生疑问：是否其他两个拓扑中的哪一个可以扩展为对任意拓扑空间  $Y$  有定义呢？对于从  $X$  映入  $Y$  的所有函数构成的空间  $Y^X$ ，这个问题还没有满意的答案。但是，对于连续函数空间  $\mathcal{C}(X, Y)$ ，却可以得到一些结果。我们在  $\mathcal{C}(X, Y)$  上定义一种拓扑，即紧致开拓扑。可见若  $Y$  是一个度量空间，则这个拓扑就与紧致收敛拓扑一致。如我们将要看到的，紧致开拓扑本身十分重要。

定义 设  $X$  和  $Y$  是两个拓扑空间。如果  $C$  是  $X$  的一个紧致子空间， $U$  是  $Y$  的一个开子集，定义

$$
S (C, U) = \{f \mid f \in \mathcal {C} (X, Y) \text {和} f (C) \subset U \}.
$$

集合  $S(C, U)$  形成  $\mathcal{C}(X, Y)$  的某一个拓扑的子基，这个拓扑就称为紧致开拓扑（compact-open topology）。

根据定义易见，紧致开拓扑一般比点态收敛拓扑更细，是可以定义在整个空间  $Y^{X}$  上的。但我们关心的只是子空间  $\mathcal{C}(X, Y)$ ，所以只考虑这个空间。

定理46.8 设  $X$  是一个空间， $(Y, d)$  是一个度量空间。对于空间  $\mathcal{C}(X, Y)$  来说，紧致开拓扑与紧致收敛拓扑一致。

证 如果  $A$  是  $Y$  的一个子集， $\varepsilon > 0$ ，我们用  $U(A, \varepsilon)$  表示  $A$  的  $\varepsilon$ -邻域。如果  $A$  是紧致的， $V$  是包含  $A$  的一个开集，于是存在  $\varepsilon > 0$ ，使得  $U(A, \varepsilon) \subset V$ 。事实上，所求的  $\varepsilon$  就是函数  $d(a, X - V)$  的极小值。

首先，我们证明紧致收敛拓扑比紧致开拓扑细。设  $S(C, U)$  是紧致开拓扑的一个子基元素，而  $f$  是  $S(C, U)$  中的一个元素，由于  $f$  连续，所以  $f(C)$  是开集  $U$  的一个紧致子集。因此，我们可以选取  $\varepsilon$ ，使得  $f(C)$  的  $\varepsilon$ -邻域包含在  $U$  中，于是

$$
B _ {C} (f, \varepsilon) \subset S (C, U).
$$

我们证明紧致开拓扑比紧致收敛拓扑细。设  $f \in \mathcal{C}(X, Y)$ 。对于紧致收敛拓扑包含  $f$  的一个开集，则它包含一个形如  $B_{\mathbb{C}}(f, \varepsilon)$  的基元素，下面我们找出紧致开拓扑的一个包含  $f$  的基元素，使它包含于  $B_{\mathbb{C}}(f, \varepsilon)$  中。

$X$  的每一点  $x$  都有一个邻域  $V_{x}$ ，使得  $f(\bar{V}_{x})$  包含在  $Y$  的一个直径小于  $\varepsilon$  的开集  $U_{x}$  中。[例如，选取  $V_{x}$ ，使  $f(V_{x})$  包含在  $f(x)$  的  $\varepsilon / 4-$  邻域中，则  $f(\bar{V}_{x})$  包含在  $f(x)$  的  $\varepsilon / 3-$  邻域中，这个邻域的直径最多是  $2\varepsilon / 3$ .]用有限多个这种集合  $V_{x}$ ，譬如  $x = x_{1}, \cdots, x_{n}$  来覆盖  $C$ 。令  $C_{x} = \bar{V}_{x} \cap C$ ，于是  $C_{x}$  为紧致子集，并且基元素

$$
S \left(C _ {x _ {1}}, U _ {x _ {1}}\right) \cap \dots \cap S \left(C _ {x _ {n}}, U _ {x _ {n}}\right)
$$

包含  $f$  ，并且被  $B_{C}(f,\varepsilon)$  所包含.

推论46.9 设  $Y$  是一个度量空间。  $\mathcal{C}(X, Y)$  的紧致收敛拓扑与  $Y$  的度量无关。因此，若  $X$  是紧致的，则  $\mathcal{C}(X, Y)$  的一致拓扑与  $Y$  的度量无关。

紧致开拓扑的定义不涉及度量，这恰是它的一个有用的特征。同时它还满足“联合连续性”的要求。粗略地说就是， $f(x)$  不仅对单变量  $x$  是连续的，而且在变量  $x$  和  $f$  同时改变时，仍然是连续的。确切地说来，便是下面的定理。

定理46.10 设  $X$  是一个局部紧致的Hausdorff空间，  $\mathcal{C}(X,Y)$  有紧致开拓扑．映射

$$
e: X \times \mathcal {C} (X, Y) \longrightarrow Y
$$

定义为

$$
e (x, f) = f (x),
$$

它是连续的.

这个映射  $e$  称为赋值映射 (evaluation map).

证 给定  $X \times \mathcal{C}(X, Y)$  的一个点  $(x, f)$ ，设  $V$  是  $Y$  中包含像点  $e(x, f) = f(x)$  的一个开集，我们希望找到一个包含  $(x, f)$  的开集，使得  $e$  将其映射到  $V$  中。首先，应用  $f$  的连续性以及  $X$  是局部紧致的 Hausdorff 空间这一事实，可以选取一个包含  $x$  的开集  $U$ ，使得  $U$  有紧致的闭包  $\overline{U}$ ，并且  $f$  将  $\overline{U}$  映射到  $V$  中。考虑  $X \times \mathcal{C}(X, Y)$  中的开集  $U \times S(\overline{U}, V)$ 。它是包含  $(x, f)$  的一个开集，并且若  $(x', f')$  属于这个集合，则  $e(x', f') = f'(x')$  属于集合  $V$ 。

这个定理的一个推论如下，它在代数拓扑中是很有用的。

定义 如果给定了一个函数  $f: X \times Z \to Y$ ，我们便有一个相应的函数  $F: Z \to \mathcal{C}(X, Y)$ ，其定义为

$$
(F (z)) (x) = f (x, z).
$$

反之，如果给定  $F: Z \to \mathcal{C}(X, Y)$ ，那么这个等式又定义了与之相应的函数  $f: X \times Z \to Y$ 。我们称从  $Z$  到  $\mathcal{C}(X, Y)$  中的映射  $F$  是由  $f$  诱导的(induced by  $f$ )。

定理46.11 设  $X$  和  $Y$  是两个空间，赋予  $\mathcal{C}(X, Y)$  紧致开拓扑。若  $f: X \times Z \to Y$  是连续的，则由  $f$  诱导的映射  $F: Z \to \mathcal{C}(X, Y)$  也是连续的。进而，若  $X$  是局部紧致的Hausdorff空间，则其逆命题也成立。

证 我们先假设  $F$  是连续的， $X$  是一个局部紧致的 Hausdorff 空间，那么  $f$  是连续的。因为  $f$  等于复合

$$
X \times Z \xrightarrow {i _ {X} \times F} X \times \mathcal {C} (X, Y) \xrightarrow {e} Y,
$$

其中  $i_X$  是  $X$  上的恒等映射.

现在设  $f$  是连续的，为了证明  $F$  的连续性，我们取  $Z$  的一个点  $z_0$  和  $\mathcal{C}(X, Y)$  中的包含  $F(z_0)$  的一个子基元素  $S(C, U)$ 。下面寻找  $z_0$  的一个邻域  $W$ ，使得  $F$  可以将  $W$  映射到  $S(C, U)$  中。这样就完成了证明。

所谓  $F(z_0)$  属于  $S(C, U)$ ，即是说，对任意  $x \in C$ ，有  $(F(z_0))(x) = f(x, z_0)$  属于  $U$ 。也就是说  $f(C \times z_0) \subset U$ 。 $f$  的连续性蕴涵着  $f^{-1}(U)$  是  $X \times Z$  中包含  $C \times z_0$  的一个开集，因此

$$
f ^ {- 1} (U) \cap (C \times Z)
$$

是  $C \times Z$  中包含  $C \times z_0$  的开集。根据第26节中的管状引理可见，在  $Z$  中存在  $z_0$  的一个邻域  $W$ ，使得  $C \times W$  包含于  $f^{-1}(U)$ ，如图46.2所示。于是对于  $z \in W$  和  $x \in C$ ，有  $f(x, z) \in U$ 。从而  $F(W) \subset S(C, U)$ 。

![](60ac1411837ad87862747df8c1518dac8461fc7fbbfeeb37c60db299bd0e1e48.jpg)  
图46.2

我们来简略地讨论一下紧致开拓扑与同伦这个概念之间的关系，其中同伦将在代数拓扑中涉及.

如果  $f$  和  $\pmb{g}$  是从  $X$  到  $Y$  的两个连续映射，我们说  $f$  和  $\pmb{g}$  是同伦的，如果存在一个连续映射

$$
h: X \times [ 0, 1 ] \longrightarrow Y,
$$

使得对于所有的  $x \in X$  有  $h(x, 0) = f(x)$  和  $h(x, 1) = g(x)$ . 映射  $h$  称为  $f$  和  $g$  之间的一个同伦.

粗略地说，一个同伦就是从  $X$  到  $Y$  的映射构成的一个“连续单参数族”。更准确些讲，一个同伦  $h$  给出一个映射

$$
H: [ 0, 1 ] \longrightarrow \mathcal {C} (X, Y),
$$

对于每一个参数  $t \in [0, 1]$ ，它对应着从  $X$  到  $Y$  的一个连续映射。假设  $X$  是局部紧致的

Hausdorff 空间, 我们知道,  $h$  连续当且仅当  $H$  连续. 这就意味着连续映射  $f$  和  $g$  之间的一个同伦  $h$ , 恰好对应着函数空间  $\mathcal{C}(X, Y)$  中连接  $\mathcal{C}(X, Y)$  的点  $f$  和  $g$  的一条道路.

我们将在本书的第二部分更详细地研究同伦的概念.

## 练习


1. 证明：所有集合  $B_{C}(f, \epsilon)$  形成  $Y^{X}$  的某一个拓扑的基。  
2. 证明定理46.7.  
3. 证明有界函数  $f: \mathbb{R} \rightarrow \mathbb{R}$  构成的集合  $\mathcal{B}(\mathbb{R}, \mathbb{R})$  关于一致拓扑是  $\mathbb{R}^{\mathbb{R}}$  的闭集，但在紧致收敛拓扑下却不是。  
4. 考虑定义为

$$
f _ {n} (x) = x / n
$$

的连续函数序列  $f_{n}$  ：  $\mathbb{R}\to \mathbb{R}$  在定理46.7中提到的三个拓扑中，关于哪个拓扑是收敛的？对于第21节的习题9中所给定的序列，情况又如何呢？

5. 考虑定义为

$$
f _ {n} (x) = \sum_ {k = 1} ^ {n} k x ^ {k}
$$

的函数序列  $f_{n}$  ：  $(-1, 1) \to \mathbb{R}$

(a) 证明  $(f_n)$  关于紧致收敛拓扑是收敛的，并且极限函数是连续的。（这是关于幂级数的一个一般性结论。）  
(b) 证明  $(f_n)$  关于一致拓扑不收敛.

6. 证明：关于紧致开拓扑，如果  $Y$  是Hausdorff的，则  $\mathcal{C}(X, Y)$  也是Hausdorff的．如果  $Y$  是正则的，则  $\mathcal{C}(X, Y)$  也是正则的．[提示：如果  $\overline{U} \subset V$  ，则  $\overline{S(C, U)} \subset S(C, V)$ ]

7. 证明：如果  $Y$  是局部紧致的Hausdorff空间，只要全都使用紧致开拓扑，那么复合映射

$$
\mathcal {C} (X, Y) \times \mathcal {C} (Y, Z) \longrightarrow \mathcal {C} (X, Z)
$$

是连续的．[提示：如果  $g\circ f\in S(C,U)$  ，找出  $V$  ，使得  $f(C)\subset V$  和  $g(\overline{V})\subset U$  成立.]

8. 设  $\mathcal{C}'(X, Y)$  表示关于某拓扑  $\mathcal{T}$  的集合  $\mathcal{C}(X, Y)$ . 证明：如果赋值映射

$$
e: X \times \mathfrak {C} ^ {\prime} (X, Y) \longrightarrow Y
$$

连续，则  $\mathcal{T}$  包含紧致开拓扑．[提示：诱导映射  $E$  ：  $\mathcal{C}'(X,Y)\to \mathcal{C}(X,Y)$  是连续的.]

9. 这是定理 46.11 在商映射上的一个 (意外的) 应用. (参照第 29 节的习题 11.)

定理 如果  $p: A \to B$  是一个商映射，并且  $X$  是局部紧致的 Hausdorff 空间，那么  $i_X \times p: X \times A \to X \times B$  是一个商映射.

证明：

(a) 设  $Y$  是由  $i_X \times p$  诱导的商空间,  $q: X \times A \to Y$  是一个商映射. 证明存在一个连续的一一映射  $f: Y \to X \times B$ , 使得  $f \circ q = i_X \times p$ .  
(b) 设  $g = f^{-1}$ ， $G: B \to \mathcal{C}(X, Y)$  和  $Q: A \to \mathcal{C}(X, Y)$  分别是由  $g$  和  $q$  诱导的映射。证明  $Q = G \circ p$ .  
(c)证明  $Q$  是连续的．推证  $G$  是连续的，因此  $\pmb{g}$  是连续的.

*10. 一个空间称为局部紧致的，如果存在它的一个开覆盖，这个开覆盖中的每一个开集都包含于  $X$  的某一个紧致子集中。一个空间称为  $\sigma$ -紧致的（ $\sigma$ -compact），如果它能被可数多个这样的开集覆盖。

(a)证明：若  $X$  是局部紧致的，并且是第二可数的，则它是  $\sigma^{-}$  紧致的.  
(b) 设  $(Y, d)$  是一个度量空间。证明：如果  $X$  是  $\sigma$ -紧致的，那么对  $Y^X$  上的紧致收敛拓扑，存在一个度量使得若  $(Y, d)$  是完备的，则  $Y^X$  在此度量下也是完备的。[提示：设  $A_1, A_2, \cdots$  是  $X$  中的可数个紧致子空间构成的族，并且这些紧致子空间的内部构成了  $X$  的一个覆盖。用  $Y_i$  表示所有从  $A_i$  到  $Y$  的映射构成的集合，并赋予其一致拓扑。定义  $Y^X$  和积空间  $Y_1 \times Y_2 \times \cdots$  的一个闭子空间之间的一个同胚。]

11. 设  $(Y, d)$  是一个度量空间， $X$  是一个空间。定义  $\mathcal{C}(X, Y)$  的一个拓扑如下：给定  $f \in \mathcal{C}(X, Y)$  和  $X$  上的一个正的连续函数  $\delta: X \to \mathbb{R}_+$ ，令

$$
B (f, \delta) = \{g \mid d (f (x), g (x)) <   \delta (x), \text {对 于 所 有} x \in X \}.
$$

(a) 证明这些集合  $B(f, \delta)$  构成了  $\mathcal{C}(X, Y)$  的某个拓扑的一个基。将这个拓扑称为细拓扑 (fine topology)。  
(b)证明细拓扑包含一致拓扑.  
(c) 若  $X$  是紧致的，则细拓扑和一致拓扑是一致的。  
(d) 证明若  $X$  是离散的，则  $\mathcal{C}(X, Y) = Y^X$ ，并且细拓扑和箱拓扑一致.

# 第35节 Ascoli定理
## 35-1 Ascoli定理

我们现在来证明 Ascoli 定理的一般形式，它刻画了关于紧致收敛拓扑  $\mathcal{C}(X, Y)$  的紧致子空间。然而，这个证明涉及函数空间的三种标准拓扑，即点态收敛拓扑、紧致收敛拓扑和一致拓扑。

定理47.1[Ascoli 定理(Ascoli theorem)] 设  $X$  是一个空间， $(Y, d)$  是一个度量空间。赋予  $\mathcal{C}(X, Y)$  紧致收敛拓扑。设  $\mathcal{F}$  是  $\mathcal{C}(X, Y)$  的一个子集。

(a) 若  $\mathcal{F}$  关于  $d$  是等度连续的，并且集合

$$
\mathcal {F} _ {a} = \{f (a) \mid f \in \mathcal {F} \}
$$

对于每一个  $a \in X$  有紧致闭包，则  $\mathcal{F}$  包含于  $\mathcal{C}(X, Y)$  的一个紧致子空间中.

(b) 若  $X$  是一个局部紧致的 Hausdorff 空间，则逆命题成立.

证 (a) 的证明. 赋予  $Y^{X}$  积拓扑, 它与点态收敛拓扑是一致的. 从而  $Y^{X}$  是一个 Hausdorff 空间. 空间  $\mathcal{C}(X, Y)$  有紧致收敛拓扑, 它不是  $Y^{X}$  的子空间. 设  $\mathcal{G}$  是  $\mathcal{F}$  在  $Y^{X}$  中的闭包.

第一步．证明  $\mathcal{G}$  是  $Y^{X}$  的一个紧致子空间．给定  $a\in X$  ，令  $C_a$  表示  $\mathcal{F}_a$  在  $Y$  中的闭包．根据假设条件可见，  $C_a$  是  $Y$  的一个紧致子空间．集合  $\mathcal{F}$  包含于积空间

$$
\prod_ {a \in X} C _ {a},
$$

因为根据定义，这个积空间由满足以下条件的所有函数  $f: X \to Y$  构成：对于所有  $a$ ，有  $f(a) \in C_a$ . 根据 Tychonoff 定理，这个积空间是紧致的，它是  $Y^X$  的一个闭子空间. 因为  $\mathcal{G}$  是  $\mathcal{F}$  在  $Y^X$  中的闭包，所以  $\mathcal{G}$  包含于  $\Pi C_a$  中，并且是闭的．从而  $\mathcal{G}$  是紧致的.

第二步．证明  $\mathfrak{g}$  中的每一个函数都是连续的，并且  $\mathfrak{g}$  关于  $d$  是等度连续的.

给定  $x_0 \in X$  和  $\varepsilon > 0$ ，选取  $x_0$  的一个邻域  $U$ ，使得

$$
d (f (x), f (x _ {0})) <   \varepsilon / 3 \quad \text {对 于 所 有} f \in \mathcal {F} \text {和 所 有} x \in U. \tag {*}
$$

下面将证明对于所有  $g \in \mathcal{G}$  和  $x \in U$ ，有  $d(g(x), g(x_0)) < \varepsilon$ 。从而  $\mathcal{G}$  是等度连续的。

设  $g \in \mathcal{G}$ ,  $x$  是  $U$  的一个点. 定义  $V_x$  是  $\mathbf{Y}^X$  中所有元素  $h$  构成的一个开集, 其中  $h$  满足条件

$$
d (h (x), g (x)) <   \varepsilon / 3 \text {和} d (h (x _ {0}), g (x _ {0})) <   \varepsilon / 3. \tag {*}
$$

因为  $g$  属于  $\mathcal{F}$  的闭包，所以  $g$  的邻域  $V_{x}$  必然包含  $\mathcal{F}$  的一个元素  $f$  ，对于  $(\ast)$  和  $(\ast \ast)$  使用三角不等式，可见  $d(g(x), g(x_0)) < \varepsilon$

第三步．证明  $Y^{X}$  上的积拓扑和  $\mathcal{C}(X,Y)$  上的紧致收敛拓扑在子集  $\vartheta$  上是一致的.

一般地，紧致收敛拓扑要比积拓扑细。我们证明对于子集  $\mathcal{G}$ ，相反的蕴涵关系也成立。令  $g$  为  $\mathcal{G}$  的一个元素，令  $B_{C}(g, \varepsilon)$  是  $Y^{X}$  上紧致收敛拓扑的包含  $g$  的一个基元素，要找到  $Y^{X}$  上点态收敛拓扑的一个包含  $g$  的基元素  $B$ ，使得

$$
[ B \cap \mathscr {G} ] \subset [ B _ {C} (g, \varepsilon) \cap \mathscr {G} ].
$$

应用  $\mathcal{G}$  的等度连续性和  $C$  的紧致性，可以选出  $X$  的有限多个开集  $U_{1},\dots ,U_{n}$  覆盖  $C$  ，要求 $U_{1},\dots ,U_{n}$  分别包含点  $x_{1},\dots ,x_{n}$  ，并且对于每一个  $i$  ，有

$$
d (g (x), g (x _ {i})) <   \varepsilon / 3
$$

其中  $x \in U_i$ ， $g \in \mathcal{G}$ ．定义  $Y^X$  的基元素  $B$  为

$$
B = \{h \mid h \in Y ^ {X} \text {和} d (h \left(x _ {i}\right), g \left(x _ {i}\right)) <   \varepsilon / 3, i = 1, \dots , n \}.
$$

下面证明若  $h$  是  $B \cap \mathcal{G}$  中的一个元素，则  $h$  便属于  $B_{C}(g, \varepsilon)$ 。也就是证明，对于  $x \in C$  有  $d(h(x), g(x)) < \varepsilon$ 。给定  $x \in C$ ，选取  $i$  使得  $x \in U_{i}$ ，由于  $x \in U_{i}$  和  $g, h \in \mathcal{G}$ ，所以有

$$
d (h (x), h (x _ {i})) <   \varepsilon / 3   \text {和}   d (g (x), g (x _ {i})) <   \varepsilon / 3.
$$

由于  $h \in B$  ，所以

$$
d \left(h \left(x _ {i}\right), g \left(x _ {i}\right)\right) <   \varepsilon / 3.
$$

从而根据三角不等式可见  $d(h(x),g(x)) < \varepsilon$

第四步．完成证明．集合  $\mathcal{G}$  包含  $\mathcal{F}$  并且包含于  $\mathcal{C}(X,Y)$  ，并且它是  $Y^{X}$  关于积拓扑的一个紧致子空间．根据刚刚证明的结论，它也是  $\mathcal{C}(X,Y)$  关于紧致收敛拓扑的一个紧致子空间.

(b)的证明．设  $\mathcal{H}$  是  $\mathcal{C}(X,Y)$  中包含  $\mathcal{F}$  的一个紧致子空间．下面证明  $\mathcal{H}$  是等度连续的，并且对于每一个  $a\in X$  ，  $\mathcal{H}_a$  是紧致的．由此可见  $\mathcal{F}$  是等度连续的（由于  $\mathcal{F}\subset \mathcal{H}$  ），以及  $\mathcal{F}_a$  包含于  $Y$  的紧致子空间  $\mathcal{H}_a$  ，从而  $\overline{\mathcal{F}}_a$  是紧致的.

为了证明  $\mathcal{H}_a$  是紧致的，考虑以下映射的复合：

$$
j: \mathcal {C} (X, Y) \longrightarrow X \times \mathcal {C} (X, Y),
$$

其中  $j(f) = a \times f$ ，以及赋值映射

$$
e: X \times \mathcal {C} (X, Y) \longrightarrow Y,
$$

其中  $e(x \times f) = f(x)$ 。显然映射  $j$  是连续的，根据定理46.8和定理46.10可见，映射  $e$  也是连续的。复合映射  $e \circ j$  将  $\mathcal{H}$  映到  $\mathcal{H}_a$  中，因为  $\mathcal{H}$  是紧致的，所以  $\mathcal{H}_a$  也是紧致的。

现在我们来证明  $\mathcal{H}$  在  $a$  点关于度量  $d$  是等度连续的。设  $A$  是  $X$  的一个紧致子空间，包含  $a$  的一个邻域。下面只需证明  $\mathcal{C}(A, Y)$  的子集

$$
\mathcal {R} = \{f \mid A; f \in \mathcal {H} \}
$$

在  $a$  点处是等度连续的.

赋予  $\mathcal{C}(A, Y)$  紧致收敛拓扑，下面证明限制映射

$$
r: \mathcal {C} (X, Y) \longrightarrow \mathcal {C} (A, Y)
$$

是连续的．设  $f$  是  $\mathcal{C}(X,Y)$  中的一个元素，  $B = B_{c}(f\mid A,\varepsilon)$  是  $\mathcal{C}(X,Y)$  的包含  $f\mid A$  的一个基元素，其中  $C$  是  $A$  的一个紧致子空间．那么  $C$  是  $X$  的一个紧致子空间，并且  $\pmb{r}$  将  $\mathcal{C}(X,Y)$  中 $f$  的邻域  $B_{\mathrm{C}}(f,\varepsilon)$  映到  $B$  中.

映射  $r$  将  $\mathcal{H}$  映到  $\mathcal{R}$  上．因为  $\mathcal{H}$  是紧致的，所以  $\mathcal{R}$  也是紧致的． $\mathcal{R}$  是  $\mathcal{C}(A, Y)$  的一个子空间，因为  $A$  是紧致的，紧致收敛拓扑和一致收敛拓扑在  $\mathcal{C}(A, Y)$  上是一致的．根据定理45.1可见， $\mathcal{R}$  关于  $\mathcal{C}(A, Y)$  的一致度量是完全有界的．从而根据引理45.2可见， $\mathcal{R}$  相对于度量 $d$  是等度连续的.

至于 Ascoli 定理的更为一般的形式可以在 [K] 或 [Wd] 中找到。在那里并没有要求 Y 是一个度量空间，仅仅假定它有所谓的一致结构。这种一致结构是度量概念的一种推广。

Ascoli 定理在分析中有很多应用, 这已超出本书的范围. 可以在 [K-F] 中找到一些这样的应用.

## 练习

1. 以下所列举的  $\mathcal{C}(\mathbb{R},\mathbb{R})$  的一些子集中哪些是点态有界的？哪些是等度连续的？

(a)族  $\{f_n\}$ ，其中  $f_{n}(x) = x + \sin nx$  
(b)族  $\{g_n\}$ ，其中  $g_{n}(x) = n + \sin x$  
(c)族  $\{h_n\}$ ，其中  $h_n(x) = |x|^{1 / n}$ .  
(d)族  $\{k_n\}$ ，其中  $k_{n}(x) = n\sin (x / n)$

2. 证明：

定理 若  $X$  是一个局部紧致的 Hausdorff 空间，则  $\mathcal{C}(X, \mathbb{R}^n)$  关于紧致收敛拓扑的子空间  $\mathcal{F}$  有紧致闭包，当且仅当在  $\mathbb{R}^n$  的任意一个标准度量下， $\mathcal{F}$  是点态收敛的并且等度连续的。

3. 证明：当  $X$  是一个Hausdorff空间时，Ascoli定理的一般形式蕴涵经典形式(定理45.4).  
4. 证明：

定理(Arzela 定理, 一般形式). 设  $X$  是一个  $\sigma$ -紧致的 Hausdorff 空间,  $f_{n}: X \to \mathbb{R}^{k}$  是一个函数序列. 若  $\{f_{n}\}$  是点态有界的和等度连续的, 则序列  $f_{n}$  存在一个子序列, 它关于紧致收敛拓扑收敛到一个连续函数.

[提示：证明  $\mathcal{C}(X,\mathbb{R}^k)$  是第一可数的.]

5. 设  $(Y, d)$  是一个度量空间， $f_n: X \to Y$  是一个连续函数序列， $f: X \to Y$  是一个函数（不必是连续的）。设关于点态收敛拓扑  $f_n$  收敛到  $f$ 。证明，若  $\{f_n\}$  是等度连续的，则  $f$  是连续的，并且  $f_n$  关于紧致收敛拓扑收敛到  $f$ 。
