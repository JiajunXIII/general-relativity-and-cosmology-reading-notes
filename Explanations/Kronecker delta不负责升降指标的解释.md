---
title: Kronecker delta不负责升降指标的解释
tags:
  - explanation
  - tensor-analysis
  - index-notation
---

# Kronecker delta不负责升降指标的解释

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

不会。混合指标的 Kronecker delta

$$
\delta^\gamma{}_\beta
$$

本身不负责把逆变矢量变成协变矢量，也不负责把协变矢量变成逆变矢量。它只是单位映射，用来原样传递指标。

真正负责升降指标的是度规：

$$
V_\alpha=\eta_{\alpha\beta}V^\beta,
\qquad
U^\alpha=\eta^{\alpha\beta}U_\beta .
$$

Kronecker delta 的作用是

$$
\delta^\gamma{}_\beta V^\beta=V^\gamma .
$$

这里 $V^\beta$ 仍然是逆变矢量，只是指标名字从 $\beta$ 变成 $\gamma$。同理，

$$
\delta^\gamma{}_\beta U_\gamma=U_\beta .
$$

这里 $U_\gamma$ 仍然是协变矢量，只是指标名字从 $\gamma$ 变成 $\beta$。

## 简明解释

$\eta_{\alpha\beta}$ 和 $\eta^{\alpha\beta}$ 负责升降指标；$\delta^\alpha{}_\beta$ 只负责保持指标类型不变并传递分量。因此 $\delta^\gamma{}_\beta U_\gamma V^\beta=U_\beta V^\beta$ 没有发生协变与逆变之间的转换。

## 相关概念

- [[Kronecker delta与单位变换]]
- [[Minkowski度规的指标形式]]
- [[协变矢量与逆变矢量]]
- [[张量缩并]]

## 来源阅读笔记链接

- [[广义相对论与宇宙学-section-2.5-矢量和张量]]
