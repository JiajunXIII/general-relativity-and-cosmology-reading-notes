---
title: Galileo变换的10个参数与Newton方程形式不变
tags:
  - explanation
  - classical-mechanics
aliases:
  - Galileo变换的10个参数
  - Newton方程形式不变
---

## 原文片段

> 这个变换有 10 个参数：3 个旋转，3 个速度，3 个空间平移，1 个时间平移。Newton 方程在这些变换下保持同样形式，这就是 Galileo 不变性，也就是 Newton 力学中的相对性原理。

## 我在对话中提出的问题

我问：为什么是 10 个参数？什么叫保持同样的形式？Newton 方程指的是什么？

## 已给出的解答

Galileo 变换为

$$
\boldsymbol x'=R\boldsymbol x+\boldsymbol v t+\boldsymbol d,
$$

$$
t'=t+\tau.
$$

$R$ 是三维旋转，有 $3$ 个参数；$\boldsymbol v$ 是相对速度，有 $3$ 个分量；$\boldsymbol d$ 是空间平移，有 $3$ 个分量；$\tau$ 是时间平移，有 $1$ 个参数。因此总共有

$$
3+3+3+1=10
$$

个参数。

这里的 Newton 方程主要指教材中的 Newton 引力 $N$-body 方程：

$$
m_N\frac{d^2\boldsymbol x_N}{dt^2}
=
G\sum_M
\frac{m_Nm_M(\boldsymbol x_M-\boldsymbol x_N)}{|\boldsymbol x_M-\boldsymbol x_N|^3}.
$$

“保持同样形式”指换到带撇坐标后，方程仍能写成同样结构，只是把 $\boldsymbol x$ 换成 $\boldsymbol x'$、把 $t$ 换成 $t'$。

## 简明解释

Galileo 变换允许惯性系之间有固定旋转、匀速相对运动、空间原点平移和时间原点平移。Newton 方程在这些变换下不改变结构，所以这些参考系同等有效。若进入加速系或旋转系，就会出现额外惯性力，方程形式不再相同。

## 相关概念

- [[Concepts/空间旋转R的三个参数]]
- [[Concepts/向量记号与boldsymbol]]

## 来源阅读笔记

- [[广义相对论与宇宙学-section-1.3-相对性原理的历史]]
