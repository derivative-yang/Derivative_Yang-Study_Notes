
# 第36节 Baire空间
## 36-1 Baire空间
本章我们介绍一类称为Baire空间的拓扑空间．要陈述定义Baire空间的条件并不容易，但它却在分析学和拓扑学中有广泛应用．我们所学过的空间大多数都是Baire空间．例如，如果一个Hausdorff空间是紧致的或者是局部紧致的，那么它便是一个Baire空间．如果一个可度量化的空间  $X$  是拓扑完备的，即存在  $X$  的一个度量，关于这个度量  $X$  是完备的，那么它便是一个Baire空间
因此，从  $X$  到  $\mathbb{R}^n$  的所有连续函数构成的空间  $\mathcal{C}(X, \mathbb{R}^n)$  在一致度量下是完备的，可见它关于一致拓扑是一个Baire空间。这个结论有一系列有趣的应用。
其中一个应用就是我们将在第49节中给出的关于连续却处处不可微的实值函数存在性的证明
另一个应用出现在拓扑学的一个分支维数论中。第50节中我们将定义拓扑维数的概念，它源自于Lebesgue。我们将证明一个经典的定理：每一个拓扑维数为  $m$  的紧致可度量化空间，都可以嵌入到维数为  $N = 2m + 1$  的欧氏空间  $\mathbb{R}^N$  中。由此可见，每一个  $m$ -流形都可以嵌入到  $\mathbb{R}^{2m + 1}$  中。这就推广了第36节中证明的嵌入定理
在本章中，我们假设读者已熟悉完备度量空间(第43节)．当学习维数论的时候，将要用到第36节(流形的嵌入)以及一些线性代数的内容


就像本书中所引入的许多条件那样，确定一个空间是Baire空间的条件也是“很不自然”的，但是我们只能暂时先忍耐一下。

在本节中，我们将定义Baire空间，并指出两类重要的空间，即完备度量空间和紧致的Hausdorff空间，它们都包含在Baire空间类中．然后再给出一些应用．尽管这些应用并没有使Baire条件显得更自然一些，但至少说明Baire空间是一个有用的工具．事实上，在分析学与拓扑学中它确实是一个十分有用而巧妙的工具.

定义 我们知道：空间  $X$  的子集  $A$  的内部，是所有包含于  $A$  的开集之并。如果除了空集， $A$  不包含  $X$  的任何其他开集，我们就说  $A$  有空内部(empty interior)。等价地，如果  $A$  的每一个点都是  $A$  的补的一个极限点，也就是说  $A$  的补在  $X$  中稠密，我们就说  $A$  有空内部。

例1有理数集  $\mathbb{Q}$  作为  $\mathbb{R}$  的子集有空内部，但闭区间[0，1]内部非空．区间[0，1]  $\times 0$  作为平面  $\mathbb{R}^2$  的子集有空内部，子集  $\mathbb{Q}\times \mathbb{R}$  也有空内部.

定义 空间  $X$  称为一个Baire空间(Baire space)，如果它满足以下条件：给定  $X$  的闭集的任意可数族  $\{A_{n}\}$ ，如果其中每一个集合在  $X$  中有空内部，那么它们的并  $\bigcup A_{n}$  在  $X$  中也有空内部。

例2 有理数空间  $\mathbb{Q}$  不是Baire空间，因为  $\mathbb{Q}$  的单点集为闭集，并且在  $\mathbb{Q}$  中有空内部，但  $\mathbb{Q}$  是它的单点子集的可数并.

另一方面，空间  $\mathbb{Z}_{+}$  是一个Baire空间．因为  $\mathbb{Z}_{+}$  的任意子集是开集，所以除了空集外， $\mathbb{Z}_{+}$  的任何子集都有非空内部，这就是说， $\mathbb{Z}_{+}$  绝对满足Baire条件.

更一般地，作为完备度量空间， $\mathbb{R}$  的任意闭子空间是一个Baire空间．出人意料的是  $\mathbb{R}$  中的无理数集也是一个Baire空间，见习题6.

这个术语最初由Baire(R. Baire)用在与“范畴”一词有关的概念之中。空间  $X$  的子集  $A$  称为  $X$  中的第一范畴集，如果它包含于具有空内部的  $X$  的可数个闭集的并之中，否则称  $A$  是  $X$  中的第二范畴集。使用这一术语，我们可以说：

空间  $X$  是一个Baire空间当且仅当  $X$  中的任意非空开集是第二范畴集.

在本书中，我们不使用“第一范畴集”与“第二范畴集”这两个词.

上述定义是Baire空间的“闭集定义”，还有一个借助于开集的定义方式也经常使用。参见以下引理。

引理48.1  $X$  是一个Baire空间当且仅当  $X$  中开集的任意可数族  $\{U_n\}$ ，若每一个  $U_n$  在  $X$  中稠密，则交  $\bigcap U_n$  也在  $X$  中稠密。

证 我们说过，集合  $C$  在  $X$  中稠密是指  $\bar{C} = X$ 。该引理可以立刻由下面两条推出：

(1)  $A$  是  $X$  中的一个闭集当且仅当  $X - A$  是  $X$  中的一个开集.

(2)  $B$  在  $X$  中有空内部当且仅当  $X - B$  在  $X$  中稠密.

有许多定理给出了确定一个空间是Baire空间的条件．其中最重要的一个定理如下：

定理48.2[Baire范畴定理(Baire category theorem)] 若  $X$  是一个紧致的Hausdorff空间或者是一个完备度量空间，则  $X$  是一个Baire空间。

证 给定  $X$  的闭集的一个可数族  $\{A_{n}\}$ ，其中每一个  $A_{n}$  有空内部。我们证明它们的并  $\bigcup A_{n}$  在  $X$  中也有空内部。为此，任意给定  $X$  的一个非空开集  $U_{0}$ ，我们必须找出一点  $x$ ，它属于  $U_{0}$ ，但不属于任何一个  $A_{n}$ 。

首先考虑集合  $A_{1}$ 。根据假定， $A_{1}$  不包含  $U_{0}$ ，因此可以选出一点  $y$ ，它属于  $U_{0}$ ，但不在  $A_{1}$  中。由于  $A_{1}$  是闭集， $X$  是正则的，所以可以选取  $y$  的一个邻域  $U_{1}$ ，使得

$$
\bar {U} _ {1} \cap A _ {1} = \varnothing ,
$$

$$
\bar {U} _ {1} \subset U _ {0},
$$

如果  $X$  是一个度量空间，还可以把  $U_{1}$  选得足够小，使其直径小于1.

一般地，给定非空开集  $U_{n - 1}$  ，可以选取  $U_{n - 1}$  的一个点，使它不在闭集  $A_{n}$  中，然后选取这个点的一个邻域  $U_{n}$  ，使得

$$
\bar {U} _ {n} \cap A _ {n} = \varnothing ,
$$

$$
\bar {U} _ {n} \subset U _ {n - 1},
$$

$\mathrm{diam}U_{n} < 1 / n$  ，当  $X$  是度量空间时.

我们断言  $\cap \overline{U}_n$  非空．根据这一结论立即可见定理成立．因为若  $x$  是  $\cap \overline{U}_n$  的一个点，则由于  $\overline{U}_1\subset U_0$  ，可见  $x$  属于  $U_{0}$  ．由于对于每一个  $n$  ，  $\overline{U}_n$  与  $A_{n}$  无交，所以  $x$  不属于  $A_{n}$

证明  $\cap \overline{U}_n$  非空可分成两部分，取决于  $X$  是紧致的Hausdorff空间还是完备度量空间．如果  $X$  一个是紧致的Hausdorff空间，考虑  $X$  的非空子集的一个套序列  $\overline{U}_1\supset \overline{U}_2\supset \dots$  ，族  $\{\overline{U}_n\}$  满

足有限交性质，由于  $X$  是紧致的，  $\bigcap \overline{U}_n$  必然非空.

如果  $X$  是一个完备度量空间，则可以应用以下引理完成定理的证明.

引理48.3 设  $C_1 \supset C_2 \supset \cdots$  是完备度量空间  $X$  中的一个非空闭集的套序列。若  $\mathrm{diam} C_n \to 0$ ，则  $\bigcap C_n \neq \emptyset$ 。

证 这个引理在第43节的习题中曾出现过，这里给出证明。对于每一个  $n$ ，选取  $x_{n} \in C_{n}$ 。因为对于  $n$ ， $m \geqslant N$ ，有  $x_{n}$ ， $x_{m} \in C_{N}$ ，并且对任意给定的  $\epsilon > 0$ ，可以选取充分大的  $N$ ，使得  $C_{N}$  的直径小于  $\epsilon$ ，所以序列  $(x_{n})$  是一个Cauchy序列。假定  $(x_{n})$  收敛于  $x$ ，则对于任意给定的  $k$ ，子序列  $x_{k}$ ， $x_{k+1}$ ，…也收敛于  $x$ 。于是， $x$  必定属于  $\bar{C}_{k} = C_{k}$ ，因此  $x \in \bigcap C_{k}$ 。

这里有Baire空间理论的一个应用，本节后面我们还将给出更多的应用。这个应用有些意思但不深奥，它涉及的是一个学生可能会问到的关于收敛的连续函数序列的问题。

设  $f_{n}\colon [0,1]\to \mathbb{R}$  是连续函数的一个序列，对于每一个  $x\in [0,1]$ ，有  $f_{n}(x)\rightarrow f(x)$ ．已有例子说明极限函数  $f$  未必是连续的．但人们想知道的是  $f$  到底是如何不连续的呢？例如，它是处处不连续的吗？答案是否定的．我们将要证明  $f$  必定在[0，1]的无限多个点处连续．事实上，所有使得  $f$  连续的点构成的集合在[0，1]中稠密.

为证明这个结论，需要以下引理

* 引理 48.4 Baire 空间  $X$  的任何一个开子空间  $Y$  是一个 Baire 空间.

证设  $A_{n}$  是  $Y$  中有空内部的闭集的一个可数族，下面证明  $\cup A_{n}$  在  $Y$  中有空内部.

设  $\overline{A}_n$  是  $A_{n}$  在  $X$  中的闭包，则  $\overline{A}_n\cap Y = A_n$  ．于是，  $\overline{A}_n$  在  $X$  中有空内部．因为若  $U$  是  $X$  中包含于  $\overline{A}_n$  的一个非空开集，则  $U$  必定与  $A_{n}$  相交，这导致  $U\cap Y$  是  $Y$  中包含在  $A_{n}$  中的一个非空开集，与假设矛盾.

若集合  $A_{n}$  的并包含着  $Y$  中的一个非空开集  $W$ ，则  $\overline{A}_{n}$  的并也包含着  $W$ 。由于  $Y$  在  $X$  中是开的，所以  $W$  在  $X$  中也是开的。但是每一个集合  $\overline{A}_{n}$  在  $X$  中有空内部，这与  $X$  是一个Baire空间矛盾。

