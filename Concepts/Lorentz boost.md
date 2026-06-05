---
title: Lorentz boost
tags:
  - concept
  - relativity/special-relativity
  - weinberg
aliases:
  - boost
  - 洛伦兹boost
  - Lorentz推动
---

# Lorentz boost

## 原文片段

> 如果只看转动和平移，Lorentz 群和 Galileo 群没有本质区别。真正新的部分是 boost，也就是改变惯性系相对速度的变换。

## 我在对话中提出的问题

我问：“Lorentz boost 会混合时间和空间是什么意思？同时需要解释 Lorentz boost。”

## 已给出的解答

Lorentz transformation 包括空间平移、时间平移、空间旋转和 boost。其中 boost 指的是从一个惯性系切换到另一个相对它匀速运动的惯性系。

例如 $S'$ 相对 $S$ 沿 $x$ 方向以速度 $u$ 运动。取 $c=1$，一个常见约定下 Lorentz boost 是：

$$
t'=\gamma(t-u x),
$$

$$
x'=\gamma(x-u t),
$$

$$
y'=y,\qquad z'=z,
$$

其中

$$
\gamma=\frac{1}{\sqrt{1-u^2}}.
$$

这和 Galilean transformation 不同。Galilean 变换是

$$
t'=t,\qquad x'=x-ut.
$$

Newton 力学里时间不变，只有空间坐标变；Lorentz boost 中，$t'$ 里含有旧的空间坐标 $x$，$x'$ 里含有旧的时间坐标 $t$。这就是时间和空间被混合。

## 简明解释

Lorentz boost 是改变惯性系相对速度的 Lorentz transformation。它不是普通空间旋转，而是 spacetime 中的 hyperbolic rotation。它会把原参考系的时间和运动方向上的空间坐标混在一起，因此也会把四动量的能量分量和动量分量混在一起。

## 相关概念

- [[Lorentz变换与Poincare变换]]
- [[四动量]]
- [[Explanations/标准boost空间部分的意义]]
- [[Explanations/Lorentz boost混合能量和动量的含义]]

## 来源阅读笔记链接

- [[广义相对论与宇宙学-section-2.1-Lorentz变换]]
- [[广义相对论与宇宙学-section-2.4-能量和动量]]
