---
title: Gamma因子低速展开的推导
tags:
  - explanation
  - relativity/special-relativity
  - weinberg
---

# Gamma因子低速展开的推导

## 原文片段

> 在低速极限下，对 $\gamma$ 展开：
>
> $$
> \gamma = 1+\frac12 v^2+O(v^4).
> $$

## 我在对话中提出的问题

我问：“该展开式是如何做到的？是 Taylor 展开吗？”

## 已给出的解答

是的，本质上是 Taylor 展开，更准确地说是 binomial expansion。这里

$$
\gamma=(1-v^2)^{-1/2}.
$$

低速极限 $v\ll 1$ 的意思是 $v^2$ 很小。令

$$
x=v^2,
$$

问题变成展开

$$
(1-x)^{-1/2}
$$

在 $x=0$ 附近的 Taylor 展开：

$$
(1-x)^{-1/2}
=
1+\frac12x+\frac38x^2+\frac{5}{16}x^3+\cdots.
$$

把 $x=v^2$ 代回去：

$$
\gamma
=
1+\frac12v^2+\frac38v^4+\frac{5}{16}v^6+\cdots.
$$

所以只保留到 $v^2$ 阶时：

$$
\gamma=1+\frac12v^2+O(v^4).
$$

这里 $O(v^4)$ 的意思是：被省略的第一项从 $v^4$ 阶开始，例如 $\frac38v^4$。

对应能量：

$$
E=m\gamma
=
m\left(1+\frac12v^2+O(v^4)\right)
=
m+\frac12mv^2+O(v^4).
$$

## 简明解释

低速展开就是把 $\gamma$ 当作小参数 $v^2$ 的函数，在 $v=0$ 附近展开。因为 $\gamma$ 依赖的是 $v^2$ 而不是 $v$，所以修正项按 $v^2,v^4,v^6,\cdots$ 出现。

## 相关概念

- [[四动量]]
- [[Explanations/函数一减x的负二分之一次方Taylor展开的推导]]
- [[Explanations/自然单位c等于1时动能项的单位恢复]]

## 来源阅读笔记链接

- [[广义相对论与宇宙学-section-2.4-能量和动量]]
