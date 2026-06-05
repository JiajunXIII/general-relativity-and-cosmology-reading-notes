---
tags:
  - reading-note/concept
  - relativity/metric
source: "[[广义相对论与宇宙学-section-2.1-Lorentz变换]]"
---

# Minkowski度规号差与eta00

## 原文片段

> $\eta_{\alpha\beta}=\mathrm{diag}(1,1,1,-1)$，并且 $d\tau^2=dt^2-d\mathbf{x}^2=-\eta_{\alpha\beta}dx^\alpha dx^\beta$。

## 我在对话中提出的问题

我问：$\eta_{\alpha\beta}=\mathrm{diag}(1,1,1,-1)$，0 行 0 列不是 1 吗？为什么为了让 $d\tau^2=dt^2-d\mathbf{x}^2=-\eta_{\alpha\beta}dx^\alpha dx^\beta$ 成立，必须有 $\eta_{00}=-1$？

## 已给出的解答

Weinberg 的指标顺序是

$$
(1,2,3,0),
$$

不是常见的

$$
(0,1,2,3).
$$

所以按 Weinberg 的顺序写成矩阵，

$$
\eta_{\alpha\beta}
=
\mathrm{diag}(1,1,1,-1),
$$

最后一个 $-1$ 才对应时间指标 $0$，即

$$
\eta_{00}=-1.
$$

展开

$$
-\eta_{\alpha\beta}dx^\alpha dx^\beta
=
-\left[
\eta_{11}(dx^1)^2+
\eta_{22}(dx^2)^2+
\eta_{33}(dx^3)^2+
\eta_{00}dt^2
\right].
$$

为了得到

$$
dt^2-(dx^1)^2-(dx^2)^2-(dx^3)^2,
$$

必须有

$$
\eta_{11}=\eta_{22}=\eta_{33}=1,
\qquad
\eta_{00}=-1.
$$

## 简明解释

这里的混淆来自矩阵排列顺序。按 $(1,2,3,0)$ 排列时，$\mathrm{diag}(1,1,1,-1)$ 的最后一项是时间分量；按 $(0,1,2,3)$ 排列，同一度规会写成 $\mathrm{diag}(-1,1,1,1)$。

## 相关概念

- [[距离与度规]]
- [[式2.1.10的推导]]

## 来源阅读笔记

- [[广义相对论与宇宙学-section-2.1-Lorentz变换]]
