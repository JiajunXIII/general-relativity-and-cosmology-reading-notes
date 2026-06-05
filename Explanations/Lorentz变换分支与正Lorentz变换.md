---
tags:
  - reading-note/explanation
  - relativity/lorentz
source: "[[广义相对论与宇宙学-section-2.1-Lorentz变换]]"
---

# Lorentz变换分支与正Lorentz变换

## 原文片段

> 任何 $\Lambda^\alpha{}_\beta$ 只要可以通过其参数的连续变化而变到单位元素 $\delta^\alpha{}_\beta$，则必是正 Lorentz 变换，因为通过参数的连续变化不可能由 $\Lambda^0{}_0\le -1$ 跳到 $\Lambda^0{}_0\ge +1$，或者由 $\det\Lambda=-1$ 跳到 $\det\Lambda=+1$。

## 我在对话中提出的问题

我问：如何理解原文这段话？

## 已给出的解答

Lorentz 条件给出两个离散结论：

$$
\Lambda^0{}_0\ge 1
\quad\text{或者}\quad
\Lambda^0{}_0\le -1,
$$

以及

$$
\det\Lambda=+1
\quad\text{或者}\quad
\det\Lambda=-1.
$$

单位变换满足

$$
\Lambda^0{}_0=+1,
\qquad
\det\Lambda=+1.
$$

如果从单位变换连续调节参数，矩阵元素不能突然跳变。$\Lambda^0{}_0$ 不可能从 $\ge 1$ 的分支连续跳到 $\le -1$ 的分支，因为中间必须经过 $-1$ 和 $1$ 之间，而 Lorentz 条件禁止。$\det\Lambda$ 也不能从 $+1$ 连续跳到 $-1$，因为中间要经过 $0$，但 Lorentz 变换必须可逆。

所以能连续变回单位变换的 Lorentz 变换一定满足

$$
\Lambda^0{}_0\ge 1,
\qquad
\det\Lambda=1.
$$

这就是正 Lorentz 变换。

## 简明解释

Lorentz 群被 Lorentz 条件分成互相隔开的几块。与单位元同一块的是保持时间方向和空间取向的那一块；Weinberg 后文默认只研究这块。

## 相关概念

- [[Kronecker delta与单位变换]]
- [[式2.1.10的推导]]
- [[式2.1.11的推导]]
- [[Lorentz变换与Poincare变换]]

## 来源阅读笔记

- [[广义相对论与宇宙学-section-2.1-Lorentz变换]]
