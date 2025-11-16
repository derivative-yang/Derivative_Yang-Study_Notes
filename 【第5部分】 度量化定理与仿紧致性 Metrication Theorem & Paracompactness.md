# 第27节 局部有限性
## 27-1 局部有限性
什么样的拓扑空间是可度量化的呢？第4章中的Urysohn度量化定理朝着解决这个问题的方向迈出了第一步，也是一大步，给出了空间  $X$  可以度量化的一个充分条件： $X$  是正则的，并且具有可数基．但是只要能证得一个更强的结论，数学家们就决不会满足于已有的这个定理．现在，人们有希望通过在  $X$  上寻找一个使  $X$  可度量化的充分必要条件，即与可度量性等价的条件来强化这个定理.

我们知道，在Urysohn度量化定理中正则性的假定是必要的，而可数基的条件却不是。于是一个很自然的想法就是用一些较弱的条件取代可数基条件。寻找这样的条件需要一些技巧。因为这个条件一方面要强到足以得出空间的可度量性，另一方面又要弱到使每一个可度量化空间都能满足它。但是，难就难在如何发现正确的假设，一旦发现了正确的假设，离成功也就为期不远了。

这个条件终于被J. Nagata和Y. Smirnov各自独立找到了，其中涉及到一个新概念，即局部有限性概念。空间  $X$  的一个子集族  $\mathcal{A}$  称为局部有限的，指的是在  $X$  的每一点处有一个邻域只和  $\mathcal{A}$  中有限多个成员相交。

我们现在可以把基  $\mathcal{B}$  可数这个条件说成  $\mathcal{B}$  可以表为

$$
\mathcal {B} = \bigcup_ {n \in \mathbf {Z} _ {+}} \mathcal {B} _ {n},
$$

其中每一个族  $\mathcal{B}_n$  是有限的．这是一个笨拙的表达方式，但是它启发我们怎样去表达一个较弱的情形，Nagata-Smirnov条件就是要求基  $\mathcal{B}$  可以表示成以下形式

$$
\mathcal {B} = \bigcup_ {n \in \mathbf {Z} _ {+}} \mathcal {B} _ {n},
$$

其中每一个族  $\mathcal{B}_n$  是局部有限的。这样的族  $\mathcal{B}$  称为可数局部有限的。出人意外的是这个条件加上正则性正好是  $X$  可度量化的充分必要条件。

拓扑学中还有一个概念涉及局部有限性，这就是所谓“仿紧致性”的概念，它是紧致性概念的一个推广。尽管这一概念的出现并不很久，但已经在许多数学分支上被证明是有用的。我们在这里引入它，是为了给出  $X$  可度量化的另一个充分必要条件，即  $X$  是可度量化的当且仅当  $X$  既是仿紧致的又是局部可度量化的。在第42节中将证明这个结论。

本章有些节之间是彼此独立的，它们之间的依从关系如下表所示：

![](187dc39166cf1a304dfa10b6a72271e1d179f6e351b81c7480d8ecb637853061.jpg)



在本节中，我们证明局部有限族的一些性质以及关于可度量化空间的一个关键性引理.

定义 设  $X$  是一个拓扑空间。 $X$  的一个子集族  $\mathcal{A}$  称为局部有限的 (locally finite)，若  $X$  中的每一点都存在一个邻域只与  $\mathcal{A}$  的有限多个成员相交。

例1 可以验证，在拓扑空间  $\mathbb{R}$  中，区间族

$$
\mathcal {A} = \{(n, n + 2) \mid n \in \mathbb {Z} \}
$$

是局部有限的．另一方面，族

$$
\mathcal {B} = \{(0, 1 / n) \mid n \in \mathbb {Z} _ {+} \}
$$

在(0，1)中是局部有限的，但在  $\mathbb{R}$  中却不是．同样，族

$$
\mathcal {C} = \{(1 / (n + 1), 1 / n) \mid n \in \mathbb {Z} _ {+} \}
$$

也是如此.

引理39.1 设  $\mathcal{A}$  是  $X$  的一个局部有限的子集族．则

(a)  $\mathcal{A}$  的任意子族是局部有限的.  
(b)  $\mathcal{A}$  中元素的闭包构成的族  $\mathcal{B} = \{\overline{A}\}_{A\in \mathcal{A}}$  是局部有限的.  
(c)  $\overline{\bigcup_{A\in\mathbf{A}}A} = \bigcup_{A\in \mathbf{A}}\overline{A}$

证 (a) 是显然的。以下证明 (b)。注意，与  $\overline{A}$  相交的任何开集  $U$  也必然与  $A$  相交。因此，如果  $U$  是  $x$  的一个邻域，它仅与  $\mathcal{A}$  中有限多个成员  $A$  相交，那么  $U$  最多只能与族  $\mathcal{B}$  中同样个数的成员相交（可能与  $\mathcal{B}$  中更少的成员相交，因为即使  $A_{1}$  与  $A_{2}$  不等， $\overline{A}_{1}$  与  $\overline{A}_{2}$  相等也是可能的）。

为了证明(c)，令  $Y$  表示  $\mathcal{A}$  的所有成员的并

$$
\bigcup_ {A \in A} A = Y.
$$

易见， $\bigcup \overline{A} \subset \overline{Y}$ 。在局部有限的条件下，我们证明相反的包含关系也成立。设  $x \in \overline{Y}$ ， $U$  是  $x$  的一个邻域，它只与  $\mathcal{A}$  中有限多个成员  $A_1, \cdots, A_k$  相交。我们将证明  $x$  必属于  $\overline{A}_1, \cdots, \overline{A}_k$  中的某一个，因而属于  $\bigcup \overline{A}$ 。否则，集合  $U - \overline{A}_1 - \cdots - \overline{A}_k$  就是  $x$  的一个邻域，它不与  $\mathcal{A}$  中任何成员相交，从而不与  $Y$  相交，这与假设  $x \in \overline{Y}$  矛盾。

对于  $X$  的加标子集族也有与局部有限类似的概念。加标族  $\{A_{\alpha}\}_{\alpha \in J}$  称为局部有限的加标族 (locally finite indexed family)，如果  $X$  中的每一个元素  $x$  都存在一个邻域仅和有限多个  $A_{\alpha}$  相交。局部有限性的这两种叙述之间有什么关系呢？容易看到  $\{A_{\alpha}\}_{\alpha \in J}$  为局部有限的加标族当且仅当作为集族它是局部有限的，并且  $X$  的每一个非空子集  $A$  最多只对有限多个  $\alpha$  有  $A$  与  $A_{\alpha}$  相等。

局部有限加标族只会在第41节中处理单位分拆时用到，到时候我们再来关注局部有限加标族.

定义  $X$  的子集族  $\mathcal{B}$  称为可数局部有限的(countably locally finite)，若  $\mathcal{B}$  可以表示成可数个局部有限族  $\mathcal{B}_n$  的并.

这一概念也叫做“ $\sigma$  局部有限”，其中  $\sigma$  来自测度论，表示“可数并”。注意，可数族和局部有限族都是可数局部有限的。

定义 设  $\mathcal{A}$  是  $X$  的子集族， $X$  的子集族  $\mathcal{B}$  称为  $\mathcal{A}$  的加细 (refinement)（或称为加细  $\mathcal{A}$ ），若对于  $\mathcal{B}$  中的每一个元素  $B$ ，存在  $\mathcal{A}$  的一个元素  $A$  包含  $B$ 。若  $\mathcal{B}$  中的每一个元素都是开集，则称  $\mathcal{B}$  是  $\mathcal{A}$  的开加细 (open refinement)。若  $\mathcal{B}$  中的每一个元素都是闭集，则称其为  $\mathcal{A}$  的闭加细 (closed refinement)。

引理39.2 设  $X$  是一个可度量化空间．若  $\mathcal{A}$  是  $X$  的一个开覆盖，则存在  $X$  的可数局部有限的开覆盖  $\mathcal{E}$  加细  $\mathcal{A}$

证为了证明这个引理，我们要用到良序定理．对于集族  $\mathcal{A}$  选取一个良序  $<$  ，用字母  $U$ $V,W,\dots$  表示  $\mathcal{A}$  的元素.

选定  $X$  的一个度量．设  $_n$  是一个暂时固定的正整数．给定  $\mathcal{A}$  中的一个元素  $U$  ，我们定义 $S_{n}(U)$  为

$$
S _ {n} (U) = \{x \mid B (x, 1 / n) \subset U \}.
$$

它是  $U$  的一个子集，通过“缩紧” $U \frac{1}{n}$  的距离得到． $(S_{n}(U)$  是一个闭集，但这一点对于我们并不重要.)现在，我们用  $\mathcal{A}$  的良序  $<$  来讨论一个更小的集合．对于  $\mathcal{A}$  中的每一个  $U$  ，定义