* 定理 48.5 设  $X$  是一个空间， $(Y, d)$  是一个度量空间。设  $f_n: X \to Y$  是一个连续函数序列，使得对于所有的  $x \in X$ ，有  $f_n(x) \to f(x)$ ，其中  $f: X \to Y$ 。如果  $X$  是一个 Baire 空间，那么使得  $f$  连续的点构成的集合在  $X$  中稠密。

证 给定正整数  $N$  和  $\epsilon > 0$  ，定义

$$
A _ {N} (\varepsilon) = \{x \mid d (f _ {n} (x), f _ {m} (x)) \leqslant \varepsilon , \text {对 于 所 有} n, m \geqslant N \}.
$$

注意， $A_{N}(\varepsilon)$  在  $X$  中是闭的．因为根据  $f_{n}$  和  $f_{m}$  的连续性可见，满足  $d(f_n(x),f_m(x))\leqslant \varepsilon$  的点的集合是  $X$  的一个闭集，并且对于所有  $n$  ，  $m\geqslant N$  ，  $A_{N}(\varepsilon)$  是这些集合的交①.

对于固定的  $\varepsilon$  ，考虑集合  $A_{1}(\varepsilon)\subset A_{2}(\varepsilon)\subset \dots$  ，这些集合的并为  $X$  ，因为任意给定  $x_0\in X$  ，由于  $f_{n}(x_{0})\to f(x_{0})$  可得序列  $f_{n}(x_{0})$  是一个Cauchy序列，因此对于某一个  $N$  ，有  $x_0\in A_N(\varepsilon)$

现在，设

$$
U (\varepsilon) = \bigcup_ {N \in \mathbf {Z} _ {+}} \operatorname {I n t} A _ {N} (\varepsilon).
$$

我们来证明两件事情：

(1)  $U(\varepsilon)$  是  $X$  中的一个稠密开集.

(2)函数  $f$  在集合

$$
C = U (1) \cap U (1 / 2) \cap U (1 / 3) \cap \dots
$$

的每一点处都连续.

由此推出，本定理在  $X$  是Baire空间的假设下成立.

为了证明  $U(\varepsilon)$  在  $X$  中是稠密的，需要证明对于  $X$  的任意一个非空开集  $V$  ，存在  $N$  使得 $V\cap \operatorname {Int}A_N(\varepsilon)$  是非空的．为此，我们先注意对每一个  $N$  ，  $V\cap A_{N}(\varepsilon)$  在  $V$  中是闭的．因为根据前述引理可见  $V$  是一个Baire空间，所以至少存在一个这种集合，不妨设为  $V\cap A_M(\varepsilon)$  ，必包含  $V$  中的一个非空开集  $W$  ，因为  $V$  在  $X$  中是开的，所以  $W$  也是  $X$  中的开集．因此，它包含于  $\operatorname {Int}A_M(\varepsilon)$

现在我们来证明，若  $x_0 \in C$ ，则  $f$  在点  $x_0$  处连续。给定  $\varepsilon > 0$ ，我们来找  $x_0$  的一个邻域  $W$ ，使得对于  $x \in W$ ， $d(f(x), f(x_0)) < \varepsilon$ 。

首先，选取  $k$  使得  $1 / k < \varepsilon /3$  ，因为  $x_0\in C$  ，所以  $x_0\in U(1 / k)$  ，因此存在某一个  $N$  ，使得 $x_0\in \mathrm{Int}A_N(1 / k)$  ，最后，由  $f_{N}$  的连续性可以找到  $x_0$  的一个邻域  $W$  包含于  $A_{N}(1 / k)$  ，使得

$$
d (f _ {N} (x), f _ {N} (x _ {0})) <   \varepsilon / 3, \quad \text {对 于} x \in W. \tag {*}
$$

根据  $W\subset A_N(1 / k)$  可见，

$$
d (f _ {n} (x), f _ {N} (x)) \leqslant 1 / k, \quad {\text {对 于}} n \geqslant N {\text {和}} x \in W.
$$

令  $n\to \infty$  ，我们得到不等式

$$
d (f (x), f _ {N} (x)) \leqslant 1 / k <   \varepsilon / 3, \quad \text {对 于} x \in W. \tag {*}
$$

特别地，因为  $x_0 \in W$  ，我们有

$$
d \left(f \left(x _ {0}\right), f _ {N} \left(x _ {0}\right)\right) <   \varepsilon / 3. \tag {*} * * *
$$

对于  $(\ast)$  、  $(\ast \ast)$  和  $(\ast \ast \ast)$  应用三角不等式，便得到结论.

## 练习

1. 设  $X$  等于可数并  $\bigcup B_{n}$ 。证明：如果  $X$  是一个非空的 Baire 空间，则至少存在一个集合  $\overline{B}_{n}$  有非空内部。  
2. 根据 Baire 范畴定理可见  $\mathbb{R}$  不能写成可数个具有空内部的闭子集的并。证明如果不要求这些集合是闭的，那么上面的结论不成立。  
3. 证明每一个局部紧致的 Hausdorff 空间是 Baire 空间.  
4. 证明：若  $X$  中的每一个点  $x$  都有一个邻域是 Baire 空间，则  $X$  是 Baire 空间。[提示：应用 Baire 条件的开集形式。]  
5. 证明：若  $Y$  为  $X$  中的一个  $G_{\delta}$  集，并且  $X$  是紧致的Hausdorff空间或完备度量空间，则  $Y$  在子空间拓扑下是一个Baire空间．[提示：假定  $Y = \bigcap W_{n}$ ，其中  $W_{n}$  在  $X$  中是开的，并假

定  $B_{n}$  是  $\pmb{Y}$  中具有空内部的一个闭集．给定  $X$  的一个开集  $U_{0}$  ，使得  $U_{0} \cap Y \neq \emptyset$  ，找出  $X$  中一个开集序列  $U_{n}$  ，满足  $U_{n} \cap Y \neq \emptyset$  ，并使得

$$
\bar {U} _ {n} \subset U _ {n - 1},
$$

$$
\bar {U} _ {n} \cap \bar {B} _ {n} = \varnothing ,
$$

$\mathrm{diam}U_{n} < 1 / n$  ，当  $X$  是度量空间时，

$$
\bar {U} _ {n} \subset W _ {n}. ]
$$

6. 证明无理数集是一个 Baire 空间.

7. 定理 若  $D$  是  $\mathbb{R}$  的一个可数稠密子集，则没有函数  $f: \mathbb{R} \rightarrow \mathbb{R}$  恰在  $D$  的所有点处连续。

(a)证明：如果  $f$  ：  $\mathbb{R}\to \mathbb{R}$  ，那么使得  $f$  连续的所有点构成的集合  $C$  是  $\mathbb{R}$  中的一个  $G_{\delta}$  集.［提示：设  $U_{n}$  是  $\mathbb{R}$  中所有满足  $\mathrm{diam}f(U) < 1 / n$  的开集  $U$  的并，证明  $C = \bigcap U_{n}$  .]

(b) 证明  $D$  不是  $\mathbb{R}$  中的一个  $G_{\delta}$  集. [提示: 设  $D = \bigcap W_{n}$ , 其中  $W_{n}$  在  $\mathbb{R}$  中是开的. 对于  $d \in D$ , 令  $V_{d} = \mathbb{R} - \{d\}$ . 证明  $W_{n}$  和  $V_{d}$  都在  $\mathbb{R}$  中稠密.]

8. 设  $f_{n}$  是一个连续函数序列， $f_{n}:\mathbb{R}\to \mathbb{R}$ ，使得对任意  $x\in \mathbb{R}$ ，有  $f_{n}(x)\rightarrow f(x)$ 。证明  $f$  在  $\mathbb{R}$  中的不可数多个点处连续。

9. 设  $g: \mathbb{Z}_{+} \to \mathbb{Q}$  是一个一一映射，令  $x_{n} = g(n)$ 。定义  $f: \mathbb{R} \to \mathbb{R}$  如下：

$f(x_{n}) = 1 / n$  ， 对于  $x_{n}\in \mathbb{Q}$

$f(x) = 0$  ，对于  $x\notin \mathbb{Q}$

证明  $f$  在每一个无理数处连续，在每一个有理数处不连续．你能找到一个连续函数序列  $f_{n}$  收敛到  $f$  吗？

10. 证明以下结论：

定理（一致有界原理）设  $X$  是一个完备度量空间， $\mathcal{F}$  是  $\mathcal{C}(X, \mathbb{R})$  的一个子集，使得对于每一个  $a \in X$ ，集合

$$
\mathcal {F} _ {a} = \{f (a) \mid f \in \mathcal {F} \}
$$

有界，则存在  $X$  中的一个非空开集  $U$ ，使得  $\mathcal{F}$  中的函数在  $U$  上一致有界，即存在一个数  $M$ ，使得对于所有的  $x \in U$  及所有  $f \in \mathcal{F}$ ，有  $|f(x)| \leqslant M$ 。[提示：令  $A_N = \{x; |f(x)| \leqslant N\}$  对于所有  $f \in \mathcal{F}\}.$ ]

11. 判定  $\mathbb{R}_t$  是否为Baire空间  
12. 证明  $\mathbb{R}^j$  在箱拓扑、积拓扑以及一致拓扑下都是 Baire 空间.  
*13. 设  $X$  是一个拓扑空间,  $Y$  是一个完备度量空间. 证明  $\mathcal{C}(X, Y)$  在细拓扑(参见第46节的习题11)下是一个Baire空间. [提示: 给定基元素  $B(f_{i}, \delta_{i})$  使得  $\delta_{1} \leqslant 1$ ,  $\delta_{i+1} \leqslant \delta_{i}/3$ , 并且  $f_{i+1} \in B(f_{i}, \delta_{i}/3)$ , 证明

$$
\bigcap B \left(f _ {i}, \delta_ {i}\right) \neq \varnothing . ]
$$

# 第37节 一个无处可微函数
## 37-1 一个无处可微函数
我们证明数学分析中的下述结论.

> [!QUOTE] THM
> $h: [0, 1] \to \mathbb{R}$  是一个连续函数。任意给定  $\varepsilon > 0$ ，存在一个函数 $g: [0, 1] \to \mathbb{R}$ ，对于所有的  $x$ ，有  $|h(x) - g(x)| < \varepsilon$ ，使得  $g$  连续并且无处可微

