---
title: Minkowski度规的指标形式
tags:
  - concept
  - relativity/metric
  - tensor-analysis
  - weinberg
aliases:
  - eta上下指标
  - Minkowski metric indexed forms
---

# Minkowski度规的指标形式

## 原文片段

> 这里引进的矩阵 $\eta^{\beta\delta}$ 在数值上与 $\eta_{\beta\delta}$ 相同，即
>
> $$
> \eta^{\beta\delta}\equiv \eta_{\beta\delta}.
> $$
>
> 把它写成上指标是为了适应我们的求和约定。

## 我在对话中提出的问题

我问：前几个 section 中的闵可夫斯基度规与 section 2.5 中的 $\eta_{\alpha\beta}$、$\eta^{\alpha\beta}$、$\eta^\alpha{}_\beta$ 有什么区别？

## 已经给出的解答

它们不是三个不同的物理度规，而是同一个 Minkowski 度规在不同指标位置下的三种张量形式。前几节主要把 $\eta_{\alpha\beta}$ 当作内积矩阵，用来写

$$
\eta_{\alpha\beta}x^\alpha x^\beta .
$$

到了 2.5 节，重点变成它在张量代数中的作用。两个下指标的 $\eta_{\alpha\beta}$ 是协变度规，用来降指标：

$$
V_\alpha=\eta_{\alpha\beta}V^\beta .
$$

两个上指标的 $\eta^{\alpha\beta}$ 是逆度规，用来升指标：

$$
U^\alpha=\eta^{\alpha\beta}U_\beta .
$$

混合形式满足

$$
\eta^\alpha{}_\beta
=
\eta^{\alpha\gamma}\eta_{\gamma\beta}
=
\delta^\alpha{}_\beta .
$$

所以它是单位张量，不会产生时间分量负号。

## 简明解释

在 Minkowski 正交惯性坐标中，$\eta_{\alpha\beta}$ 与 $\eta^{\alpha\beta}$ 的矩阵数值相同，但指标位置不同，功能也不同。$\eta_{\alpha\beta}$ 负责降指标，$\eta^{\alpha\beta}$ 负责升指标，$\eta^\alpha{}_\beta$ 等于 Kronecker delta，只是单位映射。

## 相关概念

- [[Minkowski度规号差与eta00]]
- [[协变矢量与逆变矢量]]
- [[Kronecker delta与单位变换]]
- [[张量缩并]]

## 来源阅读笔记链接

- [[广义相对论与宇宙学-section-2.5-矢量和张量]]
