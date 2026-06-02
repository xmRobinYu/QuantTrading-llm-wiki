---
title: 资料摘要：B站量化课 21 Matplotlib 绘制 KDJ
type: source
status: draft
tags: [教程, 基础, 量化交易, python]
aliases: []
created: 2026-06-02
updated: 2026-06-02
sources: []
domain: "量化交易"
confidence: medium
summary: "本讲围绕 KDJ 的超买超卖逻辑，讲解 `RSV/K/D/J` 的计算关系，并演示如何用 `pandas` 与 `matplotlib` 画出三线指标。"
source_url: https://www.bilibili.com/video/BV1D52CBREpX?p=21
media: video
raw_path: raw/量化交易/B站Python量化交易教程（BV1D52CBREpX）/21-21量化交易开发Matplotlib应用-股票技术分析实战_基于Mat.md
source_kind: file
fetched_at: 2026-06-02T00:03:31Z
---

> 本讲围绕 KDJ 的超买超卖逻辑，讲解 `RSV/K/D/J` 的计算关系，并演示如何用 `pandas` 与 `matplotlib` 画出三线指标。

## 核心要点

- KDJ 主要用于判断短期行情强弱以及超买、超卖区域，课程把 `80` 以上与 `30` 以下作为典型观察区间。
- 公式上先算 `RSV`，再递推出 `K`、`D`，最后得到 `J = 3K - 2D`；若前值缺失，则默认前一日 `K`、`D` 为 `50`。
- 实现时会用 `rolling` 求窗口内最高价和最低价，再配合平滑计算得到 `K` 和 `D`。
- 画图部分的本质，是把 `K`、`D`、`J` 三条时间序列用不同颜色叠到同一坐标系里观察交叉和区间位置。

## 详细笔记

课程先用图形例子解释 KDJ 的使用场景。核心不是预测某一根 K 线，而是通过指标所处区间与交叉位置，辅助判断短期是否可能出现反转或拐点。

计算部分，课程把 `RSV` 理解为收盘价在一段时间价格区间中的相对位置，并把 `N` 常设为 `9`。之后再用约定俗成的平滑系数 `2/3` 和 `1/3` 递推出 `K`、`D`。这说明 KDJ 本质上是“区间位置 + 平滑”的组合，而不是单纯均线。

代码实现上，课程重点提到 `pandas` 的 `rolling` 以及扩展窗口思路，先拿到局部高低点，再计算三条线，最后用 `matplotlib` 绘图。和 MACD 一样，真正关键的是先把指标转成可复用的列，而不只是把图画出来。

## 引用与数据

- 课程把 KDJ 的核心观察区间表述为：`80` 上方偏超买，`30` 下方偏超卖。
- 默认窗口 `N` 一般取 `9`。
- 平滑参数按课程口述使用 `2/3` 与 `1/3`，初始 `K`、`D` 缺失时常用 `50` 代替。

## 相关

- [[资料摘要：B站Python量化交易教程（BV1D52CBREpX）]]
- [[量化交易学习路径]]
- [[Wiki 目录]]