令  $I = [0,1]$  ，在度量
$$\rho (f, g) = \max  \left\{\mid f (x) - g (x) \mid \right\}$$
下，考虑从  $I$  到  $\mathbb{R}$  的连续函数空间  $\mathcal{C} = \mathcal{C}(I, \mathbb{R})$ 。这个空间是一个完备度量空间，因此是一个Baire空间。对于每一个  $n$ ，我们将确定  $\mathcal{C}$  的一个子集  $U_{n}$ ，使得  $U_{n}$  是  $\mathcal{C}$  中的一个稠密开集，同时还具有以下性质：属于交
$$
\bigcap_ {n \in \mathbf {Z} _ {+}} U _ {n}
$$
的函数是无处可微的．因为  $\mathcal{C}$  是一个Baire空间，根据引理48.1，这个交在  $\mathcal{C}$  中稠密．因此，给定  $h$  和  $\varepsilon$  ，这个交必然包含一个函数  $g$  ，使得  $\rho (h,g) <   \varepsilon$  ，定理由此得证
关键在于恰当地选取  $U_{n}$ ．首先取一个函数  $f$ ，并考虑它的差商．给定  $x \in I$  及  $0 < h \leqslant \displaystyle\frac{1}{2}$ ，考虑表达式
$$
\left| \frac {f (x + h) - f (x)}{h} \right| \quad \text {和} \quad \left| \frac {f (x - h) - f (x)}{- h} \right|
$$

因为  $h \leqslant \displaystyle\frac{1}{2}$ ， $x + h$  和  $x - h$  这两个数中至少有一个属于  $I$ ，所以上面两个表达式中至少有一个是有意义的。如果两个都有意义，则用  $\Delta f(x, h)$  表示其中较大的一个，否则就用它表示有意义的那一个。如果  $f$  在点  $x$  处的导数  $f'(x)$  存在，它等于这个差商的极限，所以
$$
\mid f ^ {\prime} (x) \mid = \lim  _ {h \rightarrow 0} \Delta f (x, h)
$$

我们的目的是找到一个连续函数，使得上面的极限不存在。确切地说，就是构造  $f$ ，对给定的  $x$ ，存在一个数列  $h_n$  收敛到 0，而同时  $\Delta f(x, h_n)$  变得任意大。这就为我们提供了确定集合  $U_{n}$  的一个思路．任意给定一个正数  $h \leqslant \displaystyle\frac{1}{2}$  ，令
$$
\Delta_ {h} f = \inf  \{\Delta f (x, h) \mid x \in I \}
$$
对于  $n \geqslant 2$  ，我们定义  $U_{n}$  ，使得一个函数  $f$  属于  $U_{n}$  当且仅当对某一个正数  $h \leqslant 1 / n$  ，有  $\Delta_h f > n$
例1 给定  $\alpha > 0$ 。函数  $f: [0, 1] \to \mathbb{R}$  定义为  $f(x) = 4\alpha x (1 - x)$ ，其图像是一条抛物线。容易验证，当  $h =\displaystyle\frac{1}{4}$  时，对于任意  $x$ ，有  $\Delta f(x, h) \geqslant \alpha$ 。从几何上来说，就是对于每一个  $x$ ，如下图所示，抛物线的两条割线中至少有一条，其斜率的绝对值不小于  $\alpha$ 
<img src ="2f41e99207b95ebb5737dca11d59ab57d3c1c7a65bcccc974607420a876b1ae0.jpg" width = 100>
因此，如果  $\alpha > 4$ ，那么函数  $f$  属于  $U_4$ 。下图中描述的函数  $g$  满足条件：对于任意  $h \leqslant \displaystyle\frac{1}{4}$ ，有  $\Delta g(x, h) \geqslant \alpha$ 。因此
<img src ="4cbba933a369f1e4cb22f697f08091e04ebf3e479dcb7b00ed9d8c2648840d03.jpg" width = 100><img src ="307d37c041a59489b98b7da48fe63483a994ff220b638660206745a185a88e8e.jpg" width = 100>
如果  $\alpha > n$ ，则  $g$  属于  $U_{n}$ 。函数  $k$  对于任意  $h \leqslant 1/8$ ，满足  $k(x, h) \geqslant \alpha$ ，因此对  $\alpha > n$ ， $k$  属于  $U_{n}$ 
现在证明关于集合  $U_{n}$  的以下结论：
(1)  $\bigcap U_{n}$  由无处可微函数构成．设  $f\in \bigcap U_n$  ，下面证明对给定的  $x\in [0,1]$  ，极限

$$
\lim  \Delta f (x, h)
$$

不存在：给定  $n$  ，根据  $f\in U_{n}$  可见，存在一个数  $h_n$  ，  $0 < h_n\leqslant 1 / n$  ，使得

$$
\Delta f (x, h _ {n}) > n.
$$

因此序列  $(h_n)$  收敛到0，但序列  $(\Delta f(x, h_n))$  不收敛．因此， $f$  在点  $x$  处不可微.
(2)  $U_{n}$  在  $\mathcal{C}$  中是开的．设  $f\in U_n$  ，我们找  $f$  的一个  $\delta$  -邻域，使得它包含在  $U_{n}$  中．因为 $f\in U_{n}$  ，故存在  $h$  ，  $0 <   h\leqslant 1 / n$  ，使得  $\Delta_h f > n$  令  $M = \Delta_h f$  ，设
$$
\delta = h (M - n) / 4.
$$
我们断言，若  $g$  是一个满足  $\rho(f, g) < \delta$  的函数，则对于所有的  $x \in I$ ，有
$$
\Delta g (x, h) \geqslant \frac {1}{2} (M + n) > n,
$$
从而  $g\in U_{n}$
为证明上述论断，我们先假设  $\Delta f(x, h)$  等于商  $|f(x + h) - f(x)| / h$ 。计算
$$
\begin{array}{l}\displaystyle \left| \frac {f (x + h) - f (x)}{h} - \frac {g (x + h) - g (x)}{h}| \right. \\ = (\displaystyle\frac{1}{h}) \left| [ f (x + h) - g (x + h) ] - [ f (x) - g (x) ] \right| \leqslant \displaystyle\frac{2 \delta }{h} = \displaystyle\frac{M - n}{2} \\ \end{array}
$$
如果第一个差商的绝对值至少为  $M$  ，那么第二个差商的绝对值至少为
$$
M - \frac {1}{2} (M - n) = \frac {1}{2} (M + n)
$$
若  $\Delta f(x, h)$  等于另一个差商，可做相似的讨论。

(3)  $U_{n}$  在  $\mathcal{C}$  中稠密．我们需要证明，对于  $\mathcal{C}$  中给定的  $f$  、给定的  $\varepsilon >0$  以及给定的  $n$  ，可以找到  $U_{n}$  中的一个元素  $g$  ，使它包含于  $f$  的  $\varepsilon$ -邻域中.

选取  $\alpha > n$ ，我们将把  $g$  构造为一个“分段线性”函数，也就是说， $g$  的图像由一条折线组成，其中  $g$  的图形中的每一条线段的斜率的绝对值不小于  $\alpha$ 。由此立即得出函数  $g$  属于  $U_{n}$ 。因为令

$$
0 = x _ {0} <   x _ {1} <   x _ {2} <   \dots <   x _ {k} = 1
$$

是区间[0，1]的一个分拆，使得  $\pmb{g}$  在每一个子区间  $I_{i} = [x_{i - 1},x_{i}]$  上的限制是一个线性函数.再选择  $h$  ，使得  $h\leqslant 1 / n$  并且

$$
h \leqslant \frac {1}{2} \min  \left\{\mid x _ {i} - x _ {i - 1} \mid ; i = 1, \dots , k \right\}.
$$

如果  $x$  在[0，1]中，则  $x$  必属于某一个子区间  $I_{i}$  ，如果  $x$  属于子区间  $I_{i}$  的前半段，则  $x + h$  也属于  $I_{i}$  ，并且  $(g(x + h) - g(x)) / h$  等于线性函数  $g\mid I_i$  的斜率．类似地，如果  $x$  属于子区间  $I_{i}$  的后半段，那么  $x - h$  属于  $I_{i}$  ，并且  $(g(x - h) - g(x)) / (-h)$  等于线性函数  $g\mid I_{i}$  的斜率．无论在哪一种情况下，总有  $\Delta g(x,h)\geqslant \alpha$  ，从而  $g\in U_n$

现在给定  $f, \varepsilon$  和  $\alpha$ ，下面说明如何构造上述分段线性函数  $g$ 。首先，由  $f$  的一致连续性，选择区间的一个分拆

$$
0 = t _ {0} <   t _ {1} <   \dots <   t _ {m} = 1
$$

使得  $f$  在这个分拆中的每一个子区间  $[t_{i-1}, t_i]$  上的变化最多为  $\varepsilon / 4$ 。对于每一个  $i = 1, \dots, m$ ，选取一点  $a_i \in (t_{i-1}, t_i)$ ，然后定义一个分段线性函数  $g_1$  为

