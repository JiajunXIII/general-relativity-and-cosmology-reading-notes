---
tags:
  - reading-note/concept
  - mathematics/differential-geometry
source: "[[广义相对论与宇宙学-section-2.1-Lorentz变换]]"
---

# Jacobian矩阵

## 原文片段

> 一个一般的坐标变换 $x\to x'$ 将把 $d\tau$ 变成 $d\tau'$，其中出现矩阵 $\partial x'^\alpha/\partial x^\beta$。

## 我在对话中提出的问题

我问：为什么说它还可能随位置变化，以及为什么还要继续约束它？

## 已给出的解答

一般坐标变换

$$
x'^\alpha=x'^\alpha(x)
$$

不一定是线性的。它的局部线性近似由 Jacobian 给出：

$$
J^\alpha{}_\gamma(x)
=
\frac{\partial x'^\alpha}{\partial x^\gamma}.
$$

若变换是线性的，

$$
x'^\alpha=\Lambda^\alpha{}_\beta x^\beta+a^\alpha,
$$

则

$$
\frac{\partial x'^\alpha}{\partial x^\gamma}
=
\Lambda^\alpha{}_\gamma
$$

是常数。但非线性函数的导数通常依赖位置，例如一维中 $x'=x^2$ 有

$$
\frac{dx'}{dx}=2x.
$$

## 简明解释

Jacobian 是坐标变换在某一点的局部线性部分。式 (2.1.7) 只说明每一点的 Jacobian 都保持 Minkowski metric，但还没有说明不同点的 Jacobian 是否相同。Weinberg 接着约束它，就是为了证明这个 Jacobian 不能随位置变化，最终变换只能是线性加平移。

## 相关概念

- [[非奇异坐标变换]]
- [[Jacobian为何还可能随位置变化]]
- [[式2.1.7的推导]]

## 来源阅读笔记

- [[广义相对论与宇宙学-section-2.1-Lorentz变换]]