$$
T _ {n} (U) = S _ {n} (U) - \bigcup_ {V <   U} V.
$$

如图39.1所示，其中  $\mathcal{A}$  由三个集合  $U < V < W$  组成。这个图形正好反映出所得到的这些集合是无交的。

![](7608bd348a7de83a2f330de6f2774a3b6b3dfdf3460c79568ddc2a57091d0735.jpg)  
图 39.1

事实上，可以断言，它们至少被分开了  $1 / n$  的距离。也就是说，如果  $V$  和  $W$  是  $\mathcal{A}$  中两个不同的元素，那么对于任意  $x \in T_{n}(V)$  和  $y \in T_{n}(W)$ ，有  $d(x, y) \geqslant 1 / n$ 。

为了证明这一事实，设已选定  $V < W$ 。由  $x \in T_n(V)$ ，可得  $x \in S_n(V)$ ，从而  $B(x, 1/n) \subset V$ 。另一方面，因为  $V < W$ ，并且  $y \in T_n(W)$ ，根据  $T_n(W)$  的定义可见  $y \notin V$ ，于是  $d(x, y) \geqslant 1/n$ 。

然而集合  $T_{n}(U)$  仍然不是我们想要的，因为它不是开集(实际上它是闭集)，所以还需将其放大一点，使之成为一个开集  $E_{n}(U)$ 。特别地，令  $E_{n}(U)$  为  $T_{n}(U)$  的  $\frac{1}{3n}$ -邻域，也就是说

$E_{n}(U)$  是所有开球  $B\left(x, \frac{1}{3n}\right)$  （其中  $x \in T_{n}(U)$ ）的并.

在  $U < V < W$  的假设下，如图39.2所示，我们所得到的集合是无交的．事实上，若  $V$  和 $W$  是  $\mathcal{A}$  中不同的两个元素，那么对于任意  $x\in E_n(V)$  和  $y\in E_n(W)$  ，一定有  $d(x,y)\geqslant 1 / (3n)$  这一结论根据三角不等式容易得到．注意，任意  $V\in \mathcal{A}$  ，集合  $E_{n}(V)$  包含于  $V$

![](ad38d73b6b598ad330fcf676660267e783905bf6c219c02b25e786693c021181.jpg)  
图39.2

现在，我们来定义

$$
\mathcal {E} _ {n} = \left\{E _ {n} (U) \mid U \in \mathcal {A} \right\}.
$$

我们断言： $\mathcal{E}_n$  是一个局部有限的开集族，并且加细  $\mathcal{A}$ 。 $\mathcal{E}_n$  加细  $\mathcal{A}$  是因为对于每一个  $V \in \mathcal{A}$ ，有  $E_n(V) \subset V$ 。再由任意  $x \in X$ ， $B(x, 1/(6n))$  最多与  $\mathcal{E}_n$  中的一个元素相交，可见  $\mathcal{E}_n$  是局部有限的。

当然， $\mathcal{E}_n$  并不是  $X$  的一个覆盖。（图39.2说明了这一点。）然而我们可以断言：集族

$$
\mathcal {E} = \bigcup_ {n \in \mathbb {Z} _ {+}} \mathcal {E} _ {n}
$$

覆盖  $X$

设  $x \in X$ ，族  $\mathcal{A}$  如前所述是  $X$  的一个覆盖。选取  $U$  为  $\mathcal{A}$  中包含  $x$  的第一个集合（按良序  $\langle \rangle$ ）。由于  $U$  是一个开集，所以可以选取适当的  $n$  使得  $B(x, 1/n) \subset U$ 。于是，根据定义易见  $x \in S_n(U)$ 。因为  $U$  是  $\mathcal{A}$  中包含  $x$  的第一个元素，所以  $x \in T_n(U)$ ，从而  $x$  也属于  $\mathcal{E}_n$  中的元素  $E_n(U)$ 。证明完成。

## 练习

1. 验证例 1 中的结论.  
2. 找出  $\mathbb{R}$  的一个开覆盖  $\mathcal{A}$ ，使得  $\mathcal{A}$  是点态有限的，却不是局部有限的。（集族  $\mathcal{A}$  称为点态有限的，若  $\mathbb{R}$  中的每一个点只属于  $\mathcal{A}$  中的有限多个元素。）  
3. 试给出一集族  $\mathcal{A}$ ，使得  $\mathcal{A}$  本身不是局部有限的，但  $\mathcal{B} = \{\overline{A} \mid A \in \mathcal{A}\}$  是局部有限的。  
4. 设  $\mathcal{A}$  是  $\mathbb{R}$  的子集族，

$$
\mathcal {A} = \{(n, n + 2) \mid n \in \mathbb {Z} \}.
$$

以下哪个子集族加细  $\mathcal{A}$  ?

$$
\begin{array}{l} \mathcal {B} = \{(x, x + 1) \mid x \in \mathbb {R} \}, \\ \mathcal {C} = \left\{\left(n, n + \frac {3}{2}\right) \mid n \in \mathbb {Z} \right\}, \\ \mathcal {D} = \left\{\left(x, x + \frac {3}{2}\right) \mid x \in \mathbb {R} \right\}. \\ \end{array}
$$

5. 证明：如果  $X$  有可数基，那么  $X$  的一个子集族  $\mathcal{A}$  是可数局部有限的当且仅当它是可数的。  
6. 在一致拓扑下考察  $\mathbb{R}^n$ 。给定  $n$ ，令  $\mathcal{B}_n$  为  $\mathbb{R}^n$  中所有形如  $\Pi A_i$  的子集族，其中，对于  $i \leqslant n$ ， $A_i = \mathbb{R}$ ；对于其他情形， $A_i$  等于  $\{0\}$  或者  $\{1\}$ 。证明：集族  $\mathcal{B} = \bigcup \mathcal{B}_n$  是可数局部有限的，却既不是可数的，也不是局部有限的。
# 第28节 Nagata-Smirnov度量化定理
## 28-1 Nagata-Smirnov度量化定理


现在我们来证明空间  $X$  是正则的且存在可数局部有限基就等价于  $X$  可度量化.

这些条件蕴涵可度量性的证明，非常接近于我们给出的Urysohn度量化定理的第二个证明．我们在那个证明中构造了一个从  $X$  到  $\mathbb{R}^{\omega}$  的映射，它是关于  $\mathbb{R}^{\omega}$  的一致度量  $\bar{\rho}$  的一个嵌入.这就使我们想起这个证明的主要步骤．证明的第一步是证明每一个具有可数基的正则空间是正规的．第二步是构造  $X$  上的一个可数的实值函数族  $\{f_{\alpha}\}$  ，使它能分离点和闭子集．第三步是利用函数  $f_{n}$  定义一个映射，把  $X$  嵌入到积空间  $\mathbb{R}^{\omega}$  中．第四步是说明，若对任意  $x\in X$  ，都有 $f_{n}(x)\leqslant 1 / n$  ，那么这个映射实际上是从  $X$  到度量空间  $(\mathbb{R}^{\omega},\bar{\rho})$  的一个嵌入.

为了证明一般的度量化定理，这些步骤的每一步都要加以推广。第一，我们证明具有可数局部有限基的正则空间是正规的。第二，在  $X$  上构造某个实值函数族  $\{f_n\}$ 。第三，用这些函数把  $X$  嵌入到积空间  $\mathbb{R}^J$  中（对某一个  $J$ ）。第四步是说明，若函数  $f_{\alpha}$  充分小，那么实际上它将  $X$  嵌入到度量空间  $(\mathbb{R}^J, \bar{\rho})$  中。

在证明之前，我们回顾一下在前面习题中引入的  $G_{\delta}$  集的概念.

定义 如果空间  $X$  的一个子集  $A$  等于  $X$  的可数个开子集的交，则称  $A$  为  $X$  中的一个  $\pmb{G}_{\delta}$  集  $(G_{\delta}$  set).

例1 显然， $X$  的每一个开子集是一个  $G_{\delta}$  集。在第一可数的Hausdorff空间中，每一个单点集是一个  $G_{\delta}$  集。可以验证， $\bar{S}_{\Omega}$  的单点子集  $\{\Omega\}$  不是  $G_{\delta}$  集。

例2 在度量空间  $X$  中，每一个闭集是一个  $G_{\delta}$  集．给定  $A \subset X$  ，用  $U(A, \varepsilon)$  表示  $A$  的  $\varepsilon$ -邻域. 可以验证，若  $A$  是闭集，则有

