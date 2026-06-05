---
title: 广义相对论与宇宙学 section 2.5 矢量和张量
tags:
  - reading-note
  - relativity/special-relativity
  - tensor-analysis
  - weinberg
source_markdown: "E:\\JiajunX\\PycharmProjects\\Physics_for_Intelligence\\temp\\teacher-pdf-reader\\weinberg_section_2_5_only_mineru.md"
---

# 广义相对论与宇宙学 section 2.5 矢量和张量

本节的目的不是单纯介绍新符号，而是给后面的电动力学、相对论流体力学和广义相对论张量分析建立一套“看指标就知道 Lorentz 变换性质”的语言。上一节已经把四维位移、四维力、四动量写成 $dx^\alpha$、$f^\alpha$、$p^\alpha$。自然的问题是：这些上指标到底意味着什么？为什么有些量应该写成上指标，有些量必须写成下指标？

本节的主线可以概括为：先区分 [[Concepts/协变矢量与逆变矢量|逆变矢量与协变矢量]]，再用 [[Concepts/Minkowski度规的指标形式|Minkowski 度规的指标形式]] 升降指标，接着说明哪些缩并会给出 Lorentz 不变量，最后把这一套推广到一般张量。

## 逆变矢量与协变矢量

坐标的 Lorentz 变换为

$$
x'^\alpha=\Lambda^\alpha{}_\beta x^\beta .
$$

如果某个量 $V^\alpha$ 的分量也按同样的矩阵变换，

$$
V'^\alpha=\Lambda^\alpha{}_\beta V^\beta ,
$$

那么它叫逆变矢量。这里“同样”不是说空间方向相同，而是说变换律同型。$dx^\alpha$、$p^\alpha$、$f^\alpha$ 在本节中都采用上指标形式，属于逆变四维矢量。这个问题的详细说明见 [[Explanations/dx、四动量和四维力为何是逆变矢量的解释|dx、四动量和四维力为何是逆变矢量的解释]]。

另一类量写成下指标，例如 $U_\alpha$，它满足

$$
U'_\alpha=\Lambda_\alpha{}^\beta U_\beta .
$$

这就是协变矢量。注意上式不能和逆变矢量的变换律混写：逆变矢量用 $\Lambda^\alpha{}_\beta$，协变矢量用 $\Lambda_\alpha{}^\beta$。

## Minkowski 度规与指标升降

本书在本节使用的 Minkowski 度规满足时间方向为负、空间方向为正。如果按常见顺序 $(0,1,2,3)$ 写，就是

$$
\eta_{\alpha\beta}
=
\mathrm{diag}(-1,1,1,1).
$$

两个下指标的 $\eta_{\alpha\beta}$ 用来降指标：

$$
V_\alpha=\eta_{\alpha\beta}V^\beta .
$$

两个上指标的 $\eta^{\alpha\beta}$ 用来升指标：

$$
U^\alpha=\eta^{\alpha\beta}U_\beta .
$$

在 Minkowski 正交惯性坐标里，$\eta_{\alpha\beta}$ 和 $\eta^{\alpha\beta}$ 的矩阵数值刚好相同，但它们的张量角色不同。混合指标形式满足

$$
\eta^\alpha{}_\beta
=
\eta^{\alpha\gamma}\eta_{\gamma\beta}
=
\delta^\alpha{}_\beta .
$$

所以 $\eta^\alpha{}_\beta$ 实际上是单位张量，不会产生时间分量的负号。真正负责升降指标的是 $\eta_{\alpha\beta}$ 与 $\eta^{\alpha\beta}$。这一点见 [[Concepts/Minkowski度规的指标形式|Minkowski 度规的指标形式]]。

## 为什么逆变和协变的缩并是不变量

协变矢量与逆变矢量的乘积

$$
U_\alpha V^\alpha
$$

是 Lorentz 不变量。因为

$$
U'_\alpha V'^\alpha
=
\Lambda_\alpha{}^\gamma U_\gamma
\Lambda^\alpha{}_\beta V^\beta .
$$

核心代数关系是

$$
\Lambda_\alpha{}^\gamma\Lambda^\alpha{}_\beta
=
\delta^\gamma{}_\beta .
$$

这个关系表达的是：$\Lambda_\alpha{}^\gamma$ 是 $\Lambda^\alpha{}_\beta$ 的逆变换矩阵，详细推导见 [[Explanations/Lambda逆矩阵关系的推导|Lambda 逆矩阵关系的推导]]。于是

$$
U'_\alpha V'^\alpha
=
\delta^\gamma{}_\beta U_\gamma V^\beta
=
U_\beta V^\beta .
$$

这里的 [[Concepts/Kronecker delta与单位变换|Kronecker delta]] 不负责把逆变矢量变成协变矢量，它只负责原样传递指标。这个细节见 [[Explanations/Kronecker delta不负责升降指标的解释|Kronecker delta 不负责升降指标的解释]]。

## 梯度是协变对象

不是所有带一个指标的东西都自然是逆变的。梯度

$$
\partial_\alpha
\equiv
\frac{\partial}{\partial x^\alpha}
$$

是协变对象。由链式法则，

