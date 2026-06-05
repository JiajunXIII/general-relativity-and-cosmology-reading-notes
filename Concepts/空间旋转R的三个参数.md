---
title: 空间旋转R的三个参数
tags:
  - concept
  - classical-mechanics
aliases:
  - 空间旋转R
  - 旋转矩阵R
  - rotation matrix R
---

## 原文片段

> 这里 $R$ 是空间旋转，$\boldsymbol v$ 是匀速相对运动，$\boldsymbol d$ 是空间平移，$\tau$ 是时间平移。

## 我在对话中提出的问题

我要求：详细说明空间旋转 $R$ 的参量。

## 已给出的解答

$R$ 是三维旋转矩阵。它表面上有 $9$ 个矩阵分量，但旋转必须保持长度和角度，因此满足

$$
R^TR=I.
$$

这个正交条件给出 $6$ 个独立约束，所以自由参数数目是

$$
9-6=3.
$$

这 $3$ 个参数可以用 Euler angles 表示，也可以用“旋转轴方向的 $2$ 个参数 + 绕该轴旋转角度的 $1$ 个参数”表示。

## 简明解释

在 Galileo 变换中，$R$ 只允许是常量旋转。它表示两个惯性系坐标轴的固定夹角。如果 $R$ 变成 $R(t)$，就进入旋转参考系，会出现离心力和 Coriolis 力，Newton 方程不再保持原来的简单形式。

## 相关概念

- [[Explanations/Galileo变换的10个参数与Newton方程形式不变]]
- [[Concepts/向量记号与boldsymbol]]

## 来源阅读笔记

- [[广义相对论与宇宙学-section-1.3-相对性原理的历史]]