$$
A = \bigcap_ {n \in \mathbf {Z} _ {+}} U (A, 1 / n).
$$

引理40.1 设  $X$  是一个正则空间并且具有一个可数局部有限基  $\mathcal{B}$ ，则  $X$  是正规的，并且  $X$  中每一个闭集都是  $X$  的一个  $G_{\delta}$  集。

证 第一步．设  $W$  是  $X$  的一个开集，我们将证明存在  $X$  的开集的一个可数族  $\{U_n\}$ ，使得

$$
W = \bigcup U _ {n} = \bigcup \bar {U} _ {n}.
$$

因为  $\mathcal{B}$  是  $X$  的一个可数局部有限基，所以可以写成  $\mathcal{B} = \bigcup \mathcal{B}_n$  ，其中每一个族  $\mathcal{B}_n$  都是局部有限的．设  $\mathcal{C}_n$  是  $\mathcal{B}$  中满足  $B\in \mathcal{B}_n$  并且  $\bar{B}\subset W$  的那些元素  $B$  构成的族．那么  $\mathcal{C}_n$  是局部有限

的，因为它是  $\mathcal{B}_n$  的子集的一个族．定义

$$
U _ {n} = \bigcup_ {B \in \mathcal {C} _ {n}} B,
$$

那么  $U_{n}$  是开集，并且根据引理39.1，

$$
\bar {U} _ {n} = \bigcup_ {B \in \mathfrak {C} _ {n}} \bar {B}.
$$

因此  $\bar{U}_n\subset W$  ，从而

$$
\bigcup U _ {n} \subset \bigcup \bar {U} _ {n} \subset W.
$$

我们断言等号成立．给定  $x \in W$  ，由正则性可见，存在  $B \in \mathcal{B}$  使得  $x \in B$  和  $\bar{B} \subset W$  ：现在，对某一个  $n$  有  $B \in \mathcal{B}_n$  ，根据定义可见  $B \in \mathcal{C}_n$  ，所以  $x \in U_n$  ：于是  $W \subset \bigcup U_n$

第二步．我们证明  $X$  的每一个闭集  $C$  都是  $G_{\delta}$  集．给定闭集  $C$  ，令  $W = X - C$  ．由第一步知，存在  $X$  中的集合  $U_{n}$  ，使得  $W = \bigcup \overline{U}_n$  ．于是

$$
C = \cap (X - \bar {U} _ {n}),
$$

即  $C$  等于  $X$  中可数个开集的交

第三步．证明  $X$  是正规的．设  $C$  和  $D$  为  $X$  中两个无交的闭集．对于开集  $X - D$  应用第一步构造一个可数开集族  $\{U_n\}$  ，使得  $\bigcup U_n = \bigcup \overline{U}_n = X - D.$  于是  $\{U_n\}$  覆盖  $C$  ，并且每一个  $\overline{U}_n$  都与  $D$  无交．类似地，存在  $D$  的可数开覆盖  $\{V_n\}$  ，并且每一个  $V_n$  的闭包也与  $C$  无交.

现在我们再来回顾关于具有可数基的正则空间是正规的空间的证明(定理32.1)，这里可以一字不变地重新陈述那个证明．令

$$
U _ {n} ^ {\prime} = U _ {n} - \bigcup_ {i = 1} ^ {n} \bar {V} _ {i}, \quad V _ {n} ^ {\prime} = V _ {n} - \bigcup_ {i = 1} ^ {n} \bar {U} _ {i}.
$$

则集合

$$
U ^ {\prime} = \bigcup_ {n \in \mathbb {Z} _ {+}} U _ {n} ^ {\prime}, \quad V ^ {\prime} = \bigcup_ {n \in \mathbb {Z} _ {+}} V _ {n} ^ {\prime}
$$

是分别包含  $C$  和  $D$  的无交的开集.

引理40.2 设  $X$  是一个正规空间， $A$  是  $X$  的一个闭的  $G_{\delta}$  子集，则存在连续函数  $f: X \to [0, 1]$ ，使得当  $x \in A$  时有  $f(x) = 0$ ；当  $x \notin A$  时有  $f(x) > 0$ 。

证 在第33节中曾将此命题作为练习给出，在这里我们给出证明。设  $A$  为可数个开集  $U_{n}$  的交， $n \in \mathbb{Z}_{+}$ ，对于每一个  $n$ ，选取一个连续函数  $f_{n}: X \to [0,1]$ ，使得当  $x \in A$  时， $f_{n}(x) = 0$ ，当  $x \in X - U_{n}$  时  $f_{n}(x) = 1$ 。定义函数  $f(x) = \sum f_{n}(x)/2^{n}$ 。通过与  $\sum 1/2^{n}$  比较可见，这个序列是一致收敛的，所以  $f$  是连续的，并且在  $A$  上取值为0，在  $X - A$  上取正值。

定理40.3[Nagata-Smirnov度量化定理(Nagata-Smirnov metrization theorem)] 空间  $X$  是可度量化的当且仅当  $X$  是正则的并且有一个可数局部有限基.

证 第一步。设  $X$  是正则的并且有一个可数局部有限基  $\mathcal{B}$ ，则  $X$  是正规的，并且  $X$  的每一个闭子集是一个  $G_{\delta}$  集。对于某一个  $J$ ，下面我们将把  $X$  嵌入到度量空间  $(\mathbb{R}^J, \bar{\rho})$  中，从而说明  $X$  是可度量化的。

设  $\mathcal{B} = \bigcup \mathcal{B}_n$  ，其中每一个集族  $\mathcal{B}_n$  是局部有限的．对于每一个正整数  $n$  和  $\mathcal{B}_n$  中的任意一个基元素  $B$  ，选取一个连续函数

$$
f _ {n, B}: X \longrightarrow [ 0, 1 / n ],
$$

使得对任意  $x \in B$  有  $f_{n,B}(x) > 0$ ，对于  $x \notin B$  有  $f_{n,B}(x) = 0$ 。于是，函数族  $\{f_{n,B}\}$  分离  $X$  中的点和闭集：因为对于任意给定的点  $x_0$  和  $x_0$  的一个邻域  $U$ ，都存在一个基元素  $B$ ，使得  $x_0 \in B \subset U$ ，并且对某一个  $n$  有  $B \in \mathcal{B}_n$ ，从而  $f_{n,B}(x_0) > 0$ ，并且  $f_{n,B}(x_0)$  在  $U$  的补集上取零值。

设  $J$  是  $\mathbb{Z}_{+} \times \mathcal{B}$  的一个子集，它由满足  $B \in \mathcal{B}_n$  的所有偶对  $(n, B)$  组成．定义

$$
F: X \longrightarrow [ 0, 1 ] ^ {J}
$$

为

$$
F (x) = \left(f _ {n, B} (x)\right) _ {(n, B) \in J}.
$$

根据定理34.2，相对于  $[0,1]^J$  的积拓扑而言，映射  $F$  是一个嵌入.

现在我们在  $[0, 1]^J$  上取由一致度量  $\bar{\rho}$  所诱导的拓扑，并且证明相对于这个拓扑， $F$  也是一个嵌入。这便是需要条件  $f_{n,B}(x) < 1 / n$  的地方。一致拓扑是比积拓扑更细（大）的，因此，相对于一致度量，映射  $F$  是单射，并且将  $X$  中的开集变成像空间  $Z = F(X)$  的开集。我们只要再证明  $F$  连续就够了。

注意，在  $\mathbb{R}^J$  的子空间[0，1]上，一致度量等价于度量

$$
\rho \left(\left(x _ {\alpha}\right), \left(y _ {\alpha}\right)\right) = \sup  \left\{\left| x _ {\alpha} - y _ {\alpha} \right| \right\}.
$$

为了证明连续性，我们取定  $X$  的一个点  $x_0$  和一个数  $\varepsilon > 0$ ，并取定  $x_0$  的一个邻域  $W$ ，使得

$$
x \in W \Longrightarrow \rho (F (x), F (x _ {0})) <   \varepsilon .
$$

暂时固定  $n$  ，选取  $x_0$  的一个邻域  $U_{n}$  ，使得它只与族  $\mathcal{B}_n$  中的有限多个成员相交．这就是说，当  $B$  在  $\mathcal{B}_n$  上变动时，函数  $f_{n,B}$  除了有限多个以外其他的在  $U_{n}$  上都恒等于0．因为每一个函数  $f_{n,B}$  是连续的，所以我们可以选取  $x_0$  的一个邻域  $V_{n}$  包含于  $U_{n}$  ，并且在  $V_{n}$  上，当  $B\in \mathcal{B}_n$  时，每一个保留下来的函数  $f_{n,B}$  最多改变  $\varepsilon /2$

