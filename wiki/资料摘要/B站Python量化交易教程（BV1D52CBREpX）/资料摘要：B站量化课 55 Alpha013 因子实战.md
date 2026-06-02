---
title: 资料摘要：B站量化课 55 Alpha013 因子实战
type: source
status: draft
tags: [教程, 因子, 量化交易, python]
aliases: []
created: 2026-06-02
updated: 2026-06-02
sources: []
domain: "量化交易"
confidence: medium
summary: "本讲把国泰君安 Alpha191 体系引入课程，并用 Alpha013 因子 `sqrt(high*low)-VWAP` 做单因子分析实战。"
source_url: https://www.bilibili.com/video/BV1D52CBREpX?p=55
media: video
raw_path: raw/量化交易/B站Python量化交易教程（BV1D52CBREpX）/55-55Python量化交易--因子分析_量化因子分析--alpha因子.md
source_kind: file
fetched_at: 2026-06-02T00:03:43Z
---

> 本讲把国泰君安 Alpha191 体系引入课程，并用 Alpha013 因子 `sqrt(high*low)-VWAP` 做单因子分析实战。

## 核心要点

- 课程把 Alpha 因子放回到国泰君安《基于短周期价量特征的多因子选股体系》语境里，强调 `Alpha191` 更像一套因子体系，而不是单个因子。
- 本讲选取 `Alpha013` 做实战，公式是 `sqrt(high * low) - VWAP`，依赖最高价、最低价、成交量和成交额数据。
- 代码沿用上一讲的单因子分析框架，在沪深 300 成分股上完成因子计算、分层展示和收益观察。
- 口播结论认为，这个因子相较上一讲的 `MA5` 因子收益略好，但负相关更常见，且换手率明显更高。

## 详细笔记

### 因子背景

课程先补了一层背景：`Alpha191` 来自国泰君安量化研究报告，聚宽后来把这套因子实现并开源。讲师反复强调，这里说的 Alpha 因子不是抽象名词，而是已经被整理成可直接调用的短周期价量因子集合。

### 本讲实现的因子

本讲实战对象是 `Alpha013`。按字幕给出的口径，核心公式是：

- `sqrt(high * low) - VWAP`

其中 `VWAP` 需要由成交量与成交额共同计算，因此实现时除了 `high`、`low`，还依赖 `volume` 和 `money`。

### 代码与结果观察

课程在自定义因子类里设置了因子名、`max_window=1` 和依赖字段，然后继续沿用上一讲的单因子分析与绘图流程。口播结果里有三点值得记：

- 一天、五天、十天收益里，十天收益表现相对更能看。
- IC 口播判断为负相关居多。
- 换手率显著高于上一讲 `MA5` 因子，字幕里给出的对比是一日换手率接近 `0.9`，而 `MA` 因子大约只有 `0.05`。

## 引用与数据

- 课程明确把 `Alpha191` 指向国泰君安报告《基于短周期价量特征的多因子选股体系》。 
- 本讲实战因子公式：`sqrt(high * low) - VWAP`。
- 口播对比结论：`Alpha013` 收益略好于上一讲 `MA5`，但相关性偏负、换手率更高。

## 相关

- [[资料摘要：B站Python量化交易教程（BV1D52CBREpX）]]
- [[Wiki 目录]]
