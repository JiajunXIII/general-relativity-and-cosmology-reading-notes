---
tags:
  - reading-note/explanation
  - mathematics/differential-geometry
source: "[[广义相对论与宇宙学-section-2.1-Lorentz变换]]"
---

# Jacobian为何还可能随位置变化

## 原文片段

> 这个式子的意思是：这个一般变换的 Jacobian 在每一点都像 Lorentz 矩阵一样保持 $\eta$。但它还可能随位置变化，所以还要继续约束它。

## 我在对话中提出的问题

我问：为什么说它还可能随位置变化，以及为什么还要约束它？

## 已给出的解答

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

是常数。但一般变换

$$
x'^\alpha=x'^\alpha(x)
$$

可以是非线性的。非线性函数的导数通常依赖位置，例如

$$
x'=x^2
$$

有

$$
\frac{dx'}{dx}=2x.
$$

因此式 (2.1.7) 只说明每个点上的 Jacobian 都保持 $\eta$，还没有说明不同点上的 Jacobian 是否是同一个矩阵。Weinberg 继续约束它，是为了证明位置依赖不允许存在，最终推出变换只能是线性加平移。

## 简明解释

式 (2.1.7) 是局部条件。要得到全局的 Lorentz 变换形式，还要证明 Jacobian 不能随 $x$ 改变。

## 相关概念

- [[Jacobian矩阵]]
- [[从式2.1.7到二阶导数约束]]
- [[非奇异坐标变换]]

## 来源阅读笔记

- [[广义相对论与宇宙学-section-2.1-Lorentz变换]]
