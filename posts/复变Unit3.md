---
title: 复变函数Unit3

date: 2025-10-11

tags: [复变,Tech]

pinned: false

cover: /5.jpg
---



## 第三章：复变积分

### 3.1 复变积分

1. **函数沿曲线C的积分**：

   $$\int_C f(z)dz=\lim\limits_{max|\Delta z|\to 0}\sum_{k=1}^{n} f(\zeta_k)\Delta k$$

   其中$\zeta_k$时$z_{k-1}\to z_k$段的任意一点

   一个复变积分其实是两个实变线积分的有序组合：

   $$\int_C f(z)dz=\int_C (u+iv)(dx+idy)=\int_C(udx-vdy)+i\int_C(vdx+udy)$$

2. **复变积分的性质**：

   - **函数拆分性**：

     $$\int_C[f_1(z)+f_2(z)+...+f_n(z)]dz=\int_C f_1(z)dz+ \int_C f_2(z)dz+...\int_Cf(z)dz$$

   - **区域拆分性**：如果$C=C_1+C_2+...+C_n$

     $$\int_C f(z)dz=\int_{C_1}f(z)dz+\int_{C_2}f(z)dz+...+\int_{C_n}f(z)dz$$

   - **区域逆向性**：设C-是曲线C的逆向

     $$\int_{C-}f(z)dz=-\int_C f(z)dz$$

   - **绝对值不等式**：

     $$|\int_C f(z)dz|\le\int_C|f(z)||dz|$$

   - **常见放缩**：M为$|f(z)|$在C的上界，l为C的长度

     $$|\int_Cf(z)dz|\le Ml$$

### 3.2 Cauchy 定理

**Cauchy定理**：如果函数 f(z) 在有界闭区$\overline G$中解析，则沿$\overline G$的边界C，有：

$$\oint_C f(z)dz=0$$

**Cauchy定理可以表述成复变函数的变形定理**：若f(z)在区域G内解析，C为G内简单闭合曲线， 如果能将曲线C在G内连续地变形成曲线C'，则有：

$$\oint_C f(z)dz=\oint_{C'}f(z)dz$$

**常用结论**：

$$\oint_C (z-a)^n dz=\begin{cases} 2\pi i&n=-1，且C内含有z=a\\0 &其他情形 \end{cases}$$

**推论**：若f(z)在**有界单连通区域G**内解析，则复变积分$\int_C f(z)dz$与路径C无关，其中$C\subseteq G$
*这里需要特别注意，一旦积分的上、下限给定，则在一个有界单连通区域内，上面的积分
值一定与路径无关，但对于不同的有界单连通区域，可能会给出不同的积分值.*

**复变函数的不定积分**：$\int f(z)dz=F(z)+C$

### 3.3 两个有用的引理：
**小圆弧引理**：如果函数$f(z)$在z=a点的空心领域内连续。并且在$\theta_1\le arg(z-a) \le \theta_2$中，且有$\lim\limits_{|z-a|\to 0}(z-a)f(z)=k$，则有：
$$\lim\limits_{\delta \to 0}f(z)dz=ik(\theta_2-\theta_1)$$
$|z-a|=\delta$ 、$\theta_1\le arg(z-a) \le \theta_2$的几何意义：其中$C_{\delta}$是以 z=a为圆心、 $\delta$为半径、张角为$\theta_2-\theta_1$的圆弧 

**大圆弧定理**：设 f(z) 在∞点的邻域内连续，在$\theta_1\le arg z \le \theta_2$中，$\lim\limits_{|z|\to \infty}zf(z)=K$，则有：
$$\lim\limits_{R\to \infty}\int_{C_R}f(z)dz=iK(\theta_2-\theta_2)$$

### 3.4 Cauchy积分公式
**有界区域的Cauchy积分公式**：设f(z)是*有界闭区域*$\overline G$内的单值解析函数，$\overline G$的边界C是分段光滑曲线，a为G内一点，则有：
$$f(a)=\frac{1}{2\pi i}\oint_C \frac{f(z)}{z-a}dz$$
其中积分路径沿C的正向。

**均值定理**：Cauchy积分公式的特殊形式，取C为以a为圆心，R为半径的圆周，如果f(z)在圆内解析，则有：
$$f(a)=\frac{1}{2\pi}\int_0^{2\pi}f(a+Re^{i\theta})d\theta$$
**无界区域的Cauchy积分公式**：如果f(z)在简单闭合围道C和C外解析，且$\lim\limits_{z\to \infty}f(z)=0$，则有：
$$f(a)=\frac{1}{2\pi i}\oint_C \frac{f(z)}{z-a}dz$$
同上。

### 3.5 解析函数的高阶导数
**如果f(z)在有界闭区域$\overline G$内解析，则在G内f(z)的任何阶导数均存在**
$$f^{(n)}(z)=\frac{n!}{2\pi i}\oint_C \frac{f(\zeta)}{(\zeta-z)^{n+1}}d\zeta$$**ζ (Zeta)** 代表在闭合路径或轮廓 *C* 上的任意一点。它是一个“哑变量”或积分变量，意味着它只在积分计算的过程中有意义，最终的结果并不依赖于 ζ。

### 3.6 Cauchy型积分和含参量变量积分的解析性
**Cauchy型积分**：在一条分段光滑的(闭合或不闭合)曲线 C 上连续的函数$\phi(\zeta)$所构成的积分:
$$f(z)=\frac{1}{2\pi i}\int_C\frac{\phi(\zeta)}{\zeta-a}d\zeta$$
- 条件：
	- `f(z)` 可以用柯西积分公式来表示。
	- `f(z)` 在积分路径 `C` 上是连续的。
- 尽管 `φ(ζ)` 本身不一定是解析函数，但通过柯西型积分构造出来的新函数 `f(z)` **在曲线 `C` 外部的任何点 `z` 都是解析的**
- 并且f(z)的任意n(n为自然数)阶导数$f^n(z)$可通过积分号下求导而得到
$$f^{(n)}(z)=\frac{n!}{2\pi i}\oint_C \frac{f(\zeta)}{(\zeta-z)^{n+1}}d\zeta$$

| 特性       | 柯西积分公式                       | 柯西型积分                               |
| :------- | :--------------------------- | :---------------------------------- |
| **被积函数** | 在闭曲线`C`内部**解析**              | 只需在曲线`C`上**连续** (记为`φ(ζ)`)          |
| **积分路径** | 必须是**闭合**曲线 `C`              | 可以是闭合或不闭合的曲线 `C`                    |
| **结果**   | 给出曲线`C`内部一点`z`的**函数值**`f(z)` | 定义了一个在曲线`C`**外部**处处**解析**的新函数`f(z)` |
| **求导**   | 其高阶导数公式是此公式的特例               | 其任意阶导数可通过**积分号下求导**得到               |
