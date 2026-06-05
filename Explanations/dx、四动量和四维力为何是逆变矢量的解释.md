---
title: dx、四动量和四维力为何是逆变矢量的解释
tags:
  - explanation
  - relativity/tensor
  - weinberg
---

# dx、四动量和四维力为何是逆变矢量的解释

## 原文片段

> 我们已经为诸如 $dx^\alpha$ 或 $f^\alpha$ 或 $p^\alpha$ 这些量引进了“四维矢量”这个术语。

## 我在对话中提出的问题

我问：“同向变换”是什么意思？这些 $dx^\alpha$、$p^\alpha$、$f^\alpha$ 也是采用上指标形式吗，也就是逆变矢量吗？

## 已经给出的解答

“同向变换”更准确地说，是指这些量的分量按照和坐标 $x^\alpha$ 相同的 Lorentz 变换矩阵变换。坐标满足

$$
x'^\alpha=\Lambda^\alpha{}_\beta x^\beta .
$$

如果某个量 $V^\alpha$ 也满足

$$
V'^\alpha=\Lambda^\alpha{}_\beta V^\beta ,
$$

那么它就是逆变矢量。

对 $dx^\alpha$，由

$$
x'^\alpha=\Lambda^\alpha{}_\beta x^\beta
$$

取微分得到

$$
dx'^\alpha=\Lambda^\alpha{}_\beta dx^\beta .
$$

所以 $dx^\alpha$ 是逆变四维矢量。

四动量定义为

$$
p^\alpha=m\frac{dx^\alpha}{d\tau}.
$$

其中 $m$ 是标量，$d\tau$ 是 Lorentz 不变量，所以 $p^\alpha$ 与 $dx^\alpha$ 按同样方式变换：

$$
p'^\alpha=\Lambda^\alpha{}_\beta p^\beta .
$$

四维力定义为

$$
f^\alpha=\frac{dp^\alpha}{d\tau}.
$$

因此

$$
f'^\alpha=\Lambda^\alpha{}_\beta f^\beta .
$$

所以 $dx^\alpha$、$p^\alpha$、$f^\alpha$ 在本节中都是上指标形式，也就是逆变四维矢量。

## 简明解释

上指标不是装饰，而是变换律的标记。$dx^\alpha$、$p^\alpha$、$f^\alpha$ 都按 $\Lambda^\alpha{}_\beta$ 变换，因此它们是逆变矢量。对应的下指标形式要通过 Minkowski 度规降低指标得到，例如 $p_\alpha=\eta_{\alpha\beta}p^\beta$。

## 相关概念

- [[协变矢量与逆变矢量]]
- [[四动量]]
- [[四维力]]
- [[Minkowski度规的指标形式]]

## 来源阅读笔记链接

- [[广义相对论与宇宙学-section-2.5-矢量和张量]]
