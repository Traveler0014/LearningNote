# 集合与映射

## 集合

一堆元素.

### 集合的运算

集合与集合运算得到另一个集合.
$$
A \oplus B=C
$$
目的在于判别参与运算各集合中的元素是否属于运算结果.

#### 算子

> $A$,$B$: 任意集合
>
> $U$: 全集
>
> $\varnothing$: 空集

交: 同时属于两个集合的元素.
$$
A \cap B = C\\
a \in A \and a \in B \\
\to
a \in C
$$
差: 只属于算符左侧集合的元素.
$$
A - B = C\\
a \in A \and a \notin B\\
\to
a \in C
$$
对称差: 只属于其中一个集合的元素. 
$$
A \oplus B = (A - B) + (B - A) = C\\
(a \in A \and a \notin B) \or  (a \notin A \and a \in B)\\
\to
a \in C
$$
并: 属于其中任意一个集合的元素.
$$
A \cup B \\
a \in A \or a \in B \\
\to
a \in C
$$
补: 不属于某个集合的元素.
$$
\overline{A} = U - A = C \\
a \notin A \and a \in U \\
\to
a \in C
$$

#### 等幂律

$$
A \cap A = A \\
A \cup A = A
$$

#### 交换律

$$
A \cap B = B \cap A \\
A \cup B = B \cup A \\
A \oplus B = B \oplus A
$$

#### 结合律

$$
A \cap (B \cap C) = (A \cap B) \cap C \\
A \cup (B \cup C) = (A \cup B) \cup C \\
A \oplus (B \oplus C) = (A \oplus B) \oplus C
$$

#### 分配律

$$
A \cap (B \cup C) = (A \cap B) \cup (A \cap C) \\
A \cup (B \cap C) = (A \cup B) \cap (A \cup C)
$$

#### 同一律

$$
A \cap U = A \\
A \cup \varnothing = A \\
A - \varnothing = A \\
A \oplus \varnothing = A
$$

#### 零一律

$$
A \cap \varnothing = \varnothing \\
A \cup U = U
$$

#### 补余律

$$
A \cap \overline{A} = \varnothing \\
A \cup \overline{A} = U
$$

#### 吸收律

$$
A \cup (A \cap B) = A \\
A \cap (A \cup B) = A
$$

#### De Morgan律

$$
A - (B \cup C) = (A - B) \cap (A - C) \\
A - (B \cap C) = (A - B) \cup (A - C) \\
\overline{A \cup B} = \overline{A} \cap \overline{B} \\
\overline{A \cap B} = \overline{A} \cup \overline{B} \\
\overline{\varnothing} = U \\
\overline{U} = \varnothing
$$

#### 双重否定律

$$
\overline{\overline{A}} = A
$$



## 映射

一堆元素与一堆元素的对应关系.

---

# 数列与级数

## 数列

按顺序排列的一列数, 每项是一个数.

### 数列的极限

#### 唯一性

若数列存在极限, 则其极限必唯一.

#### 有界性

若数列存在极限, 则该数列必有界.

#### 保号性

> 设数列$\{a_{n}\}$存在极限$a$, 且$a>0$, 则存在正整数$N$, 当$n>N$时有$a_n>0$.

若数列极限在原点某侧, 则在项数足够大时, 其后所有项的符号均位于极限同侧.

### 敛散性

#### 数列收敛

必要条件: 有界.

充分条件: 单调有界.

#### 区间套定理

存在区间序列满足每个区间都包含于前一个区间内, 且区间端点之差趋近零, 则存在唯一一点$x_0$包含于该序列所有区间内. 

#### 聚点原理

有界数列必存在收敛的子数列. 

#### 柯西收敛原理

数列$\{a_n\}$收敛的充要条件为: 对任给$\varepsilon>0$, 存在正整数$N$, 使得对所有满足$m>N, n>N$的$m, n$有$|a_m-a_n|<\varepsilon$. 

## 级数

按顺序排列的一列数, 但每项都是一列数之和.

#### 正项级数

##### 比值判别法

##### 根值判别法



#### 交错级数

正负项交错出现的级数.
$$
\sum\limits_{n=1}^{\infty}(-1)^{n-1}a_n\\
a_n>0,n\in\Bbb{N}^{+}
$$

##### 莱布尼兹判别法



#### 变号级数

符号会发生改变的级数.
$$
\sum\limits_{n=1}^{\infty}a_n\\
a_n \in \Bbb{R}
$$

若其对应的正项级数$\sum\limits_{n=1}^{\infty}|a_{n}|$**通过比值或根值判别法判断发散**, 则原级数发散. 

若正项级数收敛, 则原级数必收敛. 

若正项级数发散而原级数收敛, 则称该变号级数**条件收敛**. 若正项级数和原级数同时收敛, 则称该变号级数**绝对收敛**. 

### 性质

#### 可交换性

绝对收敛的级数交换其前后项的位置, 结果仍绝对收敛. 

#### 乘法

两个绝对收敛的级数其各项乘积所得级数和$\sum\limits_{i,j=1}^{\infty}a_{i}b_{j}$仍绝对收敛, 且和等于原级数收敛和的乘积. 

##### 柯西乘积

在绝对收敛的条件下,有
$$
\sum\limits_{n=1}^{\infty}a_{n} \cdot \sum\limits_{n=1}^{\infty}b_{n} = \sum\limits_{n=1}^{\infty}(a_{n}b_{1}+a_{n-1}b_{2}+...+a_{1}b_{n})
$$
**应用**:

已知$q<1$时, 几何乘积$\sum\limits_{n=0}^{\infty}q^{n}$绝对收敛.

则有: 
$$
\sum\limits_{n=0}^{\infty}q^{n} \cdot \sum\limits_{n=0}^{\infty}q^{n} = \sum\limits_{n=0}^{\infty}(n+1)q^{n} \\
\because \sum\limits_{n=0}^{\infty}q^{n} = \frac{1}{1-q} \\
\therefore \frac{1}{(1-q)^{2}} = \sum\limits_{n=0}^{\infty}(n+1)q^{n}
$$

### 敛散性判别

**收敛必要条件**: 级数通项极限为零. 

#### 一般性流程

1. 判断通项极限是否为零, 若不为零, 级数发散.
2. 判断是否为正项级数, 若为正项级数, 采用**比较判别法**(不等式与极限形式), **根值判别法**, **比值判别法**判断敛散性. 
3. 判断是否为交错级数$\sum(-1)^{n-1}u_{n}$, 若$u_{n}$单调下降, 则原级数收敛. 
4. 利用级数运算性质和其他判别法. 

#### 柯西收敛原理



---

## 附录

### 三角不等式:

> $$
> ||a|-|b||\leq|a\pm b|\leq|a|+|b|
> $$

三角形两边之差小于等于第三边, 两边之和大于等于第三边(等号成立时, 三边共线). 