$$
\frac{\partial}{\partial x'^\alpha}
=
\frac{\partial x^\beta}{\partial x'^\alpha}
\frac{\partial}{\partial x^\beta}
=
\Lambda_\alpha{}^\beta
\frac{\partial}{\partial x^\beta}.
$$

这正是协变矢量的变换形式。因此 $\partial_\alpha V^\alpha$ 是一上一下的缩并，是 Lorentz 不变量。

同理，达朗贝尔算符是

$$
\Box^2
=
\eta^{\alpha\beta}
\frac{\partial}{\partial x^\beta}
\frac{\partial}{\partial x^\alpha}
=
\nabla^2-\frac{\partial^2}{\partial t^2}.
$$

它是相对论时空中的波动算符，也可以写成

$$
\partial^\alpha\partial_\alpha
=
\Box^2 .
$$

概念解释见 [[Concepts/达朗贝尔算符|达朗贝尔算符]]，展开推导见 [[Explanations/达朗贝尔算符的推导|达朗贝尔算符的推导]]。

## 从矢量推广到张量

张量就是带若干个上指标和若干个下指标，并且每个指标都按自己的 Lorentz 变换规则变换的对象。例如

$$
T^\gamma{}_{\alpha\beta}
$$

有一个上指标 $\gamma$ 和两个下指标 $\alpha,\beta$，所以它的变换律为

$$
T'^\gamma{}_{\alpha\beta}
=
\Lambda^\gamma{}_\delta
\Lambda_\alpha{}^\varepsilon
\Lambda_\beta{}^\zeta
T^\delta{}_{\varepsilon\zeta}.
$$

规则非常机械：每个上指标配一个 $\Lambda$ 的上新下旧形式，每个下指标配一个 $\Lambda$ 的下新上旧形式。

由已有张量构造新张量有四种基本方式。第一是线性组合：只有指标结构相同的张量才能相加。第二是直积：两个张量的分量相乘，所有指标保留下来。第三是 [[Concepts/张量缩并|张量缩并]]：在同一个张量里选一对一上一下的指标，让它们同名并求和，结果少掉这两个指标。第四是微商：在齐次 Lorentz 变换下，普通偏导会给张量增加一个下指标。

## 特殊张量

第一类特殊张量是 Minkowski 度规。$\eta_{\alpha\beta}$ 是协变二阶张量，$\eta^{\alpha\beta}$ 是逆变二阶张量，二者可以升降任意张量指标。

第二类是 [[Concepts/Levi-Civita张量|Levi-Civita 张量]]。它由 $0123$ 的偶置换、奇置换和重复指标定义：

$$
\varepsilon^{\alpha\beta\gamma\delta}
=
\begin{cases}
+1, & \alpha\beta\gamma\delta \text{ 是 } 0123 \text{ 的偶置换},\\
-1, & \alpha\beta\gamma\delta \text{ 是 } 0123 \text{ 的奇置换},\\
0, & \text{有重复指标}.
\end{cases}
$$

在 $(-+++)$ 度规下，全降指标会多出一个负号：

$$
\varepsilon_{\alpha\beta\gamma\delta}
=
-\varepsilon^{\alpha\beta\gamma\delta}.
$$

这个负号不是置换造成的，而是 Minkowski 度规的时间方向分量为负。详细推导见 [[Explanations/Levi-Civita张量全降指标负号的推导|Levi-Civita 张量全降指标负号的推导]]。

第三类是零张量。只要一个张量的所有分量都是零，它在 Lorentz 变换下仍然为零。

## 本节核心判断标准

本节真正想给出的判断标准是：如果两个张量具有完全相同的指标结构，并且在一个参考系中相等，那么它们在任何 Lorentz 相关参考系中也相等。例如若

$$
T^\alpha{}_\beta=S^\alpha{}_\beta,
$$

则

$$
T'^\alpha{}_\beta
=
\Lambda^\alpha{}_\gamma
\Lambda_\beta{}^\delta
T^\gamma{}_\delta
=
\Lambda^\alpha{}_\gamma
\Lambda_\beta{}^\delta
S^\gamma{}_\delta
=
S'^\alpha{}_\beta .
$$

这就是张量记号的实际用途：只要方程两边是同类型张量，方程在一个 Lorentz 系中成立，就在所有 Lorentz 相关惯性系中成立。

## 常见误区

第一，把 $V^\alpha$ 和 $V_\alpha$ 当成同一组分量。它们可以表示同一几何对象的不同分量表示，但在 Minkowski 度规下时间分量会变号。

第二，把 $\Lambda^\alpha{}_\beta$ 和 $\Lambda_\alpha{}^\beta$ 混写。前者用于逆变矢量，后者用于协变矢量。

第三，以为 $\partial/\partial x^\alpha$ 因为出现了 $x^\alpha$ 就是上指标对象。实际上它作为 $\partial_\alpha$ 是协变对象。

第四，缩并必须是一上一下。两个上指标或两个下指标不能直接缩并，除非先用度规升降其中一个指标。

第五，忽略 Levi-Civita 张量全降指标时的负号。在 $(-+++)$ 约定下，$\varepsilon_{0123}=-1$，而 $\varepsilon^{0123}=+1$。

## 自检问题

1. 为什么 $dx^\alpha$、$p^\alpha$、$f^\alpha$ 都自然写成上指标？
2. $\eta_{\alpha\beta}$、$\eta^{\alpha\beta}$、$\eta^\alpha{}_\beta$ 分别起什么作用？
3. 为什么 $\Lambda_\alpha{}^\gamma\Lambda^\alpha{}_\beta=\delta^\gamma{}_\beta$？
4. 为什么 $\partial_\alpha$ 是协变对象？
5. 张量缩并为什么必须是一上一下？
6. 为什么在 $(-+++)$ 度规下 $\varepsilon_{\alpha\beta\gamma\delta}=-\varepsilon^{\alpha\beta\gamma\delta}$？
