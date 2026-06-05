---
tags:
  - reading-note/concept
  - linear-algebra
  - relativity/lorentz
source: "[[广义相对论与宇宙学-section-2.1-Lorentz变换]]"
---

# Kronecker delta与单位变换

## 原文片段

> 任何 $\Lambda^\alpha{}_\beta$ 只要可以通过其参数的连续变化而变到单位元素 $\delta^\alpha{}_\beta$，则必是正 Lorentz 变换。

## 我在对话中提出的问题

我问：什么叫单位元素 $\delta^\alpha{}_\beta$，以及单位变换？

## 已给出的解答

Kronecker delta 定义为

$$
\delta^\alpha{}_\beta
=
\begin{cases}
1, & \alpha=\beta,\\
0, & \alpha\ne \beta.
\end{cases}
$$

它就是四维空间里的单位矩阵。它不是 $\eta_{\alpha\beta}$；$\eta$ 是 Minkowski metric，而 $\delta^\alpha{}_\beta$ 是

$$
\mathrm{diag}(1,1,1,1).
$$

它的作用是保持坐标不变：

$$
\delta^\alpha{}_\beta x^\beta=x^\alpha.
$$

单位变换就是

$$
x'^\alpha=x^\alpha,
$$

也就是

$$
\Lambda^\alpha{}_\beta=\delta^\alpha{}_\beta,
\qquad
a^\alpha=0.
$$

## 简明解释

单位变换就是“不转动、不 boost、不平移、不反射、不改变时间方向”。原文说某个 Lorentz 变换能连续变到单位元素，就是说它和“什么都不做”的变换处在同一个连续分支。

## 相关概念

- [[Lorentz变换分支与正Lorentz变换]]
- [[Lorentz变换与Poincare变换]]
- [[Minkowski度规号差与eta00]]

## 来源阅读笔记

- [[广义相对论与宇宙学-section-2.1-Lorentz变换]]

## Section 2.5 补充：Kronecker delta 不负责升降指标

## 原文片段

> $$
> U'_\alpha V'^\alpha
> =
> \delta^\gamma{}_\beta U_\gamma V^\beta
> =
> U_\beta V^\beta .
> $$

## 我在对话中提出的问题

我问：混合指标的 $\delta$ 不会涉及逆变矢量与协变矢量的转换吗？

## 已经给出的解答

不会。$\delta^\gamma{}_\beta$ 是单位映射，只负责把指标原样传递：

$$
\delta^\gamma{}_\beta V^\beta=V^\gamma,
\qquad
\delta^\gamma{}_\beta U_\gamma=U_\beta .
$$

真正负责升降指标的是 Minkowski 度规：

$$
V_\alpha=\eta_{\alpha\beta}V^\beta,
\qquad
U^\alpha=\eta^{\alpha\beta}U_\beta .
$$

## 简明解释

Kronecker delta 保持指标类型不变；Minkowski 度规改变指标位置。不要把 $\delta^\alpha{}_\beta$ 误解成负责协变和逆变转换的对象。

## 相关概念

- [[Minkowski度规的指标形式]]
- [[协变矢量与逆变矢量]]
- [[张量缩并]]
- [[Explanations/Kronecker delta不负责升降指标的解释]]

## 来源阅读笔记链接

- [[广义相对论与宇宙学-section-2.5-矢量和张量]]