对于每一个  $n \in \mathbb{Z}_{+}$  选择  $x_{0}$  的上述邻域  $V_{n}$ ，然后选取  $N$ ，使得  $1 / N \leqslant \epsilon / 2$ ，并且定义  $W = V_{1} \cap \dots \cap V_{N}$ 。可以断言， $W$  就是所要求的  $x_{0}$  的那个邻域。令  $x \in W$ 。如果  $n \leqslant N$ ，因为函数  $f_{n,B}$  在  $W$  上或者恒等于 0，或者最多改变  $\epsilon / 2$ ，所以

$$
\left| f _ {n, B} (x) - f _ {n, B} \left(x _ {0}\right) \right| \leqslant \varepsilon / 2.
$$

如果  $n > N$  ，因为  $f_{n,B}$  把  $X$  映入  $[0,1 / n]$  中，所以

$$
\mid f _ {n, B} (x) - f _ {n, B} \left(x _ {0}\right) \mid \leqslant 1 / n <   \varepsilon / 2.
$$

综上，最后得到

$$
\rho (F (x), F (x _ {0})) \leqslant \varepsilon / 2 <   \varepsilon .
$$

第二步．现在我们来证明定理的另一方面．设  $X$  是可度量化的．易见  $X$  是正则的．以下将证明  $X$  有可数局部有限基.

选取  $X$  的一个度量．给定  $m$  ，用  $\mathcal{A}_m$  表示所有半径为  $1 / m$  的开球构成的  $X$  的开覆盖．根据引理39.2可见，存在  $X$  的一个可数局部有限的开覆盖  $\mathcal{B}_m$  加细  $\mathcal{A}_m$  ．注意  $\mathcal{B}_m$  中的每一个元素的直径最多为  $2 / m$  ．令  $\mathcal{B} = \bigcup_{m\in \mathbb{Z}_{+}}\mathcal{B}_{m}$  ，因为每一个  $\mathcal{B}_m$  是可数局部有限的，所以  $\mathcal{B}$  也是可数

局部有限的．我们来证明  $\mathcal{B}$  是  $X$  的一个基

给定  $x \in X$  和  $\varepsilon > 0$ ，下面将证明存在  $B \in \mathcal{B}$ ，使得  $x \in B$  并且  $B \subset B(x, \varepsilon)$ 。先选取  $m$ ，使得满足  $1/m < \varepsilon/2$ 。由于  $\mathcal{B}_m$  覆盖  $X$ ，可以选取  $\mathcal{B}_m$  中的一个元素  $B$ ，使得  $x \in B$ 。从而由  $x \in B$  和  $B$  的直径最多为  $2/m < \varepsilon$  可见  $B$  包含于  $B(x, \varepsilon)$ 。

## 练习


1. 验证例 1 和例 2.  
2.  $X$  的子集  $W$  称为一个  $F_{\sigma}$  集，若它等于  $X$  的可数个闭子集的并．证明  $W$  是  $X$  中的一个  $F_{\sigma}$  集当且仅当  $X - W$  是  $X$  的  $G_{\delta}$  集.

[这一术语源于法语．“F”代表“ferme”，意为“闭集”，“σ”代表“somme”，意为“并”。]

3. 许多空间都有可数基，但  $T_{1}$  空间没有局部有限基，除非它是离散的。试证明这一命题。  
4. 找一个非离散的空间，它有可数局部有限基，却没有可数基。  
5.  $X$  的子集族  $\mathcal{A}$  称为局部离散的 (locally discrete), 若对  $X$  中的每一个点都存在它的一个邻域最多只与  $\mathcal{A}$  中一个元素相交. 集族  $\mathcal{B}$  称为可数局部离散的 (countably locally discrete) (或  $\sigma$ -局部离散的), 若它等于可数个局部离散的集族的并. 证明下述命题:

定理（Bing可度量定理）一个空间  $X$  是可度量化的当且仅当它是正则的并且有一可数局部离散基.

# 第29节 仿紧致性
## 29-1 仿紧致性



仿紧致性概念是近年来出现的，它是紧致性概念的一种最有用的推广，特别是在拓扑学和微分几何中很有用。这里，我们只给出它的一个应用，这就是在下一节将要证明的度量化定理。

我们熟悉的许多空间都是仿紧致的。例如，每一个紧致空间都是仿紧致的，这一点可从定义直接推得。每一个可度量化空间也是仿紧致的，这就是我们将要证明的A．H．Stone推出的定理。这样，仿紧致空间就包含了我们已讨论过的两类重要空间，同时，它也包含其他的一些空间。

为了搞清楚仿紧致性是怎样由紧致性推广而来的，我们回忆一下紧致性的定义：一个空间  $X$  称为紧致的，如果  $X$  的每一个开覆盖包含一个覆盖  $X$  的有限子族．等价地说就是：

一个空间  $X$  是紧致的，如果  $X$  的任意一个开覆盖  $\mathcal{A}$  有有限的开加细  $\mathcal{B}$  覆盖  $X$ .

这个定义与通常的定义等价，因为给定了这样的加细  $\mathcal{B}$  之后，我们就可以对  $\mathcal{B}$  中每一个成员选取  $\mathcal{A}$  的一个成员包含它，于是就得到了  $\mathcal{A}$  的一个覆盖  $X$  的有限子族。

紧致性这种新的说法虽然比较繁琐，但是它蕴涵着一种推广的契机。

定义 空间  $X$  称为仿紧致的 (paracompact)，如果  $X$  的任意一个开覆盖  $\mathcal{A}$  有一个覆盖  $X$  的局部有限的开加细  $\mathcal{B}$ 。

许多作者仿照Bourbaki，在仿紧致性的定义中也要求  $X$  是一个Hausdorff空间，(Bourbaki在紧致的定义中要求了Hausdorff条件)这里我们不遵循这一方式.

例1 空间  $\mathbb{R}^n$  是仿紧致的。令  $X = \mathbb{R}^n$ 。设  $\mathcal{A}$  是  $X$  的一个开覆盖。令  $B_0 = \varnothing$ ，对于任意正整数  $m$ ， $B_m$  表示球心是坐标原点、半径为  $m$  的开球。给定  $m$ ，选取  $\mathcal{A}$  的有限多个元素覆盖  $\overline{B}_m$  并且都和开集  $X - \overline{B}_{m-1}$  相交。用  $\mathcal{C}_m$  表示这有限多个开集族。那么族  $\mathcal{C} = \bigcup \mathcal{C}_m$  就是  $\mathcal{A}$  的一个加细。显然  $\mathcal{C}$  是局部有限的。因为开集  $B_m$  只与其中有限多个元素相交（即  $\mathcal{C}_1 \cup \dots \cup \mathcal{C}_m$  中的元素）。最后， $\mathcal{C}$  覆盖  $X$ 。因为对于任意给定  $x$ ，设  $m$  是满足  $x \in \overline{B}_m$  的最小整数，根据定义可见， $x$  属于  $\mathcal{C}_m$  中的某一个元素。

仿紧致空间的某些性质类似于紧致空间的某些性质。例如，仿紧致空间的子空间未必仿紧致，但闭子空间一定是仿紧致的。仿紧致的Hausdorff空间必定是正规的。另一方面，仿紧致空间也有与紧致空间不同的地方，特别是两个仿紧致空间的积未必再是仿紧致的。稍后，我们将证明这一事实。

定理41.1 每一个仿紧致的Hausdorff空间  $X$  是正规的.

证 这一证明类似于紧致的Hausdorff空间是正规空间的证明.

首先证明正则性。设  $a$  是空间  $X$  的一个点， $B$  是不包含点  $a$  的一个闭子集。根据Hausdorff条件，对于  $B$  中的任意点  $b$ ，可以选取包含  $b$  的一个开集  $U_{b}$ ，使它的闭包仍然不包含点  $a$ 。这些开集  $U_{b}$  和开集  $X - B$  一起构成了  $X$  的一个覆盖，取  $X$  的一个局部有限开加细  $\mathcal{C}$  覆盖  $X$ 。将  $\mathcal{C}$  中所有与  $B$  相交的成员组成的子族记为  $\mathcal{D}$ ，则  $\mathcal{D}$  覆盖  $B$ 。进而，如果  $D \in \mathcal{D}$ ，则  $\overline{D}$  不包含点  $a$ ，因为  $D$  与  $B$  相交，所以它必定在某一个集合  $U_{b}$  中，而  $U_{b}$  的闭包不包含  $a$  点。令

$$
V = \bigcup_ {D \in \mathcal {D}} D.
$$

则  $V$  是  $X$  中包含  $B$  的开集．又因  $\mathcal{D}$  是局部有限的，