$$
g _ {1} (x) = \left\{ \begin{array}{l l} f (t _ {i - 1}) & \text {如 果} x \in [ t _ {i - 1}, a _ {i} ] \\ f (t _ {i - 1}) + m _ {i} (x - a _ {i}) & \text {如 果} x \in [ a _ {i}, t _ {i} ], \end{array} \right.
$$

其中  $m_{i} = (f(t_{i}) - f(t_{i - 1})) / (t_{i} - a_{i})$  ，  $f$  和  $\pmb{g}_{1}$  的图像如图所示
<img src="71138eea90dcb0e32459ee3b22885534fb0af2daedf7b1e6819b309e643ce019.jpg" width =260>


对点  $a_{i}$  的选取要自由些．如果  $f(t_{i})\neq f(t_{i - 1})$  ，那么我们可以要求  $a_{i}$  充分靠近  $t_i$  ，使得
$$
t _ {i} - a _ {i} <   \frac {\left| f \left(t _ {i}\right) - f \left(t _ {i - 1}\right) \right|}{\alpha}
$$

于是  $g_{1}$  的图像将完全由一些斜率为零和斜率的绝对值至少为  $\alpha$  的线段组成
进而，我们断言  $\rho(g_1, f) \leqslant \varepsilon / 2$ 。这是因为在区间  $I_i$  上， $g_1(x)$  与  $f(x)$  两者相对于  $f(t_{i-1})$  的变化都不超过  $\varepsilon / 4$ 。因此，它们中的每一个相对于另一个的变化不超过  $\varepsilon / 2$ 。于是， $\rho(g_1, f) = \max \{|g_1(x) - f(x)|\} \leqslant \varepsilon / 2$ 
函数  $g_{1}$  还不是我们要找的。现在定义函数  $g$  如下：用一个“锯齿形”图像代替  $g_{1}$  图像中的水平线段，并且这些锯齿形全部包含在  $g_{1}$  图像的  $\varepsilon / 2$  范围以内，锯齿的每一条边的斜率的绝对值至少为  $\alpha$ 。我们把具体的做法留给读者去完成。这样，我们就得到了所要求的函数  $g$ 。如图所示
<img src="f209a237d27cc88faf08f2206077111bd73394e539e7c9a27364acc0d82a9d0f.jpg" width=260>

---
读者可能会觉得这个证明障碍重重，似乎过于玄妙而缺乏建设性。但是，这个证明中却隐含着一个构造特殊的分段线性函数序列  $f_{n}$ ，使其一致收敛于无处可微函数  $f$  的过程。用这种方法定义函数  $f$ ，恰好就像通常用无穷级数的极限来定义正弦函数一样是建设性的。
## 练习

1. 验证例 1 中提到的关于函数  $f$ ， $g$  和  $k$  的性质。  
2. 给定  $n$  和  $\epsilon$ ，定义一个连续函数  $f: I \to \mathbb{R}$ ，使得  $f \in U_n$ ，并且对任意  $x$ ，有  $|f(x)| \leqslant \epsilon$ .


# 第38节 维数论导引
## 38-1 维数论导引


在第36节中已经指出过，若  $X$  是一个紧致流形，则对于某一个正整数  $N$  ，  $X$  可以嵌入到  $\mathbb{R}^N$  中．本节我们将这一定理推广到任意紧致的可度量化空间.

对任意拓扑空间  $X$  ，我们将给出拓扑维数的概念，这就是最初由Lebesgue定义的“覆盖维数”。我们将证明  $\mathbb{R}^m$  的每一个紧致子集的拓扑维数最多是  $m$  。还将证明，每一个  $m$ -维紧致流形的拓扑维数最多是  $m$  。（事实上恰好等于  $m$  ，不过这一点我们不予证明。）

本节的主要定理是：任意拓扑维数为  $m$  的紧致的可度量化空间可以嵌入到  $\mathbb{R}^N$  中，其中  $N = 2m + 1$ 。这个定理由K．Menger和G．Nöbeling证得。这个定理的证明是Baire定理的一个应用。由此得到，每一个紧致的  $m$  -维流形可以嵌入到  $\mathbb{R}^{2m + 1}$  中。此外，还可以得到，对某一个正整数  $N$  ，一个紧致的可度量化空间可以嵌入到  $\mathbb{R}^N$  中当且仅当它有有限的拓扑维数。

我们将要做的讨论之中有很大一部分并不要求所涉及的空间是紧致的，只是为了讨论的方便，才加上了紧致的限制，至于这些结果在非紧致情形下的推广，则放在习题中.

定义 空间  $X$  的一个子集族  $\mathcal{A}$  称为  $m + 1$  阶 (order) 的, 如果  $X$  的某一点属于  $\mathcal{A}$  的  $m + 1$  个元素之中, 并且  $X$  的任何点都不会包含在  $\mathcal{A}$  的多于  $m + 1$  个元素之中.

现在来定义空间  $X$  的拓扑维数．前面说过，对于  $X$  的一个子集族  $\mathcal{A}$  ，子集族  $\mathcal{B}$  称为加细 $\mathcal{A}$  或  $\mathcal{A}$  的一个加细，指的是对  $\mathcal{B}$  的每一个元素  $B$  都存在  $\mathcal{A}$  的一个元素  $A$  ，使得  $B\subset A$

定义 空间  $X$  称为有限维的 (finite dimensional), 如果存在整数  $m$ , 使得对于  $X$  的任意开覆盖  $\mathcal{A}$ , 有最多为  $m + 1$  阶的  $X$  的一个开覆盖  $\mathcal{B}$  加细  $\mathcal{A}$ .  $X$  的拓扑维数 (topological dimension) 定义为满足上述要求的  $m$  的最小值, 记为  $\dim X$ .

例1  $\mathbb{R}$  的任意一个紧致子空间  $X$  的拓扑维数最多为1．我们先从定义  $\mathbb{R}$  的一个2阶开覆

盖开始．用  $\mathcal{A}_1$  表示  $\mathbb{R}$  中所有形如  $(n,n + 1)$  的开区间构成的集族，其中  $n$  是整数．用  $\mathcal{A}_0$  表示 $\mathbb{R}$  中所有形如  $(n - 1 / 2$  ，  $n + 1 / 2)$  的开区间构成的集族，其中  $n$  也是整数．那么  $\mathcal{A} = \mathcal{A}_0\cup \mathcal{A}_1$  是 $\mathbb{R}$  的一个开覆盖，其中每一个集合的直径为1．因为在  $\mathcal{A}_0$  和  $\mathcal{A}_1$  中都没有两个元素相交的情况，所以  $\mathcal{A}$  是2阶的.

现在设  $X$  为  $\mathbb{R}$  的任意一个紧致子空间，给定  $X$  的一个开覆盖  $\mathcal{C}$ ，并且  $\mathcal{C}$  有一个Lebesgue数  $\delta$ ，那么  $X$  的任意直径小于  $\delta$  的一个子集族都是  $\mathcal{C}$  的加细。考虑同胚  $f: \mathbb{R} \to \mathbb{R}$ ，其中  $f(x) = \left(\frac{1}{2}\delta\right)x$ 。 $\mathcal{A}$  中的元素在映射  $f$  下的像构成了  $\mathbb{R}$  的阶为2的开覆盖，并且这个覆盖中的每一个元素的直径均为  $\frac{1}{2}\delta$ ，它们与  $X$  的交就构成了所要求的  $X$  的开覆盖。

例2区间  $X = [0,1]$  的拓扑维数为1．已知  $\dim X\leqslant 1$  ，下面证明等号成立．设  $\mathcal{A}$  是由集合[0，1)和(0，1]构成的  $X$  的覆盖．下面证明如果  $\mathcal{B}$  是  $X$  的任意一个开覆盖，加细  $\mathcal{A}$  ，那么 $\mathcal{B}$  至少为2阶的．因为  $\mathcal{B}$  加细  $\mathcal{A}$  ，故它必定包含了不止一个元素．设  $U$  是  $\mathcal{B}$  中的一个元素，  $V$  是其他元素的并．如果  $\mathcal{B}$  的阶为1，那么  $U$  和  $V$  是无交的，由此产生了  $X$  的一个分割．因此 $\mathcal{B}$  的阶数至少为2.

例3  $\mathbb{R}^2$  的任意一个紧致子集  $X$  的拓扑维数最多为2．为了证明这一点，我们来构造  $\mathbb{R}^2$  的一个开覆盖  $\pmb{\mathcal{A}}$  使其阶数为3．首先，定义  $\mathcal{A}_2$  是  $\mathbb{R}^2$  中具有以下形式的开的单位正方形构成的集族：

$$
\mathcal {A} ^ {2} = \{(n, n + 1) \times (m, m + 1) \mid m, n \text {是 整 数} \}.
$$

注意  $\mathcal{A}_2$  中的元素是两两无交的．其次，取这些正方形之一的每一条(开)边  $e$

$$
e = \{n \} \times (m, m + 1) \quad {\text {或 者}} \quad e = (n, n + 1) \times \{m \},
$$

并且将其稍加扩大而成为  $\mathbb{R}^2$  中的开集  $U_{e}$  ，使得如果  $e\neq e^{\prime}$  ，那么集合  $U_{e}$  和  $U_{e^{\prime}}$  无交．同时还要求所选的每一个  $U_{e}$  的直径最多为2．最后，定义  $\mathcal{A}_0$  为由所有中心在点  $n\times m$  、半径为  $\frac{1}{2}$  的开球所构成的集族，如图50.1所示.

![](72f636f99e83be4b5ca8c651c6ed06bb8da15c2521548da7b1073f78c46f4f66.jpg)

![](215511f7ee36016bf61e0fb60a2a51ffb8bbe3467ec29fc1e9838608026c2516.jpg)  
图50.1

![](9e3306f89460bb389157db9bd6d767abe449586bfcff00cccd7f3046f707567e.jpg)

开集族  $\mathcal{A} = \mathcal{A}_2 \cup \mathcal{A}_1 \cup \mathcal{A}_0$  覆盖了  $\mathbb{R}^2$ ，并且它的每一个元素的直径最多为 2。又因为  $\mathbb{R}^2$  中的任何点最多落在每一个  $\mathcal{A}_i$  中的一个集合中，所以  $\mathcal{A}$  的阶数为 3。

现在设  $X$  是  $\mathbb{R}^2$  的紧致子空间．给定  $X$  的一个开覆盖，它有一个正的Lebesgue数  $\delta$  ，考虑同胚  $f: \mathbb{R}^2 \to \mathbb{R}^2$  ，其中  $f(x) = (\delta / 3)x$  ，集族  $\mathcal{A}$  中的开集在  $f$  之下的像构成了  $\mathbb{R}^2$  的一个开覆盖，并且其中每一个集合的直径小于  $\delta$  。它们与  $X$  的交构成了所求的  $X$  的一个开覆盖.

我们将推广这一结论到  $\mathbb{R}^n$  的紧致子集上.

下列定理给出有关拓扑维数的一些基本结论

定理50.1 设  $X$  是具有有限维数的一个空间．如果  $Y$  是  $X$  的一个闭子空间，那么  $Y$  也具有有限维数，并且  $\dim Y \leqslant \dim X$ .

证设  $\dim X = m$  ，  $\mathcal{A}$  是由  $Y$  的开集构成的  $Y$  的一个覆盖．对于每一个  $A\in \mathcal{A}$  ，选取  $X$  的一个开集  $A^{\prime}$  ，使得  $A^{\prime}\cap Y = A$  ．这些开集  $A^{\prime}$  连同开集  $X - Y$  一起构成了  $X$  的一个覆盖．设  $\mathcal{B}$  是这个覆盖的一个加细，同时它也是  $X$  的一个开覆盖，并且最多是  $m + 1$  阶的．于是集族

$$
\{B \cap Y \mid B \in \mathcal {B} \}
$$

是由  $Y$  的一个开集构成的  $Y$  的一个覆盖，它加细  $\mathcal{A}$  并且阶数最多为  $m + 1$ .

定理50.2 设  $X = Y \cup Z$ ，其中  $Y$  和  $Z$  是  $X$  中的两个闭子空间，都具有有限拓扑维数。那么

$$
\dim X = \max  \{\dim Y, \dim Z \}.
$$

证 设  $m = \max \{\dim Y, \dim Z\}$ 。下面我们证明  $X$  是有限维的，并且拓扑维数最多为  $m$ 。再根据前述定理便得到  $X$  的拓扑维数是  $m$  的结论。

第一步．如果  $\mathcal{A}$  是  $X$  的一个开覆盖，我们说  $\mathcal{A}$  在  $Y$  中的点的阶数最多为  $m + 1$  ，是指  $Y$  中的点最多属于  $\mathcal{A}$  的  $m + 1$  个元素.

下面证明，如果  $\mathcal{A}$  是  $X$  的一个开覆盖，那么存在  $X$  的一个开覆盖加细  $\mathcal{A}$ ，并且在  $Y$  中的点的阶数最多为  $m + 1$ .

为了证明这一点，考虑集族

$$
\{A \cap Y \mid A \in \mathcal {A} \}.
$$

它是  $Y$  的一个开覆盖，所以它有一个开的加细  $\mathcal{B}$  覆盖  $Y$  ，并且其阶数最多为  $m + 1$  。任意给定  $B \in \mathcal{B}$  ，选取  $X$  中的一个开集  $U_{B}$  ，使得  $U_{B} \cap Y = B$  。选取  $\mathcal{A}$  中的一个元素  $A_{B}$  ，使得  $B \subset A_{B}$  。令  $\mathcal{C}$  是由所有集合  $U_{B} \cap A_{B}$  以及所有集合  $A - Y$  组成的集族，其中  $B \in \mathcal{B}$  ， $A \in \mathcal{A}$  ，则  $\mathcal{C}$  就是所要找的  $X$  的那个开覆盖。

第二步．设  $\mathcal{A}$  是  $X$  的一个开覆盖．我们将构造  $X$  的一个开覆盖  $\mathcal{D}$ ，使得  $\mathcal{D}$  加细  $\mathcal{A}$ ，并且它的阶数最多为  $m + 1$ ．设  $\mathcal{B}$  为  $X$  的一个开覆盖， $\mathcal{B}$  加细  $\mathcal{A}$ ，并且在  $Y$  中的点的阶数最多为  $m + 1$ ．再设  $\mathcal{C}$  是  $X$  的开覆盖，它加细  $\mathcal{B}$  并且在  $Z$  中的点的阶数最多为  $m + 1$

我们用以下方式来构造  $X$  的一个新的覆盖  $\mathcal{D}$  ：定义  $f: \mathcal{C} \to \mathcal{B}$  为对于每一个  $C \in \mathcal{C}$ ，取  $f(C)$  为  $\mathcal{B}$  中的一个元素，满足  $C \subset f(C)$ 。给定  $B \in \mathcal{B}$ ，定义  $D(B)$  为  $\mathcal{C}$  中所有满足  $f(C) = B$  的元素  $C$  的并。（当然，如果  $B$  不在  $f$  的像中，则  $D(B)$  为空集。）取  $\mathcal{D}$  为所有集合  $D(B)$  的族，其中  $B \in \mathcal{B}$ 。

现在  $\mathcal{D}$  加细  $\mathcal{B}$ ，这是因为对于每一个  $B$  有  $D(B) \subset B$ 。因此  $\mathcal{D}$  加细  $\mathcal{A}$ ，并且  $\mathcal{D}$  覆盖  $X$ ，这是因为  $\mathcal{C}$  覆盖  $X$ ，并且对于每一个  $C \in \mathcal{C}$  有  $C \subset D(f(C))$ 。下面，我们证明  $\mathcal{D}$  最多为  $m + 1$  阶。假设  $x \in D(B_1) \cap \dots \cap D(B_k)$ ，其中  $D(B_i)$  是互不相同的。我们希望能证明  $k \leqslant m + 1$ 。注意集合  $B_1, \dots, B_k$  是互不相同的，这是因为集合  $D(B_i)$  互不相同。又因为  $x \in D(B_i)$ ，所以对于每一个  $i$ ，可以选取一个集合  $C_i \in \mathcal{C}$ ，使得  $x \in C_i$  并且  $f(C_i) = B_i$ 。因为集合  $B_i$  是互不相同的，所以集合  $C_i$  也是互不相同的。进而，有

$$
x \in \left[ C _ {1} \cap \dots \cap C _ {k} \right] \subset \left[ D \left(B _ {1}\right) \cap \dots \cap D \left(B _ {k}\right) \right] \subset \left[ B _ {1} \cap \dots \cap B _ {k} \right].
$$

如果  $x$  恰好在  $Y$  中，根据  $\mathcal{B}$  在  $Y$  的点上最多为  $m + 1$  阶，可见  $k \leqslant m + 1$ 。如果  $x$  恰好在  $Z$  中，再根据  $\mathcal{C}$  在  $Z$  中的点最多为  $m + 1$  阶，可见  $k \leqslant m + 1$ 。

推论50.3 设  $X = Y_{1} \cup \dots \cup Y_{k}$ , 其中每一个  $Y_{i}$  是  $X$  中的一个闭子空间, 并且是有限维的, 则

$$
\dim X = \max  \left\{\dim Y _ {1}, \dots , \dim Y _ {k} \right\}.
$$

例4每一个紧致的1-维流形  $X$  的拓扑维数为1．空间  $X$  可以表示成同胚于单位区间[0，1]的空间的有限并，然后应用上述推论便得到了所需的结论.

例5每一个紧致2-维流形的拓扑维数最多为2．空间  $X$  可以表示成同胚于  $\mathbb{R}^2$  中单位闭球的空间的有限并，再根据前述推论便得到了所需的结论.

一个很自然的问题由此产生：紧致2-维流形的拓扑维数恰好是2吗？答案是肯定的，但它的证明却不太容易，需要以代数拓扑作为工具。我们将在本书的第二部分证明： $\mathbb{R}^2$  中每一个闭的三角区域的拓扑维数至少为2。（见第55节。）据此可见， $\mathbb{R}^2$  中任何包含一个闭的三角区域的紧致子空间的拓扑维数就为2。从而，紧致2-维流形的拓扑维数恰好是2。

例6 弧(arc)  $A$  是指同胚于单位闭区间的一个空间。 $A$  的端点(end point)是指使得  $A - \{p\}$  和  $A - \{q\}$  是连通子集的点  $p$  和  $q$ 。（有限）线性图(linear graph)  $G$  是指一个Hausdorff空间，它可以表示成有限多段弧的并，其中每对弧最多交于一个公共端点。这些弧就称为  $G$  的边(edge)，这些弧的端点就称为  $G$  的顶点(vertex)。 $G$  的每条边，因为是紧致的，所以在  $G$  中是闭的。由前述推论可见  $G$  的拓扑维数是1。

图50.2中刻画了两个特殊的线性图。第一个是通常的“气水电问题”的图示。第二个被称为“五个顶点的完全图”。它们都不能嵌入到  $\mathbb{R}^2$  中。尽管这个结论是“显而易见的”，但其证明却不那么容易。在第64节中我们将给出其证明。

![](05fb60ab814175b7db9429ed34417a2b90cd77a64febca0f94db20b6403fc4b2.jpg)  
图50.2

![](da90f3a6808d2413e37d66127949d7adb14f52716c00db3b10403e8bda3d59aa.jpg)

例7 每一个有限线性图都能嵌入到  $\mathbb{R}^3$  中。这个证明涉及“最广位置”的概念。  $\mathbb{R}^3$  的一个子集  $S$  称为占有最广位置，如果  $S$  中没有三点共线且没有四点共面。这样的点集是容易找到的。例如，曲线

$$
S = \left\{\left(t, t ^ {2}, t ^ {3}\right) \mid t \in \mathbb {R} \right\}
$$

上的点集就占有最广位置．因为如果有四个点位于同一平面  $Ax + By + Cz = D$  上，那么多项式方程

$$
A t + B t ^ {2} + C t ^ {3} = D
$$

将有四个不同的实根！如果有三点共线，那么可以取  $S$  中另外一个点，获得位于同一平面上的四个点.

现在给定一个有限线性图  $G$ ，其顶点分别是  $v_{1}, \cdots, v_{n}$ ，选取  $\mathbb{R}^{3}$  中占有最广位置的一个点集  $\{z_{1}, \cdots, z_{n}\}$ 。定义映射  $f: G \to \mathbb{R}^{3}$ ，使得  $f$  将顶点  $v_{i}$  映为  $z_{i}$ ，并将连接  $v_{i}$  和  $v_{j}$  的边同胚地映射到直线的连接  $z_{i}$  和  $z_{j}$  的那条线段上。现在  $G$  的每条边在  $G$  中都是闭的，从而根据黏结引理可见， $f$  是连续的。下面我们证明  $f$  是一个单射，从而说明  $f$  是一个嵌入。设  $e = v_{i}v_{j}$  和  $e' = v_{k}v_{m}$  是  $G$  的两条边。如果它们没有公共的顶点，那么  $f(e)$  和  $f(e')$  无交。因为如果有交，那么  $z_{i}, z_{j}, z_{k}, z_{m}$  共面。如果  $e$  和  $e'$  有公共的顶点，不妨设  $i = k$ ，那么  $f(e)$  和  $f(e')$  只能交于一点  $z_{i} = z_{k}$ ，因为如若不然，就有  $z_{i}, z_{j}, z_{m}$  共线。

