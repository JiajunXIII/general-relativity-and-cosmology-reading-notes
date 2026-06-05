---
title: 广义相对论与宇宙学 section 2.1 Lorentz变换
tags:
  - reading-note
  - relativity/special-relativity
  - weinberg
---

# 广义相对论与宇宙学 section 2.1 Lorentz变换

理解这一节时，最重要的是不要把它看成“公式清单”。Weinberg 真正要做的是：把狭义相对论中的“惯性系之间如何变换”定义清楚，并证明这种变换的核心作用是保持同一个时空间隔不变。

第一章的问题背景是这样的：Newton 力学适合 Galileo 变换，但 Maxwell 方程不适合 Galileo 变换。如果我们相信电磁学方程不是某个特殊惯性系里的偶然形式，那就不能继续把 Galileo 变换当成自然界最根本的惯性系变换。Einstein 的处理是把 Galileo 不变性换成 Lorentz 不变性。Weinberg 在这里不按历史顺序讲，而是直接定义 Lorentz 变换，再说明它为什么能作为自然定律的对称性。

为了把时间和空间放在同一个语言里，书中把四维坐标写成 $x^\alpha$。其中 $x^1,x^2,x^3$ 是空间坐标，$x^0=t$ 是时间坐标，并且采用 $c=1$。这意味着光速被当作单位速度，时间可以用长度单位来表示，所以 $t$ 和 $x^i$ 可以放进同一个四维对象里。

接下来引入 [[Minkowski度规号差与eta00|Minkowski metric]]：

$$
\eta_{\alpha\beta}
=
\mathrm{diag}(1,1,1,-1)
$$

也就是空间分量取正号，时间分量取负号。这样，原本写作

$$
d\tau^2=dt^2-d\mathbf{x}^2
$$

的固有时间隔，可以写成

$$
d\tau^2
=
-\eta_{\alpha\beta}dx^\alpha dx^\beta
$$

这里 $d\tau$ 是这一节的核心对象。不同惯性系可以不同意 $dt$，也可以不同意 $d\mathbf{x}$，但 Lorentz 变换要求它们必须同意组合 $dt^2-d\mathbf{x}^2$。

现在再看 Lorentz 变换的定义。原文写成

$$
x'^\alpha
=
\Lambda^\alpha{}_\beta x^\beta+a^\alpha
\tag{2.1.1}
$$

这里 $a^\alpha$ 是时空平移，它只是改变坐标原点；真正重要的是 $\Lambda^\alpha{}_\beta$，它描述时间和空间坐标怎样相互混合。由于平移对微分没有影响，所以对两个相邻事件来说，

$$
dx'^\alpha
=
\Lambda^\alpha{}_\beta dx^\beta
$$

重复指标默认求和，见 [[爱因斯坦求和约定|求和约定]]。为了让固有时间隔不变，我们要求

$$
d\tau'^2=d\tau^2
$$

把定义代入就是

$$
-\eta_{\alpha\beta}dx'^\alpha dx'^\beta
=
-\eta_{\gamma\delta}dx^\gamma dx^\delta
$$

再代入 $dx'^\alpha=\Lambda^\alpha{}_\gamma dx^\gamma$，得到

$$
-\eta_{\alpha\beta}
\Lambda^\alpha{}_\gamma
\Lambda^\beta{}_\delta
dx^\gamma dx^\delta
=
-\eta_{\gamma\delta}dx^\gamma dx^\delta
$$

因为这必须对任意 $dx^\gamma$ 都成立，所以二次型前面的系数必须相等：

$$
\Lambda^\alpha{}_\gamma
\Lambda^\beta{}_\delta
\eta_{\alpha\beta}
=
\eta_{\gamma\delta}
\tag{2.1.2}
$$

这就是 Lorentz 条件。用矩阵语言说，就是

$$
\Lambda^T\eta\Lambda=\eta
$$

所以这条公式的逻辑地位很明确：它不是随便规定的，而是“保持 $d\tau^2$ 不变”这个要求的矩阵表达。

这个条件马上解释了光速不变。光在 $c=1$ 的单位制中满足

$$
|d\mathbf{x}|=dt
$$

所以

$$
d\tau^2=dt^2-d\mathbf{x}^2=0
\tag{2.1.6}
$$