$$
\bar {V} = \bigcup_ {D \in \mathcal {D}} \bar {D},
$$

从而  $\bar{V}$  也不包含点  $a$  ，正则性得证

为了证明正规性，我们只须重复上面的论证，用闭集  $A$  代替点  $a$  ，用正则性代替Hausdorff条件就行了.

定理41.2 仿紧致空间的每一个闭子空间是仿紧致的。

证 设  $Y$  是仿紧致空间  $X$  的一个闭子空间， $\mathcal{A}$  是由  $Y$  中开集组成的  $Y$  的一个覆盖。对于每一个  $A \in \mathcal{A}$ ，选取  $X$  的一个开集  $A'$ ，使得  $A' \cap Y = A$ 。所有开集  $A'$  连同开集  $X - Y$  一起构成  $X$  的一个覆盖。同时，设  $\mathcal{B}$  是  $X$  的局部有限开覆盖，并且  $\mathcal{B}$  加细这一覆盖，于是，族

$$
\mathcal {C} = \{B \cap Y \mid B \in \mathcal {B} \}
$$

就是所要求的  $\mathcal{A}$  的局部有限开加细.

例2 Hausdorff空间  $X$  的仿紧致子空间未必是  $X$  的闭集．事实上，开区间(0，1)是仿紧致的，因为它同胚于  $\mathbb{R}$  ，但它却不是  $\mathbb{R}$  中的闭子集.

例3仿紧致空间的子空间未必是仿紧致的．空间  $\overline{S}_\alpha \times \overline{S}_\alpha$  是紧致的，因此是仿紧致的.但是子空间  $S_{\Omega}\times \bar{S}_{\Omega}$  却不是仿紧致的，因为它是Hausdorff的，却不是正规的.

为了证明每一个可度量化空间都是仿紧致的这个重要定理，我们还需要下面这一引理，它由E. Michael给出，并可用于其他目的。

引理41.3 设  $X$  是一个正则空间．则加在  $X$  上的下列条件等价①： $X$  的每一个开覆盖有一个加细，它是

(1)  $X$  的一个开覆盖，并且是可数局部有限的.  
(2)  $X$  的一个覆盖，并且是局部有限的.  
(3)  $X$  的一个闭覆盖，并且是局部有限的.  
(4)  $X$  的一个开覆盖，并且是局部有限的.

证  $(4) \Rightarrow (1)$  是显然的，对于我们打算证明的定理而言，需要证明的是它的逆命题。为此，我们要通过  $(1) \Rightarrow (2) \Rightarrow (3) \Rightarrow (4)$  这样的步骤来做。为方便起见，我们已将相应的条件列在引理的条文中了。

$(1) \Rightarrow (2)$ . 设  $\mathcal{A}$  是  $X$  的一个开覆盖,  $\mathcal{B}$  是  $\mathcal{A}$  的一个可数局部有限的开加细, 并且覆盖  $X$ . 令

$$
\mathcal {B} = \bigcup \mathcal {B} _ {n},
$$

其中每一个  $\mathcal{B}_n$  都是局部有限的.

现在我们利用与以前用过的收缩法基本相同的方法，从不同的  $\mathcal{B}_n$  作出一些两两无交的集合．给定  $i$  ，令

$$
V _ {i} = \bigcup_ {U \in \mathfrak {Z} _ {i}} U.
$$

再对于每一个  $n \in \mathbb{Z}_{+}$  和  $\mathcal{B}_n$  的每一个成员  $U$  ，定义

$$
S _ {n} (U) = U - \bigcup_ {i <   n} V _ {i}.
$$

[注意  $S_{n}(U)$  不一定是开的，也不一定是闭的.]令

$$
\mathcal {C} _ {n} = \left\{S _ {n} (U) \mid U \in \mathcal {B} _ {n} \right\}.
$$

则  $\mathcal{C}_n$  是  $\mathcal{B}_n$  的一个加细，因为对于每一个  $U\in \mathcal{B}_n$  ，  $S_{n}(U)\subset U$

令  $\mathcal{C} = \bigcup \mathcal{C}_n$  ，可以断言  $\mathcal{C}$  就是所要求的  $\mathcal{A}$  的局部有限加细，并且覆盖  $X$

设  $x$  是  $X$  的一个点，我们要证明  $x$  落入  $\mathcal{C}$  的某一个元素中，并且  $x$  有一个邻域，只与  $\mathcal{C}$  中的有限多个元素相交．考虑覆盖  $\mathcal{B} = \bigcup \mathcal{B}_n$  ，令  $N$  为满足以下条件的那个最小的整数：在  $\mathcal{B}_N$  中存在某元素包含着  $x$  ，设  $U$  是  $\mathcal{B}_N$  中包含着  $x$  的一个元素．首先注意，对于  $i < N$  ， $x$  不属于  $\mathcal{B}_i$  的任何元素，所以  $x$  在  $\mathcal{C}$  的元素  $S_n(U)$  中．其次，因为每一个族  $\mathcal{B}_n$  是局部有限的，所以对于每一个  $n = 1, \dots, N$  选取  $x$  的邻域  $W_n$  ，使它仅和  $\mathcal{B}_n$  中的有限多个成员相交．如果  $W_n$  与  $\mathcal{B}_n$  的成员  $S_n(V)$  相交，那么它也必与  $\mathcal{B}_n$  中的成员  $V$  相交，因为  $S_n(V) \subset V$  ，因此  $W_n$  仅和  $\mathcal{C}_n$  的有限多个成员相交．此外，因为  $U$  在  $\mathcal{B}_N$  中，所以对于  $n > N$  ， $U$  不与  $\mathcal{C}_n$  的任何成员相交．于是  $x$  的邻域

$$
\mathbf {W} _ {1} \cap \mathbf {W} _ {2} \cap \dots \cap \mathbf {W} _ {N} \cap U
$$

仅与  $\pmb{c}$  的有限多个成员相交

(2)  $\Rightarrow$  (3). 设  $\mathcal{A}$  是  $X$  的一个开覆盖,  $\mathcal{B}$  是  $X$  所有满足以下条件的开集  $U$  构成的集族:  $\overline{U}$ .

包含在  $\mathcal{A}$  的一个元素之中．由正则性可见  $\mathcal{B}$  覆盖  $X$  ，再应用(2)，可以找到  $X$  的一个覆盖  $\mathcal{C}$  加细  $\mathcal{B}$  ，并且  $\mathcal{C}$  是局部有限的．令

$$
\mathcal {D} = \{\bar {C} \mid C \in \mathfrak {c} \}.
$$

则  $\mathcal{D}$  也覆盖  $X$  ，根据引理39.1可见  $\mathcal{D}$  是局部有限的，并且加细  $\mathcal{A}$

$(3) \Rightarrow (4)$ . 设  $\mathcal{A}$  是  $X$  的一个开覆盖. 根据(3)，选取  $\mathcal{B}$  为  $X$  的一个局部有限的覆盖并且加细  $\mathcal{A}$ . （如果愿意的话，也可以取  $\mathcal{B}$  为闭加细，但这不是必要的.）我们希望将  $\mathcal{B}$  的每一个元素  $B$  稍加扩大，使之成为一个开集．此外，还要把这种扩大做得充分小，使得所得出的开集族仍然是局部有限的，并且仍然是  $\mathcal{A}$  的加细.

这一步包含着一个新的技巧。前面多次采用的办法都是先按照某种方式将集合排序，再用减掉前面所有集合的办法构造新集合。那种办法是缩小集合，而现在要扩大这些集合，我们必须要有不同的做法。我们将引进  $X$  的一个局部有限闭覆盖  $\mathcal{C}$  作为辅助，然后再用它扩大  $\mathcal{B}$  的成员。

对于  $X$  的每一点  $x$  ，存在  $x$  的一个邻域仅与  $\mathcal{B}$  的有限多个成员相交．那么所有满足仅与 $\mathcal{B}$  的有限多个成员相交这一条件的开集构成的族是  $X$  的一个开覆盖．再应用(3)，设  $\mathcal{C}$  是这个覆盖的一个闭加细，它覆盖  $X$  ，并且是局部有限的．于是  $\mathcal{C}$  的每一个成员也仅与  $\mathcal{B}$  的有限多个成员相交.

对于  $\mathcal{B}$  的每一个成员  $B$  ，令

$$
\mathcal {C} (B) = \{C \mid C \in \mathcal {C} \text {和} C \subset X - B \}.
$$

然后定义

$$
E (B) = X - \bigcup_ {C \in \mathcal {C} (B)} C.
$$