现在，我们证明一个更一般的嵌入定理：每一个拓扑维数是  $m$  的紧致可度量化空间都可以嵌入到  $\mathbb{R}^{2m + 1}$  中。这个定理又是一个“深刻”的定理。它并非显而易见的，例如，为什么取  $2m + 1$  为这个关键的维数。这将在证明的过程中进行说明。

为了证明嵌入定理，我们需要将最广位置的概念推广到  $\mathbb{R}^N$  中．这将会涉及  $\mathbb{R}^N$  上一些解析几何的知识，与通常的  $\mathbb{R}^N$  上的线性代数差不多，只是所用的语言不同而已.

定义  $\mathbb{R}^N$  中的一个点集  $\{\pmb{x}_0,\dots ,\pmb{x}_k\}$  称为几何独立的（geometrically independent)或仿射独立的(affinely independent)，如果等式

$$
\sum_ {i = 0} ^ {k} a _ {i} \pmb {x} _ {i} = \mathbf {0} \quad {\text {和}} \quad \sum_ {i = 0} ^ {k} a _ {i} = 0
$$

仅在每一个  $a_{i} = 0$  时才成立.

显然，任意单点集是几何独立的。那么，一般情况下几何独立意味着什么呢？如果由第二个等式解出  $a_0$ ，再代入第一个等式，可见这个定义实际上等价于等式

$$
\sum_ {i = 1} ^ {k} a _ {i} \left(\boldsymbol {x} _ {i} - \boldsymbol {x} _ {0}\right) = \mathbf {0}
$$

仅在每一个  $a_{i} = 0$  时才成立．这恰好是向量空间  $\mathbb{R}^N$  中向量集  $x_{1} - x_{0}$  ，…，  $x_{k} - x_{0}$  线性独立的定义．这样，我们就得出了一些直观印象：任意两个不同的点构成几何独立点集，不共线的三点构成一个几何独立点集，在  $\mathbb{R}^3$  中不共面的四点构成几何独立点集，等等.

由这些说明可见，下述点

$$
\begin{array}{l} \mathbf {0} = (0, 0, \dots , 0), \\ \varepsilon_ {1} = (1, 0, \dots , 0), \\ \dots \\ \varepsilon_ {N} = (0, 0, \dots , 1) \\ \end{array}
$$

