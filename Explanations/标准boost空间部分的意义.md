---
title: 标准boost空间部分的意义
tags:
  - explanation
  - relativity/special-relativity
  - weinberg
---

# 标准boost空间部分的意义

## 原文片段

> Weinberg 给出标准 boost 的空间部分：
>
> $$
> \Lambda^i{}_j
> =
> \delta_{ij}
> +
> v_iv_j\frac{\gamma-1}{v^2}.
> \tag{2.1.20}
> $$

## 我在对话中提出的问题

我问：section 2.1 中为什么要给出这个式子？有什么作用与意义吗？

## 已给出的解答

这个式子给出一个“纯 boost”的标准代表，也就是只改变参考系速度、不额外旋转空间坐标的 Lorentz transformation。

在 2.1 前面，Weinberg 已经得到

$$
\Lambda^0{}_0=\gamma,\qquad
\Lambda^i{}_0=\gamma v_i,\qquad
\Lambda^0{}_j=\gamma v_j.
$$

但这些还没有完全确定整个矩阵，因为还需要知道空间坐标之间如何变换，即 $\Lambda^i{}_j$。式 (2.1.20) 正是在回答：当参考系以任意方向 $\boldsymbol v$ 相对运动时，空间部分怎样变换，才能构成一个无额外旋转的标准 Lorentz boost。

## 简明解释

矩阵

$$
\frac{v_iv_j}{v^2}
$$

是沿 $\boldsymbol v$ 方向的投影算符。对任意空间向量 $\boldsymbol A$，

$$
\left(\frac{v_iv_j}{v^2}\right)A^j
=
v_i\frac{\boldsymbol v\cdot\boldsymbol A}{v^2}
=
A_\parallel^i.
$$

因此

$$
\delta_{ij}+(\gamma-1)\frac{v_iv_j}{v^2}
$$

对垂直于 $\boldsymbol v$ 的分量作用为 $1$，对平行于 $\boldsymbol v$ 的分量作用为 $\gamma$。它的几何意义是：

$$
\boldsymbol A_\perp+\boldsymbol A_\parallel
\longmapsto
\boldsymbol A_\perp+\gamma\boldsymbol A_\parallel.
$$

它在 2.3 中的直接作用，是让我们能够从瞬时静止系的普通力 $\boldsymbol F$ 推出四维力空间分量。

## 相关概念

- [[Lorentz变换与Poincare变换]]
- [[Kronecker delta与单位变换]]
- [[四维力]]
- [[Explanations/式2.3.5的推导]]

## 来源阅读笔记链接

- [[广义相对论与宇宙学-section-2.1-Lorentz变换]]
