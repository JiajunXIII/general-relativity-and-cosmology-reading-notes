---
title: Levi-Civita张量
tags:
  - concept
  - tensor-analysis
  - orientation
aliases:
  - Levi-Civita tensor
  - epsilon tensor
  - Levi-Civita符号
---

# Levi-Civita张量

## 原文片段

> Levi-Civita 张量是由下式定义的量 $\varepsilon^{\alpha\beta\gamma\delta}$：
>
> $$
> \varepsilon^{\alpha\beta\gamma\delta}
> =
> \begin{cases}
> +1, & \alpha\beta\gamma\delta \text{ 是 } 0123 \text{ 的偶置换},\\
> -1, & \alpha\beta\gamma\delta \text{ 是 } 0123 \text{ 的奇置换},\\
> 0, & \text{其它情形}.
> \end{cases}
> $$

## 我在对话中提出的问题

我问：偶置换与奇置换是什么？为什么全降低到下指标后多一个负号？

## 已经给出的解答

以标准顺序 $0123$ 为基准。把 $0123$ 重新排列成 $\alpha\beta\gamma\delta$，如果需要交换两个位置的次数是偶数次，就叫偶置换；如果需要交换奇数次，就叫奇置换。例如 $0123$ 本身是偶置换，所以

$$
\varepsilon^{0123}=+1.
$$

交换一次得到 $1023$，所以

$$
\varepsilon^{1023}=-1.
$$

如果有重复指标，例如 $\varepsilon^{0113}$，它不是 $0,1,2,3$ 的排列，所以为零。

全降指标时，

$$
\varepsilon_{\alpha\beta\gamma\delta}
=
\eta_{\alpha\mu}\eta_{\beta\nu}\eta_{\gamma\rho}\eta_{\delta\sigma}
\varepsilon^{\mu\nu\rho\sigma}.
$$

在 $(-+++)$ 约定下，

$$
\eta_{00}=-1,\qquad \eta_{11}=\eta_{22}=\eta_{33}=1.
$$

所以

$$
\varepsilon_{0123}
=
\eta_{00}\eta_{11}\eta_{22}\eta_{33}\varepsilon^{0123}
=
(-1)(1)(1)(1)(+1)
=
-1.
$$

因此

$$
\varepsilon_{\alpha\beta\gamma\delta}
=
-\varepsilon^{\alpha\beta\gamma\delta}.
$$

## 简明解释

Levi-Civita 张量记录四个指标排列的取向。偶置换给 $+1$，奇置换给 $-1$，重复指标给 $0$。全降指标多出的负号来自 Minkowski 度规的时间方向负号，而不是来自置换本身。

## 相关概念

- [[Minkowski度规的指标形式]]
- [[张量缩并]]
- [[哑指标与自由指标]]
- [[Explanations/Levi-Civita张量全降指标负号的推导]]

## 来源阅读笔记链接

- [[广义相对论与宇宙学-section-2.5-矢量和张量]]