在  $\mathbb{R}^N$  中是几何独立的．另外，  $\mathbb{R}^N$  中不存在包含多于  $N + 1$  个点的几何独立点集.

定义 设  $\{\pmb{x}_0, \dots, \pmb{x}_k\}$  为  $\mathbb{R}^N$  中的一个几何独立点集，由这些点确定的平面  $\pmb{P}$  (plane  $P$  determined by these points) 定义为  $\mathbb{R}^N$  中所有满足以下条件的点  $\pmb{x}$  构成的集合：

$$
\pmb {x} = \sum_ {i = 0} ^ {k} t _ {i} \pmb {x} _ {i}, \quad \text {其 中} \quad \sum_ {i = 0} ^ {k} t _ {i} = 1.
$$

仅由代数知识即可验证  $P$  也可以表示为所有点  $\pmb{x}$  的集合，其中  $\pmb{x}$  满足对某一组纯量  $a_1, \dots, a_k$ ，有

$$
\boldsymbol {x} = \boldsymbol {x} _ {0} + \sum_ {i = 1} ^ {k} a _ {i} \left(\boldsymbol {x} _ {i} - \boldsymbol {x} _ {0}\right). \tag {*}
$$

这样，  $P$  不仅可以描述成“由点  $\pmb{x}_0$  ，…，  $\pmb{x}_k$  确定的平面”，还可以描述成“过点  $\pmb{x}_0$  ，并且与向量 $\pmb {x}_1 - \pmb {x}_0$  ，…，  $\pmb {x}_k - \pmb {x}_0$  平行的平面”

现在考虑定义为  $T(\pmb {x}) = \pmb {x} - \pmb {x}_0$  的同胚  $T$  ：  $\mathbb{R}^N\to \mathbb{R}^N$  ，它称为  $\mathbb{R}^N$  中的一个平移(translation)， $(\ast)$  式表明映射  $T$  把平面  $P$  映到  $\mathbb{R}^N$  的一个向量子空间  $V^{k}$  上，其中  $V^{k}$  以向量  $\pmb {x}_1 - \pmb {x}_0$  ，…，  $\pmb {x}_k-$ $\pmb{x_0}$  为基．由于这个原因，常常称  $P$  为  $\mathbb{R}^N$  中的一个  $\pmb{k}$  -维平面  $(k$  -plane).

于是立即可见以下两点：首先，如果  $k < N$  ， $k$ -维平面必然在  $\mathbb{R}^N$  中有空内部（因为  $V^k$  有空内部）。其次，如果  $\mathbf{y}$  是  $\mathbb{R}^N$  中不在  $P$  中的任意一点，则集合

$$
\left\{\boldsymbol {x} _ {0}, \dots , \boldsymbol {x} _ {k}, \boldsymbol {y} \right\}
$$

是几何独立的．因为若  $y \notin P$  ，则  $T(y) = y - x_0$  不在  $V^k$  中．根据线性代数中的一个标准定理，向量  $\{x_1 - x_0, \dots, x_k - x_0, y - x_0\}$  线性无关，从而得出我们所期望的结果.

定义  $\mathbb{R}^N$  中的一个点集  $A$  称为在  $\mathbb{R}^N$  中占有最广位置（general position in  $\mathbb{R}^N$ ），如果  $A$  的每一个含有  $N + 1$  个点或者少于  $N + 1$  个点的子集都是几何独立的。

在  $\mathbb{R}^3$  的情形下，可以验证这与以前的定义是一致的.

引理50.4 给定  $\mathbb{R}^N$  的一个有限点集  $\{\pmb{x}_1, \dots, \pmb{x}_n\}$  和  $\delta > 0$ ，存在  $\mathbb{R}^N$  中占有最广位置的一个点集  $\{\pmb{y}_1, \dots, \pmb{y}_n\}$ ，使得对于所有的  $i$ ，有  $|\pmb{x}_i - \pmb{y}_i| < \delta$ 。

证 我们采用归纳法证明。令  $y_1 = x_1$ ，假定已经给定了  $\mathbb{R}^N$  中占有最广位置的  $y_1, \dots, y_p$ 。考虑  $\{y_1, \dots, y_p\}$  中不多于  $N$  个点的子集确定的  $\mathbb{R}^N$  中的所有平面的集合。当  $k \leqslant N - 1$  时，每一个这样的子集都是几何独立的，并且确定了一个  $k$ -维平面。这些平面在  $\mathbb{R}^N$  中都有空内部。由于这些平面只有有限多个，所以它们的并在  $\mathbb{R}^N$  中也有空内部。（注意  $\mathbb{R}^N$  是一个Baire空间。）选取  $y_{p + 1}$  为  $\mathbb{R}^N$  中的一点，它与  $x_{p + 1}$  的距离不超过  $\delta$ ，并且不在上述任何一个平面之中。由此立即可见集合

$$
C = \left\{\mathbf {y} _ {1}, \dots , \mathbf {y} _ {p}, \mathbf {y} _ {p + 1} \right\}
$$

是  $\mathbb{R}^N$  中占有最广位置的集合。因为若令  $D$  为包含  $C$  中不多于  $N + 1$  个点的一个子集，当  $D$  不包含  $\mathbf{y}_{p + 1}$  时，根据归纳假设， $D$  是几何独立的。如果  $D$  含有  $\mathbf{y}_{p + 1}$ ，则  $D - \{\mathbf{y}_{p + 1}\}$  包含不多于  $N$  个点，并且根据选择， $\mathbf{y}_{p + 1}$  不在由这些点所确定的平面中。于是根据前面所述， $D$  是几何独立的。

定理50.5[嵌入定理(imbedding theorem)] 每一个拓扑维数为  $m$  的紧致可度量化空间  $X$  都可以嵌入到  $\mathbb{R}^{2m+1}$  中。

证 设  $N = 2m + 1$  ，我们用

$$
\mid x - y \mid = \max  \left\{\mid x _ {i} - y _ {i} \mid ; i = 1, \dots , N \right\}
$$

表示  $\mathbb{R}^N$  上的平方度量．用  $\rho$  表示空间  $\mathcal{C}(X,\mathbb{R}^N)$  上相应的上确界度量，其中

$$
\rho (f, g) = \sup  \left\{\mid f (x) - g (x) \mid ; x \in X \right\}.
$$

因为  $\mathbb{R}^N$  在平方度量下是完备的，所以在度量  $\rho$  下，空间  $\mathcal{C}(X,\mathbb{R}^N)$  也是完备的.

选取空间  $X$  的一个度量  $d$  ，因为  $X$  紧致，所以  $d$  是有界的．给定一个连续映射  $f: X \to \mathbb{R}^N$  ，定义

$$
\Delta (f) = \sup  \left\{\operatorname {d i a m} f ^ {- 1} (\{z \}) \mid z \in f (X) \right\}.
$$

数  $\Delta(f)$  可以测量  $f$  “偏离”单射的程度，如果  $\Delta(f) = 0$ ，则每一个集合  $f^{-1}(\{z\})$  恰好由一个点组成，因而  $f$  是一个单射。

现在，给定  $\varepsilon > 0$  ，定义  $U_{\varepsilon}$  为所有使得  $\Delta(f) < \varepsilon$  的连续映射  $f: X \to \mathbb{R}^{N}$  的集合，它是由“偏离”单射的程度小于  $\varepsilon$  的那些映射组成的．下面证明  $U_{\varepsilon}$  是  $\mathcal{C}(X, \mathbb{R}^{N})$  中的一个稠密开集．据此，交

$$
\bigcap_ {n \in \mathbf {Z} _ {+}} U _ {1 / n}
$$

在  $\mathcal{C}(X,\mathbb{R}^N)$  中是稠密的，特别地，它是非空的

如果  $f$  是这个交的一个元素，那么对任意的  $n$  ，有  $\Delta (f) < 1 / n$  ，因此  $\Delta (f) = 0$  ，从而  $f$  是单射．又因为  $X$  紧致，所以  $f$  是一个嵌入．于是嵌入定理得证.

(1)  $U_{\epsilon}$  是  $\mathcal{C}(X, \mathbb{R}^{N})$  中的一个开集。给定  $U_{\epsilon}$  中的一个元素  $f$ ，我们希望找到以  $f$  为中心的一个球  $B_{\rho}(f, \delta)$  包含于  $U_{\epsilon}$ 。首先选一个数  $b$ ，使得  $\Delta(f) < b < \varepsilon$ 。注意，如果  $f(x) = f(y) = z$ ，则有  $x$  和  $y$  都属于  $f^{-1}(\{z\})$ ，所以  $d(x, y)$  必小于  $b$ 。由此可见，若令  $A$  为  $X \times X$  的子集

$$
A = \{x \times y \mid d (x, y) \geqslant b \},
$$

则函数  $|f(x) - f(y)|$  在  $A$  上是正的．由于  $A$  在  $X \times X$  中是闭的，所以是紧致的．于是函数  $|f(x) - f(y)|$  在  $A$  上有一个正的极小值．令

$$
\delta = \frac {1}{2} \min  \left\{\mid f (x) - f (y) \mid ; x \times y \in A \right\}.
$$

我们断言，这个  $\delta$  便足够了.

假设  $g$  是一个映射，使得  $\rho(f, g) < \delta$ 。如果  $x \times y \in A$ ，则根据定义  $|f(x) - f(y)| \geqslant 2\delta$ 。这是因为  $g(x)$  与  $g(y)$  分别与  $f(x)$  和  $f(y)$  的距离小于  $\delta$ ，所以必有  $|g(x) - g(y)| > 0$ 。因此函数  $|g(x) - g(y)|$  在  $A$  上是正的。由此推出，若  $x$  和  $y$  是满足  $g(x) = g(y)$  的两个点，则必有  $d(x, y) < b$ 。所以  $\Delta(g) \leqslant b < \varepsilon$ 。

(2)  $U_{\epsilon}$  在  $\mathcal{C}(X, \mathbb{R}^{N})$  中稠密。这是证明中的困难之处，需要用到上面讨论过的  $\mathbb{R}^{N}$  的解析几何知识。设  $f \in \mathcal{C}(X, \mathbb{R}^{N})$ 。给定  $\epsilon > 0$  和  $\delta > 0$ ，我们希望找到一个函数  $g \in \mathcal{C}(X, \mathbb{R}^{N})$  使得  $g \in U_{\epsilon}$ ，并且  $\rho(f, g) < \delta$ 。

用有限多个开集  $\{U_1, \dots, U_n\}$  覆盖  $X$ ，使得

(1) 在  $X$  中,  $\mathrm{diam}U_{i} < \varepsilon / 2$ .  
(2)在  $\mathbb{R}^N$  中，  $\mathrm{diam}f(U_i) < \delta / 2.$  
(3)  $\{U_{1}, \dots, U_{n}\}$  的阶数  $\leqslant m + 1$ .