因为  $\mathcal{C}$  是一个局部有限的闭集族，根据引理39.1， $\mathcal{C}$  的任意子族的成员之并仍然是闭集，因此，集合  $E(B)$  是开集．此外，按定义， $B \subset E(B)$ ．（如图41.1所示，其中  $\mathcal{B}$  的成员表示为闭圆域及线段，而  $\mathcal{C}$  的成员表示为闭正方形区域.）

![](842a7585db5f9981906609adfc9a74de86cb6c66992db5d591f1cde310291857.jpg)  
图41.1

现在我们可能把每一个  $B$  扩得太大，集族  $\{E(B)\}$  可能不是  $\mathcal{A}$  的加细了．但这是容易弥补的．对于每一个  $B\in \mathcal{B}$  ，可以选取  $\mathcal{A}$  中包含  $B$  的成员  $F(B)$  ．然后定义

$$
\mathcal {D} = \left\{E (B) \cap F (B) \mid B \in \mathcal {B} \right\}.
$$

那么集族  $\mathcal{D}$  便是  $\mathcal{A}$  的一个加细．因为  $B\subset (E(B)\cap F(B))$  并且  $\mathcal{B}$  覆盖  $X$  ，所以  $\mathcal{D}$  也覆盖  $X$

最后，我们证明  $\mathcal{D}$  是局部有限的．给定  $X$  的一个点  $x$  ，选取  $x$  的邻域  $W$  ，使得它只与  $\mathcal{C}$  的有限多个成员，比如说  $C_1,\dots ,C_k$  相交．下证  $W$  只与  $\mathcal{D}$  中有限多个元素相交．因为  $\mathcal{C}$  是  $X$  的一个覆盖，故  $W$  被  $C_1,\dots ,C_k$  所覆盖．由此只需说明  $\mathcal{C}$  中的每一个成员  $C$  仅与  $\mathcal{D}$  中有限多个成员相交．若  $C$  与集合  $E(B)\cap F(B)$  相交，则  $C$  与  $E(B)$  相交．根据  $E(B)$  的定义，  $C$  不可能含在  $X - B$  中，从而它必与  $B$  相交．因为  $C$  仅与  $\mathcal{B}$  中有限多个元素相交，因此它最多与 $\mathcal{D}$  中同样多个集合相交.

定理41.4 每一个可度量化空间都是仿紧致的。

证 设  $X$  是一个可度量化空间，根据引理39.2可见， $X$  的每一个开覆盖  $\mathcal{A}$ ，有  $X$  的一个可数局部有限的开覆盖加细它，前述引理蕴涵着开覆盖  $\mathcal{A}$  有覆盖  $X$  的一个局部有限的开加细。

定理41.5 每一个正则的Lindelof空间是仿紧致的，

证 设  $X$  是正则的Lindelof空间．给定  $X$  的一个开覆盖  $\mathcal{A}$ ，那么它有一个可数子族覆盖  $X$ ，这个可数子族当然是可数局部有限的．由前述引理可见， $\mathcal{A}$  有局部有限的开加细覆盖  $X$ 。

例4 两个仿紧致空间的积未必是仿紧致的。空间  $\mathbb{R}_t$  是仿紧致的，因为它是正则的Lindelof空间。但  $\mathbb{R}_t \times \mathbb{R}_t$  却不是仿紧致的，因为它是一个Hausdorff空间但不是正规的。

例5 空间  $\mathbb{R}^n$  在积拓扑和一致拓扑下都是仿紧致的．这是因为这些拓扑下， $\mathbb{R}^n$  都是可度量化的．在箱拓扑下  $\mathbb{R}^n$  是否是仿紧致的并不知道．（见第32节习题5.）

例6 若  $J$  是不可数的，那么积空间  $\mathbb{R}^J$  就不是仿紧致的。因为  $\mathbb{R}^J$  是Hausdorff的却不是正规的。

仿紧致空间具有很多有用的性质，其中一条就被用来处理空间  $X$  上单位分拆的存在性。对于这个概念，其有限情形下的表达形式我们已在第36节中提到过，现在我们来讨论更一般的情况。先来回顾一个概念：设  $\phi: X \to \mathbb{R}$ ，那么  $\phi$  的支撑就是所有满足  $\phi(x) \neq 0$  的点  $x$  构成的集合的闭包。

定义 设  $\{U_{\alpha}\}_{\alpha \in J}$  是  $X$  的一个加标开覆盖。一个加标的连续函数族

$$
\phi_ {\alpha}: X \longrightarrow [ 0, 1 ]
$$

称为  $X$  的由  $\{U_{\alpha}\}$  所控制的一个单位分拆(partition of unity)，若：

(1)对于每一个  $\alpha$  ，  $\phi_{\alpha}$  的支撑包含于  $U_{\alpha}$  
(2)加标族  $\{\phi_{\alpha}$  的支撑}是局部有限的.  
(3) 对于每一个  $x$ ， $\sum \phi_{a}(x) = 1$

条件(2)蕴涵着：每一个  $x \in X$  都有一个邻域，除了有限多个  $\alpha$  外，其他的  $\phi_{\alpha}$  在此邻域上取值都为0．因此我们可以明白条件(3)中“取和”的意思了．我们解释这些是为了说明“和”是对那些不为0的  $\phi_{\alpha}(x)$  求取的.

我们现在来构造任意一个仿紧致的Hausdorff空间上的单位分拆．正如在第36节中处理有限的情形那样，我们先来证明一个“收缩引理”

$\hat{\mathbf{\alpha}}$  引理41.6设  $X$  是仿紧致的Hausdorff空间，  $\{U_{\alpha}\}_{\alpha \in J}$  是  $X$  的加标开覆盖．那么存在  $X$  的一个局部有限的加标开覆盖  $\{V_{\alpha}\}_{\alpha \in J}$  ，使得对于每一个  $\alpha$  ，有  $\bar{V}_{\alpha} \subset U_{\alpha}$

对于每一个  $\alpha$  有  $\bar{V}_{\alpha} \subset U_{\alpha}$ ，这一条件有时也被表述为：集族  $\{\bar{V}_{\alpha}\}$  是集族  $\{U_{\alpha}\}$  的精加细（precise refinement）.

证 令  $\mathcal{A}$  为所有那些开集  $A$  的族，要求这些开集  $A$  满足条件： $\overline{A}$  包含于族  $\{U_{\alpha}\}$  的某一个元素之中。根据  $X$  的正则性可见， $\mathcal{A}$  是  $X$  的一个覆盖。因为  $X$  是仿紧致的，所以可以找到  $X$  的一个局部有限的开覆盖  $\mathcal{B}$  加细  $\mathcal{A}$ 。我们用某一个指标集  $K$  来一一地给  $\mathcal{B}$  加标，这样  $\mathcal{B}$  中的成员就可以表示为  $B_{\beta}$ ， $\beta \in K$ ，并且  $\{B_{\beta}\}_{\beta \in K}$  是一个局部有限的加标族。因为  $\mathcal{B}$  加细  $\mathcal{A}$ ，我们可以定义映射  $f: K \to J$ ，使得对于每一个  $\beta \in K$ ， $f(\beta) \in J$ ，使得

$$
\bar {B} _ {\beta} \subset U _ {f (\beta)}.
$$

对于每一个  $\alpha \in J$  ，我们定义  $V_{\alpha}$  为集族

$$
\mathcal {B} _ {\alpha} = \left\{B _ {\beta} \mid f (\beta) = \alpha \right\}
$$

中成员的并．（注意，如果没有指标  $\beta$  使得  $f(\beta) = \alpha$  ，  $V_{\alpha}$  便是空集.）对于  $\mathcal{B}_{\alpha}$  的每一个成员  $B_{\beta}$  根据定义有  $\overline{B}_{\beta} \subset U_{\alpha}$  ，因为集族  $\mathcal{B}_{\alpha}$  是局部有限的，故  $\overline{V}_{\alpha}$  为集族  $\{\mathcal{B}_{\alpha}\}$  中成员的闭包的并，因此  $\overline{V}_{\alpha} \subset U_{\alpha}$

最后，我们来验证局部有限性．给定  $x\in X$  ，选取  $\pmb{x}$  的一个邻域  $W$  使得只有有限多个  $\beta$  设为  $\beta = \beta_{1},\dots ,\beta_{K}$  ，使得  $B_{\beta}$  与  $W$  相交．那么仅当  $\alpha$  是指标  $f(\beta_1)$  ，…，  $f(\beta_K)$  中的某一个时， $W$  与  $V_{\alpha}$  相交.

定理41.7 设  $X$  是仿紧致的Hausdorff空间， $\{U_{\alpha}\}_{\alpha \in J}$  是  $X$  的一个加标开覆盖．则存在 $X$  的被  $\{U_{\alpha}\}$  控制的一个单位分拆.