这叫 null interval。由于 Lorentz 变换保持 $d\tau^2$，如果一条光线在一个惯性系里满足 $d\tau=0$，换到另一个惯性系后仍然满足 $d\tau'=0$。换句话说，所有惯性系都同意哪些事件可以被光连接，因此所有惯性系测得的光速相同。

到这里，原文还没有结束。Weinberg 接着证明一个更强的结论：如果一个 [[非奇异坐标变换|非奇异坐标变换]] 保持所有 $d\tau^2$ 不变，那么它只能是上面这种线性形式加平移。假设有一般变换

$$
x'^\alpha=x'^\alpha(x)
$$

那么微分为

$$
dx'^\alpha
=
\frac{\partial x'^\alpha}{\partial x^\gamma}dx^\gamma
$$

若它保持间隔不变，就必须满足 [[式2.1.7的推导|式 (2.1.7) 的推导]]

$$
\eta_{\gamma\delta}
=
\eta_{\alpha\beta}
\frac{\partial x'^\alpha}{\partial x^\gamma}
\frac{\partial x'^\beta}{\partial x^\delta}
\tag{2.1.7}
$$

这个式子的意思是：这个一般变换的 [[Jacobian矩阵|Jacobian]] 在每一点都像 Lorentz 矩阵一样保持 $\eta$。但 [[Jacobian为何还可能随位置变化|它还可能随位置变化]]，所以还要继续约束它。

对上式再对 $x^\varepsilon$ 求导，右边用乘积法则展开。然后原文通过 [[自由指标交换后的方程为何仍成立|交换指标]] $\gamma,\varepsilon,\delta$，把几个等式相加相减，消掉不需要的项，最后得到 [[从式2.1.7到二阶导数约束|二阶导数约束]]

$$
0
=
2\eta_{\alpha\beta}
\frac{\partial^2 x'^\alpha}
{\partial x^\gamma\partial x^\varepsilon}
\frac{\partial x'^\beta}{\partial x^\delta}
$$

这里的消项还依赖 [[哑指标与自由指标|哑指标与自由指标]] 的区别；例如 [[倒数第二项与第四项相消的原因|倒数第二项与第四项相消]] 不是因为自由指标可以随便交换，而是因为哑指标可重命名、$\eta_{\alpha\beta}$ 对称且混合偏导可交换。

由于 $\eta_{\alpha\beta}$ 非奇异，Jacobian 也非奇异，所以只能推出 [[非奇异矩阵为何推出二阶导数为零|二阶导数为零]]

$$
\frac{\partial^2 x'^\alpha}
{\partial x^\gamma\partial x^\varepsilon}
=
0
\tag{2.1.8}
$$

二阶导数为零说明 $x'^\alpha$ 对 $x^\beta$ 只能是线性函数加常数，也就是

$$
x'^\alpha
=
\Lambda^\alpha{}_\beta x^\beta+a^\alpha
$$

这就说明 Lorentz 变换不是随便挑出来的形式，而是由“完整时空间隔不变”强制推出的形式。原文还补充说，如果只要求 $d\tau=0$ 的光锥保持不变，会得到更大的 [[共形变换|conformal group]]；但自然界有有质量粒子，它们的世界线满足 $d\tau^2>0$，所以只保持光锥不够，必须保持整个 $d\tau^2$。见 [[共形群为何不能作为自然界基本不变性|共形群为何不能作为自然界基本不变性]]。

接下来原文开始给 Lorentz 变换分类。包含平移 $a^\alpha$ 的全体变换叫 [[Lorentz变换与Poincare变换|Poincare 群]]，也叫非齐次 Lorentz 群；如果 $a^\alpha=0$，只剩线性部分，就叫齐次 Lorentz 群。

Lorentz 群还有不同分支。由 Lorentz 条件取 $\gamma=\delta=0$，可以推出 [[式2.1.10的推导|式 (2.1.10) 的推导]]

$$
(\Lambda^0{}_0)^2
=
1+\sum_i(\Lambda^i{}_0)^2
\ge 1
\tag{2.1.10}
$$

所以 $\Lambda^0{}_0$ 要么 $\ge 1$，要么 $\le -1$。同时由 $\Lambda^T\eta\Lambda=\eta$ 取行列式，可以得到 [[式2.1.11的推导|式 (2.1.11) 的推导]]

$$
(\det\Lambda)^2=1
\tag{2.1.11}
$$

所以 $\det\Lambda=\pm1$。与 [[Kronecker delta与单位变换|单位变换]] 连续相连的那一支必须满足

$$
\Lambda^0{}_0\ge 1,
\qquad
\det\Lambda=1
\tag{2.1.9}
$$

这就是原文所谓的 [[Lorentz变换分支与正Lorentz变换|正 Lorentz 变换]]。它排除了空间反射和时间反演。后文默认研究的就是这一类。

最后，原文讨论 Lorentz 变换中真正区别于 Galileo 变换的部分。空间转动当然属于 Lorentz 群：

$$
\Lambda^i{}_j=R_{ij},
\qquad
\Lambda^i{}_0=\Lambda^0{}_i=0,
\qquad
\Lambda^0{}_0=1
$$

如果只看转动和平移，Lorentz 群和 Galileo 群没有本质区别。真正新的部分是 boost，也就是改变惯性系相对速度的变换。

为了推出 boost，原文考虑一个粒子。观察者 $O$ 看它静止，所以 $dx^i=0$；观察者 $O'$ 看它以速度 $\mathbf v$ 运动。由

$$
dx'^\alpha=\Lambda^\alpha{}_\beta dx^\beta
\tag{2.1.12}
$$

因为原来只有 $dt$ 不为零，所以

$$
dx'^i=\Lambda^i{}_0dt
\tag{2.1.13}
$$

并且

$$
dt'=\Lambda^0{}_0dt
\tag{2.1.14}
$$

于是

$$
v_i
=
\frac{dx'^i}{dt'}
=
\frac{\Lambda^i{}_0}{\Lambda^0{}_0}
$$

也就是

$$
\Lambda^i{}_0
=
v_i\Lambda^0{}_0
\tag{2.1.15}
$$

再用 Lorentz 条件的 $(0,0)$ 分量：

$$
-1
=
\sum_i(\Lambda^i{}_0)^2-(\Lambda^0{}_0)^2
\tag{2.1.16}
$$

把 $\Lambda^i{}_0=v_i\Lambda^0{}_0$ 代入：

$$
-1
=
v^2(\Lambda^0{}_0)^2-(\Lambda^0{}_0)^2
=
-(1-v^2)(\Lambda^0{}_0)^2
$$

因此

$$
\Lambda^0{}_0
=
(1-v^2)^{-1/2}
=
\gamma
\tag{2.1.17}
$$

并且

$$
\Lambda^i{}_0=\gamma v_i
\tag{2.1.18}
$$

其中

$$
\gamma=(1-\mathbf v^2)^{-1/2}
\tag{2.1.19}
$$

这就是 Lorentz 因子在原文中的来源：它不是经验上补进去的修正，而是从“boost 必须保持 $d\tau^2$”推出的。

不过这些分量还没有完全确定整个 $\Lambda$，因为还可以额外接一个空间转动。Weinberg 给出一个方便的标准选择：

$$
\Lambda^i{}_j
=
\delta_{ij}
+
v_i v_j\frac{\gamma-1}{v^2}
\tag{2.1.20}
$$

关于这个标准 boost 空间部分为什么这样写，以及它如何表示沿 $\mathbf v$ 方向的投影，见 [[Explanations/标准boost空间部分的意义|标准boost空间部分的意义]]。

$$
\Lambda^0{}_j=\gamma v_j
\tag{2.1.21}
$$

这个标准 boost 可以理解为：垂直于 $\mathbf v$ 的方向不发生额外变化，沿 $\mathbf v$ 的方向与时间发生混合。最后原文指出，任意正齐次 Lorentz 变换都可以写成一个 boost 和一个 rotation 的乘积。

所以 2.1 的完整逻辑是：为了解决 Galileo 变换不适合电磁学的问题，Weinberg 引入保持固有时间隔 $d\tau^2=dt^2-d\mathbf{x}^2$ 的变换；这个要求给出 Lorentz 条件 $\Lambda^T\eta\Lambda=\eta$；进一步证明表明，保持完整间隔的非奇异变换只能是 Lorentz 变换加平移；这些变换组成 Poincare 群，其中与单位元连续相连的是正 Lorentz 群；最后，正 Lorentz 群中新出现的物理内容是 boost，而 boost 的系数 $\gamma=(1-v^2)^{-1/2}$ 由间隔不变性直接推出。