设  $\{\phi_i\}$  是由  $\{U_i\}$  控制的一个单位分拆(见第36节). 对于每一个  $i$  ，选取一个点  $x_{i} \in U_{i}$  ，再对于每一个  $i$  ，选取一个点  $z_{i} \in \mathbb{R}^{N}$  ，使得  $z_{i}$  与点  $f(x_{i})$  的距离小于  $\delta /2$  ，并且使得  $\{z_1,\dots ,z_n\}$  在 $\mathbb{R}^N$  中占有最广位置．最后，定义  $g: X \to \mathbb{R}^N$  为

$$
g (x) = \sum_ {i = 1} ^ {n} \phi_ {i} (x) z _ {i}.
$$

我们断言，  $g$  便是所求的函数

首先，我们证明  $\rho(f, g) < \delta$ 。注意，

$$
g (x) - f (x) = \sum_ {i = 1} ^ {n} \phi_ {i} (x) z _ {i} - \sum_ {i = 1} ^ {n} \phi_ {i} (x) f (x).
$$

其中用到了  $\sum \phi_{i}(x) = 1$  ，于是

$$
g (x) - f (x) = \sum \phi_ {i} (x) \left(z _ {i} - f \left(x _ {i}\right)\right) + \sum \phi_ {i} (x) \left(f \left(x _ {i}\right) - f (x)\right).
$$

根据点  $\pmb{z}_i$  的选取，对于每一个  $i$  ， $|z_i - f(x_i)| < \delta / 2$ 。如果  $i$  是使得  $\phi_i(x) \neq 0$  的一个指标，则有  $x \in U_i$ 。因为  $\operatorname{diam} f(U_i) < \delta / 2$ ，所以  $|f(x_i) - f(x)| < \delta / 2$ 。由于  $\sum \phi_i(x) = 1$ ，可见  $|g(x) - f(x)| < \delta$ 。于是  $\rho(g, f) < \delta$ 。

其次，证明  $g \in U_{\epsilon}$ 。我们要证明，若  $x, y \in X$ ，并且  $g(x) = g(y)$ ，则  $x$  和  $y$  同时属于某一个开集  $U_{i}$ ，因而必有  $d(x, y) < \varepsilon / 2$ 。（因为  $\mathrm{diam} U_{i} < \varepsilon / 2$ 。）于是  $\Delta(g) \leqslant \varepsilon / 2 < \varepsilon$ 。

为此假定  $g(x) = g(y)$ ，于是

$$
\sum_ {i = 1} ^ {n} \left[ \phi_ {i} (x) - \phi_ {i} (y) \right] z _ {i} = \mathbf {0}.
$$

因为覆盖  $\{U_i\}$  最多为  $m + 1$  阶，所以最多有  $m + 1$  个  $\phi_i(x)$  不为零，也最多有  $m + 1$  个  $\phi_i(y)$  不为零．从而，和式  $\sum_{i = 1}^{n}[\phi_i(x) - \phi_i(y)]z_i$  最多有  $2m + 2$  个非零项．注意到和式的系数之和蜕化，因为

$$
\sum \left[ \phi_ {i} (x) - \phi_ {i} (y) \right] = 1 - 1 = 0.
$$

这些点  $z_{i}$  在  $\mathbb{R}^N$  中占有最广位置，所以其含有不多于  $N + 1$  个元素的任何一个子集必定是几何独立的．根据假设  $N + 1 = 2m + 2$  ，于是对于所有的  $i$

$$
\phi_ {i} (x) - \phi_ {i} (y) = 0.
$$

对某一个  $i$  ，  $\phi_i(x) > 0$  ，所以  $x\in U_{i}$  ，因为  $\phi_i(y) = \phi_i(x)$  ，所以也有  $y\in U_{i}$

为了充实嵌入定理的内涵，我们需要一些有限维空间的例子．为此，我们证明以下定理.

定理50.6  $\mathbb{R}^N$  的每一个紧致子空间的拓扑维数最多为  $N$ .

证 这个证明是例3中对于  $\mathbb{R}^2$  所给证明的一个推广。设  $\rho$  是  $\mathbb{R}^N$  上的平方度量。

第一步．首先把  $\mathbb{R}^N$  分解成一些“单位方体”．定义  $\mathcal{I}$  是  $\mathbb{R}$  中的以下开区间族：

$$
\mathcal {J} = \{(n, n + 1) \mid n \in \mathbb {Z} \},
$$

再定义  $\mathcal{K}$  为  $\mathbb{R}$  中的以下单点集族：

$$
\mathcal {K} = \{\{n \} \mid n \in \mathbb {Z} \}.
$$

如果  $M$  是一个整数，使得  $0 \leqslant M \leqslant N$  ，令  $\mathcal{C}_M$  表示所有积

$$
C = A _ {1} \times A _ {2} \times \dots \times A _ {N}
$$

的集合，其中恰有  $M$  个  $A_{i}$  属于  $\mathcal{F}$ ，而其余的  $A_{i}$  则属于  $\mathcal{K}$ 。如果  $M > 0$ ，则  $C$  同胚于积空间  $(0,1)^{M}$ ，称之为  $M$ -维方体（ $M$ -cube）。如果  $M = 0$ ，则  $C$  是一个单点集，称之为  $0$ -维方体（0-cube）。

令  $\mathcal{C} = \mathcal{C}_0 \cup \mathcal{C}_1 \cup \dots \cup \mathcal{C}_N$ 。注意  $\mathbb{R}^N$  的每一个点  $x$  恰属于  $\mathcal{C}$  的一个元素，因为每一个实数  $x_i$  恰在  $\mathcal{J} \cup \mathcal{K}$  的一个元素中。我们将  $\mathcal{C}$  的每一个元素  $C$  稍加扩大，使之成为  $\mathbb{R}^N$  中直径不超过  $3/2$  的一个开集  $U(C)$ ，使得如果  $C$  和  $D$  是两个不同的  $M$ -维方体，则  $U(C)$  和  $U(D)$  无交。

设  $x = (x_{1},\dots ,x_{N})$  是  $M$  -维方体  $C$  的一个点．我们将证明，存在一个数  $\varepsilon (\pmb {x}) > 0$  ，使得  $\pmb{x}$  的  $\varepsilon (\pmb {x})$  -邻域与异于  $C$  的  $M$  -维方体无交．如果  $C$  是0-维方体，我们令  $\varepsilon (\pmb {x}) = 1 / 2$  ，从而完成证明．若  $M > 0$  ，并且  $x_{i}$  中恰好有  $M$  个不是整数，则选取  $\varepsilon (\pmb {x})\leqslant 1 / 2$  ，使得对于每一个不是整数的  $x_{i}$  ，区间  $(x_{i} - \varepsilon ,x_{i} + \varepsilon)$  中不包含整数．如果  $\mathbf{y} = (y_{1},\dots ,y_{N})$  是  $\pmb{x}$  的  $\varepsilon$  -邻域的一个点，那么当  $x_{i}$  不是整数时，  $y_{i}$  也不是整数．这意味着，要么  $\mathbf{y}$  与  $\pmb{x}$  属于同一个  $M$  -维方体，要么  $\mathbf{y}$  属于某一个  $L$  -维方体，其中  $L > M$  ，不论何种情况，  $\pmb{x}$  的  $\varepsilon$  -邻域与异于  $C$  的  $M$  -维方体无交.

给定一个  $M$ -维方体  $C$ ，定义  $C$  的邻域  $U(C)$  为  $C$  中所有点  $\pmb{x}$  的  $\varepsilon(x)/2$ -邻域的并。易见，若  $C$  与  $D$  是两个不同的  $M$ -维方体，则  $U(C)$  与  $U(D)$  无交。进而，若  $\pmb{z}$  是  $U(C)$  的一个点，则存在  $C$  的一个点  $\pmb{x}$ ，使得  $d(\pmb{z}, \pmb{x}) < \varepsilon(\pmb{x})/2 < 1/4$ 。由于  $C$  的直径为 1，所以集合  $U(C)$  的直径最多为  $3/2$ 。

第二步．给定  $M$  ，  $0\leqslant M\leqslant N$  ，定义  $\mathcal{A}_M$  为所有集合  $U(C)$  的族，其中  $C\in \mathcal{C}_M$  ：  $\mathcal{A}_M$  中的元素两两无交，并且每一个元素的直径最多为  $3 / 2$  ，剩下来的证明只不过是例3中对  $\mathbb{R}^2$  所做证明的翻版.

推论50.7 每一个紧致的  $m$ -维流形的拓扑维数最多为  $m$

推论50.8每一个紧致的  $m$  -维流形可以嵌入到  $\mathbb{R}^{2m + 1}$  中，

推论50.9 设  $X$  是一个紧致的可度量化空间，那么  $X$  可以嵌入到某一个欧氏空间  $\mathbb{R}^N$  中，当且仅当  $X$  具有有限拓扑维数。

正如先前提到过的，我们证明的结果之中，有许多并不要求紧致性条件，在下面的习题中，请读者去证明相应结果的推广.

有一点我们没有要求证明，即证明  $m$ -维流形的拓扑维数恰好是  $m$ 。一个重要的原因就是，这个证明要以代数拓扑为工具。

还有一点我们也没有要求证明，即  $N = 2m + 1$  是使得每一个拓扑维数为  $m$  的紧致可度量化空间可以嵌入到  $\mathbb{R}^N$  中的  $N$  的最小值。我们曾提到过，即使对于线性图，其中  $m = 1$ ，该证明也不容易。

关于维数论的进一步结果，读者可以参见 Hurewicz 和 Wallman[H-W]的经典书籍。特别地，那本书中讨论了一个完全不同的拓扑维数的定义，归功于 Menger 和 Urysohn。它是一个归纳定义。空集的维数为 -1。如果一个空间有一个拓扑基，该基中每一个元素  $B$  的边界的维数最多为  $n - 1$ ，则这个空间的维数最多为  $n$ 。一个空间的维数便是使得这一条件成立的最小的  $n$ 。这个维数概念与我们对紧致可度量化空间所定义的概念是一致的。

## 练习

1. 证明任意离散空间是0维的  
2. 证明任意多于一个点的连通  $T_{1}$  空间的维数至少为 1.  
3. 证明拓扑学家的正弦曲线是1维的

4. 证明：点  $\mathbf{0}, \varepsilon_1, \varepsilon_2, \varepsilon_3$  和(1，1，1)在  $\mathbb{R}^3$  中占有最广位置。画出由这五个顶点构成的完全图嵌入到  $\mathbb{R}^3$  中的草图。  
5. 验证当  $m = 1$  时，嵌入定理的证明，并证明在第(2)部分中，映射  $\pmb{g}$  将  $X$  映到  $\mathbb{R}^3$  中的一个线性图上.  
6. 定理 设  $X$  是一个具有可数基的局部紧致的 Hausdorff 空间，且其每一个紧致子空间的拓扑维数最多为  $m$ ，则  $X$  同胚于  $\mathbb{R}^{2m+1}$  的一个闭子空间。