证 我们先两次使用收缩引理，以获得  $X$  的一个局部有限的加标开覆盖  $\{W_{\alpha}\}$  和  $\{V_{\alpha}\}$ ，使得对于每一个  $\alpha$ ，有  $\overline{W}_{\alpha} \subset V_{\alpha}$  和  $\overline{V}_{\alpha} \subset U_{\alpha}$ 。因为  $X$  是正规的，所以对于每一个  $\alpha$  我们可以选取一个连续函数  $\psi_{\alpha}: X \to [0,1]$ ，使得  $\psi_{\alpha}(\overline{W}_{\alpha}) = \{1\}$  并且  $\psi_{\alpha}(X - V_{\alpha}) = \{0\}$ 。因为  $\psi_{\alpha}$  的函数值非 0 的点只在  $V_{\alpha}$  中取到，所以

$$
(\psi_ {\alpha} \text {的 支 撑}) \subset \overline {{{V}}} _ {\alpha} \subset U _ {\alpha}.
$$

进而，还可见  $\{\bar{V}_{\alpha}\}$  是局部有限的．（因为一个开集只有当它与  $V_{\alpha}$  相交的情况下，它才能与  $\bar{V}_{\alpha}$  相交.)因此加标族  $\{\psi_{\alpha}$  的支撑》也是局部有限的．注意  $\{W_{\alpha}\}$  是  $X$  的覆盖，所以对于任意给定的 $x\in X$  ，至少存在一个  $\psi_{\alpha}$  在  $\pmb{x}$  点上取正值.

无限和

$$
\Psi (x) = \sum_ {a} \psi_ {a} (x)
$$

是有意义的。因对任意一个  $x \in X$ ，存在一个邻域  $W_x$ ，使得在  $(\psi_\alpha$  的支撑)中只有有限多个成员与之相交。我们可以说这个无限和就是(有限多个)非0项的和，由此可见，将  $\Psi$  限制在  $W_x$  上就等于有限多个连续函数的和。因此它在  $X$  上也是连续的，并且总取正值。现在定义

$$
\phi_ {\alpha} (x) = \psi_ {\alpha} (x) / \Psi (x),
$$

这便得到了所求的单位分拆.

数学中单位分拆常被用来“拼凑”函数，即将局部定义的函数“拼凑”起来以获得一个全局有定义的函数。第36节中对它们的使用已说明了这一过程，这里是另一个例子。

* 定理 41.8 设  $X$  是一个仿紧致的 Hausdorff 空间。 $\mathcal{C}$  是  $X$  的一个子集族。对于每一个  $C \in \mathcal{C}$ ，设  $\varepsilon_{C}$  是一个正数。如果  $\mathcal{C}$  是局部有限的，那么存在一个连续函数  $f: X \to \mathbb{R}$ ，使得对于所有  $x$  有  $f(x) > 0$ ，同时对于  $x \in C$  有  $f(x) \leqslant \varepsilon_{C}$ 。

证 选取  $X$  的一个开覆盖，它的每一个成员最多与  $\mathcal{C}$  中有限多个元素相交。将此开集族变成一个加标族  $\{U_{\alpha}\}_{\alpha \in J}$ 。选取  $X$  上的一个由  $\{U_{\alpha}\}$  控制的单位分拆  $\{\phi_{\alpha}\}$ 。给定  $\alpha$ ，当  $C$  取遍  $\mathcal{C}$  中所有与  $\phi_{\alpha}$  的支撑相交的元素时，设  $\delta_{\alpha}$  是所有  $\varepsilon_{C}$  中极小的数。若没有这样的元素  $C$ ，令  $\delta_{\alpha} = 1$ 。然后定义

$$
f (x) = \sum \delta_ {a} \phi_ {a} (x).
$$

因为所有的  $\delta_{\alpha}$  都是正的，因此  $f$  也是正的．下面我们要说明的是，对于  $x \in C$  ，有  $f(x) \leqslant \varepsilon_{C}$  为此只需说明，对于任意  $x \in C$  和任意  $\alpha$  ，有

$$
\delta_ {\alpha} \phi_ {\alpha} (x) \leqslant \varepsilon_ {C} \phi_ {\alpha} (x); \tag {*}
$$

当  $\sum \phi_{\alpha}(x) = 1$  时，所要求证的不等式成立。若  $x \notin \phi_{\alpha}$  的支撑，则由于  $\phi_{\alpha}(x) = 0$ ，可见所求证的不等式是显然的。若  $x \in \phi_{\alpha}$  的支撑，并且  $x \in C$ ，那么  $C$  与  $\phi_{\alpha}$  的支撑相交，因此  $\delta_{\alpha} \leqslant \varepsilon_{C}$ ，所以不等式  $(*)$  成立。
## 练习

1. 举例说明，空间  $X$  是仿紧致的，但未必它的每一个开覆盖  $\mathcal{A}$  有一个局部有限的子族覆盖  $\mathcal{A}$ .

2. (a) 证明：一个仿紧致的空间和一个紧致空间构成的积空间是仿紧致的。[提示：使用管状引理。]

(b) 证明:  $S_{\Omega}$  不是仿紧致的.

3. 每一个局部紧致的Hausdorff空间都是仿紧致的吗？

4. (a) 证明：若  $X$  具有离散拓扑，那么  $X$  是仿紧致的。

(b) 若  $f: X \to Y$  是连续的，并且  $X$  是仿紧致的，但  $Y$  的子空间  $f(X)$  未必是仿紧致的.

5. 设  $X$  是仿紧致的。对于  $X$  的任意加标开覆盖我们已经证明了“收缩引理”，这里将要对  $X$  的任意局部有限加标族证明“扩张引理”。

引理 设  $\{B_{\alpha}\}_{\alpha \in J}$  是仿紧致的 Hausdorff 空间  $X$  的子集构成的局部有限的加标族. 则存在  $X$  的开子集构成的局部有限的加标族  $\{U_{\alpha}\}_{\alpha \in J}$ , 使得对于每一个  $\alpha$ ,  $B_{\alpha} \subset U_{\alpha}$ .

6. (a) 设  $X$  是正则空间．若  $X$  能表示成自身的可数个紧致子空间的并，则  $X$  是仿紧致的.

(b) 证明  $\mathbb{R}^{\infty}$  作为  $\mathbb{R}^{\omega}$  的子空间，在箱拓扑下是仿紧致的。

*7. 设  $X$  是正则空间.

(a) 若  $X$  是有限个仿紧致的闭子空间的并，那么  $X$  是仿紧致的.

(b) 若  $X$  是可数个仿紧致的闭子空间的并, 并且这些闭子空间的内部覆盖  $X$ , 那么  $X$  是仿紧致的.

8. 设  $p: X \to Y$  是一个完备映射。（参见第31节的习题7.）

(a) 证明：若  $Y$  是仿紧致的，那么  $X$  也是仿紧致的。[提示：若  $\mathcal{A}$  是  $X$  的一个开覆盖，选取由集合  $B$  构成的  $Y$  的一个局部有限开覆盖，要求  $B$  满足条件  $p^{-1}(B)$  能被  $\mathcal{A}$  中有限多个元素覆盖。然后取  $p^{-1}(B)$  与  $\mathcal{A}$  中元素的交。]

(b) 证明：若  $X$  是仿紧致的 Hausdorff 空间，则  $Y$  也是仿紧致的 Hausdorff 空间。[提示：若  $\mathcal{B}$  是  $X$  的一个局部有限的闭覆盖，则  $\{p(B) \mid B \in \mathcal{B}\}$  是  $Y$  的局部有限的闭覆盖。]

9. 设  $G$  是局部紧致的连通拓扑群。证明  $G$  是仿紧致的。[提示：设  $U_{1}$  是  $\pmb{e}$  的有紧致闭包的一个邻域，归纳地定义  $U_{n+1} = \overline{U}_{n} \cdot U_{1}$ 。证明  $\overline{U}_{n}$  的并在  $G$  中是既开又闭的。]

没有连通的条件，此结论依然成立，但证明要困难些。

10. 定理 设  $X$  是局部紧致的和仿紧致的 Hausdorff 空间，那么  $X$  的每一个分支有一个可数基。

证明：设  $X_0$  是  $X$  的一个分支，那么  $X_0$  是局部紧致的和仿紧致的。设  $\mathcal{C}$  是  $X_0$  的一个局部有限的覆盖，它的每一个成员是  $X_0$  中的开集并且有紧致的闭包。设  $U_1$  是  $\mathcal{C}$  中的一个非空成员，一般地， $U_n$  是  $\mathcal{C}$  中所有与  $\overline{U}_{n-1}$  相交的成员的并。证明  $\overline{U}_n$  是紧致的，并且这些集合  $U_n$  覆盖  $X_0$ 。

# 第30节 Smirnov度量化定理
## 30-1 Smirnov度量化定理

Nagata-Smirnov度量化定理给出了空间可度量化的一个充分必要条件．在本节中，我们给出另一个度量化定理，它是Nagata-Smirnov定理的一个推论，是由Smirnov首先证明的.

定义 称空间  $X$  是局部可度量化的 (locally metrizable), 如果  $X$  的每一点  $x$  有一个邻域  $U$  在子空间拓扑之下是可度量化的.

定理42.1[Smirnov度量化定理(Smirnov metrization theorem)] 空间  $X$  可度量化当且仅当  $X$  是仿紧致的Hausdorff空间，并且是局部可度量化的。

证 假定  $X$  可度量化．根据定理41.4可见， $X$  是局部可度量化的，也是仿紧致的.

反之，假设  $X$  是仿紧致的Hausdorff空间，并且是局部可度量化的．我们只需证明  $X$  有一个可数局部有限基．因为  $X$  是正则的，根据Nagata-Smirnov定理可见  $X$  是可度量化的.

将定理40.3证明的后一部分调整一下就是这里的证明。先用一些可度量化的开集来覆盖  $X$ ，然后选取这个覆盖的一个局部有限开加细  $\mathcal{C}$  覆盖  $X$ 。 $\mathcal{C}$  的每一个成员  $C$  都是可度量化的。设函数  $d_{\mathbb{C}}: C \times C \to \mathbb{R}$  是给出  $C$  的拓扑的一个度量。给定  $x \in X$ ，用  $B_{\mathbb{C}}(x, \varepsilon)$  表示  $C$  中所有满足  $d_{\mathbb{C}}(x, y) < \varepsilon$  的点  $y$  构成的集合，因为  $B_{\mathbb{C}}(x, \varepsilon)$  是  $C$  的一个开集，所以也是  $X$  的一个开集。

给定  $m \in \mathbb{Z}_{+}$ , 令  $\mathcal{A}_m$  为半径是  $1 / m$  的开球构成的  $X$  的覆盖, 即

$$
\mathcal {A} _ {m} = \{B _ {C} (x, 1 / m) \mid x \in C \text {且} C \in \mathcal {C} \}.
$$

设  $\mathcal{D}_m$  为  $\mathcal{A}_m$  的覆盖  $X$  的一个局部有限开加细。（此处用到了仿紧致性。）设  $\mathcal{D}$  是这些集族  $\mathcal{D}_m$  的并。则  $\mathcal{D}$  是可数局部有限的。我们断言  $\mathcal{D}$  是  $X$  的一个基，从而定理得证。

设  $x$  是  $X$  的一个点， $U$  是  $x$  的一个邻域．我们设法找到  $\mathcal{D}$  的一个成员  $U$ ，使得  $x \in D \subset U$ ．现在， $x$  仅属于  $\mathcal{C}$  中有限多个成员，比如说属于  $C_1, \dots, C_k$ ．于是在集合  $C_i$  中， $U \cap C_i$

是  $x$  的一个邻域，所以存在一个  $\varepsilon_{i} > 0$  使得

$$
B _ {C _ {i}} (x, \varepsilon) \subset (U \cap C _ {i}).
$$

选取  $m$  ，使得  $2 / m < \min \{\varepsilon_1,\dots ,\varepsilon_k\}$  ，因为族  $\mathcal{D}_m$  覆盖  $X$  ，因此  $\mathcal{D}_m$  中必存在一个成员  $D$  包含 $x$  ．因为  $\mathcal{D}_m$  加细  $\mathcal{A}_m$  ，所以对某一个  $C\in \mathbb{C}$  及某一个  $y\in C$  ，必存在  $\mathcal{A}_m$  的一个成员  $B_{C}(y,1 / m)$  包含  $D$  .因为

$$
x \in D \subset B _ {c} (y, 1 / m),
$$

所以  $x$  属于  $C$  ，从而  $C$  必然是集合  $C_1, \cdots, C_k$  中的一个，比如说  $C = C_i$  。又因  $B_C(y, 1/m)$  的直径最多为  $2/m < \varepsilon_i$  ，于是，我们有

$$
x \in D \subset B _ {c _ {i}} (y, 1 / m) \subset B _ {c _ {i}} (x, \varepsilon_ {i}) \subset U.
$$

## 练习

Nagata-Smirnov度量化定理给出了空间可度量化的一个充分必要条件．在本节中，我们给出另一个度量化定理，它是Nagata-Smirnov定理的一个推论，是由Smirnov首先证明的.

定义 称空间  $X$  是局部可度量化的 (locally metrizable), 如果  $X$  的每一点  $x$  有一个邻域  $U$  在子空间拓扑之下是可度量化的.

定理42.1[Smirnov度量化定理(Smirnov metrization theorem)] 空间  $X$  可度量化当且仅当  $X$  是仿紧致的Hausdorff空间，并且是局部可度量化的。

证 假定  $X$  可度量化．根据定理41.4可见， $X$  是局部可度量化的，也是仿紧致的.

反之，假设  $X$  是仿紧致的Hausdorff空间，并且是局部可度量化的．我们只需证明  $X$  有一个可数局部有限基．因为  $X$  是正则的，根据Nagata-Smirnov定理可见  $X$  是可度量化的.

将定理40.3证明的后一部分调整一下就是这里的证明。先用一些可度量化的开集来覆盖  $X$ ，然后选取这个覆盖的一个局部有限开加细  $\mathcal{C}$  覆盖  $X$ 。 $\mathcal{C}$  的每一个成员  $C$  都是可度量化的。设函数  $d_{\mathbb{C}}: C \times C \to \mathbb{R}$  是给出  $C$  的拓扑的一个度量。给定  $x \in X$ ，用  $B_{\mathbb{C}}(x, \varepsilon)$  表示  $C$  中所有满足  $d_{\mathbb{C}}(x, y) < \varepsilon$  的点  $y$  构成的集合，因为  $B_{\mathbb{C}}(x, \varepsilon)$  是  $C$  的一个开集，所以也是  $X$  的一个开集。

给定  $m \in \mathbb{Z}_{+}$ , 令  $\mathcal{A}_m$  为半径是  $1 / m$  的开球构成的  $X$  的覆盖, 即

$$
\mathcal {A} _ {m} = \{B _ {C} (x, 1 / m) \mid x \in C \text {且} C \in \mathcal {C} \}.
$$

设  $\mathcal{D}_m$  为  $\mathcal{A}_m$  的覆盖  $X$  的一个局部有限开加细。（此处用到了仿紧致性。）设  $\mathcal{D}$  是这些集族  $\mathcal{D}_m$  的并。则  $\mathcal{D}$  是可数局部有限的。我们断言  $\mathcal{D}$  是  $X$  的一个基，从而定理得证。

设  $x$  是  $X$  的一个点， $U$  是  $x$  的一个邻域．我们设法找到  $\mathcal{D}$  的一个成员  $U$ ，使得  $x \in D \subset U$ ．现在， $x$  仅属于  $\mathcal{C}$  中有限多个成员，比如说属于  $C_1, \dots, C_k$ ．于是在集合  $C_i$  中， $U \cap C_i$

是  $x$  的一个邻域，所以存在一个  $\varepsilon_{i} > 0$  使得

$$
B _ {C _ {i}} (x, \varepsilon) \subset (U \cap C _ {i}).
$$

选取  $m$  ，使得  $2 / m < \min \{\varepsilon_1,\dots ,\varepsilon_k\}$  ，因为族  $\mathcal{D}_m$  覆盖  $X$  ，因此  $\mathcal{D}_m$  中必存在一个成员  $D$  包含 $x$  ．因为  $\mathcal{D}_m$  加细  $\mathcal{A}_m$  ，所以对某一个  $C\in \mathbb{C}$  及某一个  $y\in C$  ，必存在  $\mathcal{A}_m$  的一个成员  $B_{C}(y,1 / m)$  包含  $D$  .因为

$$
x \in D \subset B _ {c} (y, 1 / m),
$$

所以  $x$  属于  $C$  ，从而  $C$  必然是集合  $C_1, \cdots, C_k$  中的一个，比如说  $C = C_i$  。又因  $B_C(y, 1/m)$  的直径最多为  $2/m < \varepsilon_i$  ，于是，我们有

$$
x \in D \subset B _ {c _ {i}} (y, 1 / m) \subset B _ {c _ {i}} (x, \varepsilon_ {i}) \subset U.
$$
