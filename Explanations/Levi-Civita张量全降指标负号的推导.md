---
title: Levi-Civita张量全降指标负号的推导
tags:
  - explanation
  - derivation
  - tensor-analysis
---

# Levi-Civita张量全降指标负号的推导

## 原文片段

> 当下降了全部指标后就回到数值相同的量，但差一个负号：
>
> $$
> \varepsilon_{\alpha\beta\gamma\delta}
> =
> -\varepsilon^{\alpha\beta\gamma\delta}.
> $$

## 我在对话中提出的问题

我问：偶置换与奇置换是什么？为什么全降低到下指标后多一个负号？

## 已经给出的解答

偶置换和奇置换以 $0123$ 为基准。把 $0123$ 重新排列成 $\alpha\beta\gamma\delta$，若需要交换两个位置的次数是偶数次，就是偶置换；若需要交换奇数次，就是奇置换。

例如

$$
\varepsilon^{0123}=+1,
\qquad
\varepsilon^{1023}=-1.
$$

全降指标时使用

$$
\varepsilon_{\alpha\beta\gamma\delta}
=
\eta_{\alpha\mu}
\eta_{\beta\nu}
\eta_{\gamma\rho}
\eta_{\delta\sigma}
\varepsilon^{\mu\nu\rho\sigma}.
$$

看基本分量 $0123$：

$$
\varepsilon_{0123}
=
\eta_{00}\eta_{11}\eta_{22}\eta_{33}\varepsilon^{0123}.
$$

在 Weinberg 的 $(-+++)$ 约定下，

$$
\eta_{00}=-1,\qquad
\eta_{11}=\eta_{22}=\eta_{33}=1.
$$

因此

$$
\varepsilon_{0123}
=
(-1)(1)(1)(1)(+1)
=
-1.
$$

由于 Levi-Civita 张量完全反对称，其他非零分量都只是 $0123$ 的置换，所以整体关系为

$$
\varepsilon_{\alpha\beta\gamma\delta}
=
-\varepsilon^{\alpha\beta\gamma\delta}.
$$

## 简明解释

全降指标的负号来自度规，不来自置换。四个指标全部下降时，三个空间方向给 $+1$，一个时间方向给 $-1$，所以整体多出一个负号。

## 相关概念

- [[Levi-Civita张量]]
- [[Minkowski度规的指标形式]]
- [[张量缩并]]
- [[协变矢量与逆变矢量]]

## 来源阅读笔记链接

- [[广义相对论与宇宙学-section-2.5-矢量和张量]]