证明：设  $f: X \to \mathbb{R}^N$  是一个连续映射，我们说当  $x \to \infty$  时  $f(x) \to \infty$ ，是指对于任意给定的  $n$ ，存在  $X$  的紧致子空间  $C$ ，使得对于每一个点  $x \in X - C$  有  $f(x) > n$ .

(a) 设  $\bar{\rho}$  是  $\mathcal{C}(X, \mathbb{R}^N)$  上的一致度量。证明：若当  $x \to \infty$  时， $f(x) \to \infty$ ，并且  $\bar{\rho}(f, g) < 1$ ，则当  $x \to \infty$  时， $g(x) \to \infty$ 。  
(b) 证明：若当  $x \to \infty$  时， $f(x) \to \infty$ ，则  $f$  可以扩张成单点紧致化空间上的一个连续映射。证明：若  $f$  是一个单射，则  $f$  是  $X$  与  $\mathbb{R}^N$  的一个闭子空间的同胚。  
(c)给定  $f$  ：  $X\to \mathbb{R}^N$  和  $X$  的一个紧致子空间  $C$  ，令

$$
U _ {\varepsilon} (C) = \{f \mid \Delta (f \mid C) <   \varepsilon \}.
$$

证明  $U_{\epsilon}(C)$  在  $\mathcal{C}(X,\mathbb{R}^N)$  中是开的.

(d) 证明：若  $N = 2m + 1$ ，则  $U_{\varepsilon}(C)$  在  $\mathcal{C}(X, \mathbb{R}^N)$  中稠密。[提示：给定  $f$  和  $\varepsilon, \delta > 0$ ，选取  $g: C \to \mathbb{R}^N$  使得对于  $x \in C$ ，有  $d(f(x), g(x)) < \delta$ ，并且  $\Delta(g) < \varepsilon$ 。应用Tietze扩张定理，扩充  $f - g$  为  $h: X \to [-\delta, \delta]^N$ 。]  
(e)证明存在映射  $f$  ：  $X\to \mathbb{R}$  使得当  $x\rightarrow \infty$  时，  $f(x)\rightarrow \infty$  ，[提示：将  $X$  表示成紧致子空间 $C_n$  的并，其中对于每一个  $\pmb{n}$  ，  $C_n\subset \operatorname {Int}C_{n + 1}$  .]  
(f) 设  $C_n$  是 (e) 中所定义的集合，应用  $\bigcap U_{1/n}(C_n)$  在  $\mathcal{C}(X, \mathbb{R}^N)$  中稠密这一结论完成证明.

7. 推论 每一个  $m$ -维流形都可以嵌入到  $\mathbb{R}^{2m+1}$  中作为一个闭子空间。  
8. 称  $X$  为  $\sigma$ -紧致的，如果存在  $X$  的可数个紧致子空间的族，其内部覆盖  $X$ 。

定理 设  $X$  是一个  $\sigma$ -紧致的 Hausdorff 空间。如果  $X$  的每一个紧致子空间的拓扑维数最多为  $m$ ，那么  $X$  的拓扑维数也最多为  $m$ 。

证明：令  $\mathcal{A}$  是  $X$  的一个开覆盖，用以下方法找到  $X$  的另一个开覆盖  $\mathcal{B}$  加细  $\mathcal{A}$ ，并且  $\mathcal{B}$  的阶数最多为  $m + 1$ .

(a) 证明  $X = \bigcup X_{n}$ , 其中  $X_{n}$  是紧致的, 并且对于每一个  $n$ , 有  $X_{n} \subset \operatorname{Int} X_{n+1}$ . 设  $X_{0} = \varnothing$ .  
(b) 找到  $X$  的一个开覆盖  $\mathcal{B}_0$  加细  $\mathcal{A}$ ，并且对于每一个  $n$ ， $\mathcal{B}_0$  中与  $X_n$  相交的成员包含于  $X_{n+1}$ 。

(c) 设  $n \geqslant 0$ ， $\mathcal{B}_n$  是  $X$  的一个开覆盖，加细  $\mathcal{B}_0$ ，使得  $\mathcal{B}_n$  在  $X_n$  中的点的阶最多为  $m + 1$ 。选取  $X$  的一个开覆盖  $\mathcal{C}$  加细  $\mathcal{B}_n$ ，使得  $\mathcal{C}$  在  $X_{n+1}$  中的点的阶最多为  $m + 1$ 。选取  $f: \mathcal{C} \to \mathcal{B}_n$  使得  $C \subset f(C)$ ，对于  $B \in \mathcal{B}_n$ ，用  $D(B)$  表示所有满足  $f(C) = B$  的集合  $C$  的并。设

$\mathcal{B}_{n + 1}$  是由  $\mathcal{B}_n$  中所有满足  $B\cap X_{n - 1}\neq \emptyset$  的集合  $B$  ，以及  $\mathcal{B}_n$  中所有满足  $B\cap X_{n - 1} = \varnothing$  的集合  $B$  确定的集合  $D(B)$  所构成的族．证明  $\mathcal{B}_{n + 1}$  是  $X$  的一个开覆盖，加细  $\mathcal{B}_n$  ，并且在 $X_{n + 1}$  中的点的阶最多为  $m + 1$

(d)定义  $\mathcal{B}$  为：给定集合  $B$  ，若存在某一个  $N$  ，使得对于所有的  $n\geqslant N$  ，有  $B\in \mathcal{B}_n$  ，则有  $B\in \mathcal{B}$  9.推论每一个  $m$  -维流形的拓扑维数最多为  $m$

10. 推论  $\mathbb{R}^N$  的每一个闭子空间的拓扑维数最多为  $N$ .

11. 推论 空间  $X$  能嵌入到  $\mathbb{R}^N$  中作为一个闭子空间，其中  $N$  是某一个非负整数，当且仅当  $X$  是具有可数基的局部紧致的 Hausdorff 空间，并且具有有限拓扑维数。

### * 附加习题：局部欧氏空间

一个空间  $X$  称为局部  $\pmb{m}$  -维欧氏的(locally  $m$  -Euclidean)，如果对于每一个  $x\in X$  ，存在  $\pmb{x}$  的一个邻域同胚于  $\mathbb{R}^m$  中的一个开集．这样的空间自然满足  $T_{1}$  公理，但不一定是Hausdorff空间．（见第36节的习题.)若  $X$  还是一个Hausdorff空间，并且有可数基，那么称  $X$  为一个  $\pmb{m}$  维流形  $(m$  -manifold).

以下习题中统统假设  $X$  是局部  $m$ -维欧氏空间

1. 证明  $X$  是局部紧致的和局部可度量化的。  
2. 考虑关于  $X$  的以下条件：

(i)  $X$  是一个紧致的Hausdorff空间.  
(ii)  $X$  是一个  $m$ -维流形.  
(iii)  $X$  是可度量化的.  
(iv)  $X$  是正规的.  
(v)  $X$  是Hausdorff的.

证明：  $(\mathrm{i})\Rightarrow (\mathrm{ii})\Rightarrow (\mathrm{iii})\Rightarrow (\mathrm{iv})\Rightarrow (\mathrm{v}).$

3. 证明  $\mathbb{R}$  是局部1-维欧氏空间，并满足(ii)，但不满足(i).  
4. 证明  $\mathbb{R} \times \mathbb{R}$  在字典序拓扑下是局部 1-维欧氏空间，并且满足 (iii)，但不满足 (ii).  
5. 证明长直线是局部1-维欧氏空间，并且满足(iv)，但不满足(iii)．（见第24节的习题.)  
*6. 存在一个空间，它是局部2-维欧氏空间，满足(v)，但不满足(iv)．这个空间的构造方法如下：设  $A$  是  $\mathbb{R}^3$  的以下子空间：

$$
A = \{(x, y, 0) \mid x > 0 \}.
$$

给定实数  $c$  ，令  $B_{c}$  是  $\mathbb{R}^3$  的以下子空间：

$$
B _ {c} = \{(x, y, c) \mid x \leqslant 0 \}.
$$

设  $X$  为  $A$  和所有子空间  $B_{c}$  的并，其中  $c$  取遍所有实数．选取以下三种集合作为基将  $X$  拓扑化：

(i)  $U$  ，其中  $U$  在  $A$  中是开的.  
(ii)  $V$  ，其中  $V$  是子空间  $B_{c}$  中所有满足  $x < 0$  的点构成的  $B_{c}$  中的一个开集.  
(iii)对于  $\mathbb{R}$  的每一个开区间  $I = (a,b)$  、每一个实数  $c$  以及每一个  $\varepsilon >0$  ，集合  $A_{c}(I,\varepsilon)\cup$

$B_{\varepsilon}(I,\varepsilon)$  ，其中

$$
\begin{array}{l} A _ {c} (I, \varepsilon) = \{(x, y, 0) \mid 0 <   x <   \varepsilon \text {和} c + a x <   y <   c + b x \}, \\ B _ {c} (I, \varepsilon) = \{(x, y, c) \mid - \varepsilon <   x \leqslant 0 \text {和} a <   y <   b \}. \\ \end{array}
$$

空间  $X$  称为“Prüfer流形”

(a) 画出  $A_{c}(I, \varepsilon)$  和  $B_{c}(I, \varepsilon)$  的草图.  
(b) 证明  $(\mathrm{i}) \sim (\mathrm{iii})$  三种集合共同构成了  $X$  的拓扑的一个基.  
(c)证明：定义为

$$
f _ {c} (x, y) = \left\{ \begin{array}{l l} (x, c + x y, 0) & \text {对 于} x > 0, \\ (x, y, c) & \text {对 于} x \leqslant 0 \end{array} \right.
$$

的映射  $f_{c}$  ：  $\mathbb{R}^2\to X$  是  $\mathbb{R}^2$  和  $X$  的子空间  $A\cup B_{c}$  之间的一个同胚.

(d) 证明  $A \cup B_{c}$  在  $X$  中是开的。证明  $X$  是 2-维欧氏空间。  
(e) 证明  $X$  是Hausdorff的.  
(f) 证明  $X$  不是正规的. [提示:  $X$  的子空间

$$
L = \{(0, 0, c) \mid c \in \mathbb {R} \}
$$

是闭的和离散的．与第31节中的习题3比较.

7. 证明:  $X$  是Hausdorff的当且仅当  $X$  是完全正则的.  
8. 证明:  $X$  是可度量化的当且仅当  $X$  是仿紧致的和Hausdorff 的.  
9. 证明：若  $X$  是可度量化的，则  $X$  的每一个分支都是一个  $m$ -维流形。
