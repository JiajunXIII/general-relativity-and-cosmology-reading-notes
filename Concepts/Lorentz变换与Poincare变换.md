---
tags:
  - reading-note/concept
  - relativity/lorentz
source: "[[广义相对论与宇宙学-section-2.1-Lorentz变换]]"
---

# Lorentz变换与Poincare变换

## 原文片段

> 形如 (2.1.1) 的所有 Lorentz 变换的集合称为非齐次 Lorentz 群，或 Poincare 群；而 $a^\alpha=0$ 的子集合称为齐次 Lorentz 群。

## 我在对话中提出的问题

我问：Lorentz 变换都是指这样的线性表达吗？

## 已给出的解答

在 Weinberg 2.1 的语境里，

$$
x'^\alpha=\Lambda^\alpha{}_\beta x^\beta+a^\alpha
$$

是非齐次 Lorentz 变换，也叫 Poincare 变换。其中 $\Lambda$ 满足

$$
\Lambda^\alpha{}_\gamma
\Lambda^\beta{}_\delta
\eta_{\alpha\beta}
=
\eta_{\gamma\delta}.
$$

若

$$
a^\alpha=0,
$$

则

$$
x'^\alpha=\Lambda^\alpha{}_\beta x^\beta
$$

叫齐次 Lorentz 变换。

## 简明解释

很多教材日常说 Lorentz 变换时，有时只指齐次部分 $\Lambda$，有时宽泛包含平移。Weinberg 这里明确区分：齐次 Lorentz 群没有平移；非齐次 Lorentz 群包含平移，也叫 Poincare 群。

## 相关概念

- [[Kronecker delta与单位变换]]
- [[Lorentz变换分支与正Lorentz变换]]
- [[共形变换]]

## 来源阅读笔记

- [[广义相对论与宇宙学-section-2.1-Lorentz变换]]
