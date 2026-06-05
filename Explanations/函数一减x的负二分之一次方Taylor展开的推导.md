---
title: 函数一减x的负二分之一次方Taylor展开的推导
tags:
  - explanation
  - mathematics/taylor-expansion
  - relativity/special-relativity
  - weinberg
aliases:
  - (1-x)^(-1/2)的Taylor展开
---

# 函数一减x的负二分之一次方Taylor展开的推导

## 原文片段

> 对 $\gamma=(1-v^2)^{-1/2}$ 做低速展开，需要展开函数：
>
> $$
> (1-x)^{-1/2}.
> $$

## 我在对话中提出的问题

我问：“$(1-x)^{-1/2}$ 是如何 Taylor 展开的？使用了什么公式？”

## 已给出的解答

使用的是 Maclaurin 展开，也就是在 $x=0$ 处的 Taylor 展开。通用公式是：

$$
f(x)=f(0)+f'(0)x+\frac{f''(0)}{2!}x^2+\frac{f^{(3)}(0)}{3!}x^3+\cdots.
$$

这里取

$$
f(x)=(1-x)^{-1/2}.
$$

逐项求导：

$$
f(0)=1.
$$

一阶导数为

$$
f'(x)=\frac12(1-x)^{-3/2},
$$

所以

$$
f'(0)=\frac12.
$$

二阶导数为

$$
f''(x)=\frac12\cdot\frac32(1-x)^{-5/2}
=\frac34(1-x)^{-5/2},
$$

所以

$$
\frac{f''(0)}{2!}
=
\frac{3/4}{2}
=
\frac38.
$$

三阶导数为

$$
f^{(3)}(x)
=
\frac12\cdot\frac32\cdot\frac52(1-x)^{-7/2}
=
\frac{15}{8}(1-x)^{-7/2},
$$

所以

$$
\frac{f^{(3)}(0)}{3!}
=
\frac{15/8}{6}
=
\frac{5}{16}.
$$

因此

$$
(1-x)^{-1/2}
=
1+\frac12 x+\frac38 x^2+\frac{5}{16}x^3+\cdots.
$$

也可以用 generalized binomial theorem：

$$
(1+u)^a
=
\sum_{n=0}^{\infty}\binom{a}{n}u^n,
$$

其中

$$
\binom{a}{n}
=
\frac{a(a-1)(a-2)\cdots(a-n+1)}{n!}.
$$

令

$$
a=-\frac12,\qquad u=-x,
$$

就得到

$$
(1-x)^{-1/2}
=
1+\frac12x+\frac38x^2+\frac{5}{16}x^3+\cdots.
$$

## 简明解释

这个展开是普通 Taylor 展开在 $x=0$ 附近的应用，也可以看成 generalized binomial theorem 的特例。相对论里令 $x=v^2$，所以 $\gamma$ 的低速展开自动变成关于 $v^2$ 的级数。

## 相关概念

- [[Explanations/Gamma因子低速展开的推导]]
- [[四动量]]

## 来源阅读笔记链接

- [[广义相对论与宇宙学-section-2.4-能量和动量]]
