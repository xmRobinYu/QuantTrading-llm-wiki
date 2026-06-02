---
title: 资料摘要：B站量化课 20 Matplotlib 绘制 MACD
type: source
status: draft
tags: [教程, 基础, 量化交易, python]
aliases: []
created: 2026-06-02
updated: 2026-06-02
sources: []
domain: "量化交易"
confidence: medium
summary: "本讲讲清 MACD 的五个核心组成，并用 `pandas` 的 `ewm` 与 `matplotlib` 把指标线和柱状图画出来。"
source_url: https://www.bilibili.com/video/BV1D52CBREpX?p=20
media: video
raw_path: raw/量化交易/B站Python量化交易教程（BV1D52CBREpX）/20-20量化交易开发Matplotlib应用-股票技术分析实战_基于Mat0.md
source_kind: file
fetched_at: 2026-06-02T00:03:30Z
---

> 本讲讲清 MACD 的五个核心组成，并用 `pandas` 的 `ewm` 与 `matplotlib` 把指标线和柱状图画出来。

## 核心要点

- MACD 被拆成短期 EMA、长期 EMA、`DIF`、`DEA` 和 MACD 柱五个部分，课程用它解释趋势方向与变化速度。
- 指标计算的重点不是手写循环，而是利用 `pandas` 的 `ewm(...).mean()` 快速得到指数移动均线。
- 绘图时，`matplotlib` 的 `bar` 用于表现多空柱状图，折线用于表现 `DIF` 和 `DEA` 两条信号线。
- 课程强调：MACD 大于零通常对应上升趋势，小于零通常对应下降趋势，零轴是重要参考线。

## 详细笔记

这讲先回顾 MACD 的业务含义，再进入公式和实现。课程把短期 EMA 设为 `12` 日，长期 EMA 设为 `26` 日，`DIF` 是二者差值，`DEA` 是 `DIF` 的 `9` 日指数移动均线，MACD 柱则是 `DIF - DEA` 后再放大展示。

实现上，课程明显偏向 `pandas` 向量化思路。先从收盘价序列出发，用 `ewm` 求短期和长期 EMA，再得到 `DIF`、`DEA` 和柱状图序列。这样写法比手工循环更短，也更适合后续批量算指标。

画图部分延续前几讲的 `matplotlib` 思路：先准备画布，再给正柱和负柱分配不同颜色，最后叠加两条均线并设置图例。整讲的重点，是把技术指标从“看图识别”转成“先算序列，再标准化绘图”。

## 引用与数据

- 课程给出的常用参数是：短期 EMA `12` 日、长期 EMA `26` 日、`DEA` 常取 `9` 日。
- 指标实现里明确点名 `pandas` 的 `ewm` 函数和 `matplotlib` 的 `bar` 柱状图函数。
- 业务解释里，MACD 正值对应上升趋势，负值对应下降趋势，零轴用于区分多空区域。

## 相关

- [[资料摘要：B站Python量化交易教程（BV1D52CBREpX）]]
- [[量化交易学习路径]]
- [[Wiki 目录]]
