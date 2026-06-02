---
title: 资料摘要：B站量化课 19 Pandas 实现 K 线图
type: source
status: draft
tags: [教程, 基础, 量化交易, python]
aliases: []
created: 2026-06-02
updated: 2026-06-02
sources: []
domain: "量化交易"
confidence: medium
summary: "本讲把 K 线图从技术分析概念落到 Python 绘图实践，重点演示 `matplotlib` 与 `mplfinance` 的基本用法。"
source_url: https://www.bilibili.com/video/BV1D52CBREpX?p=19
media: video
raw_path: raw/量化交易/B站Python量化交易教程（BV1D52CBREpX）/19-19量化交易开发Pandas应用-股票分析实战_基于Pandas实现K.md
source_kind: file
fetched_at: 2026-06-02T00:03:30Z
---

> 本讲把 K 线图从技术分析概念落到 Python 绘图实践，重点演示 `matplotlib` 与 `mplfinance` 的基本用法。

## 核心要点

- 课程先回顾 K 线图的作用，强调它用于观察价格强弱、多空力量和常见形态，是技术分析里最常见的图形工具之一。
- 用 Python 画 K 线时，单靠 `matplotlib` 可以完成基础蜡烛图，但若想更贴近金融场景，需要配合更专门的 `mplfinance` 一类工具。
- 画图前的数据准备很关键，尤其是开高低收字段、时间格式转换、`DatetimeIndex` 设置，以及成交量序列的整理。
- `mplfinance` 相比基础绘图库更适合金融图表，能直接处理蜡烛图、成交量和后续技术指标展示。

## 详细笔记

本讲延续前一讲的 `pandas` 时间序列处理，开始把股票数据真正画出来。课程先从 K 线图的业务意义切入，再过渡到代码实现，核心是把“技术分析图形”转成“结构化行情数据 + 绘图函数调用”。

实现路径分成两段。第一段是基础版蜡烛图：把开盘价、收盘价、最高价、最低价等字段按函数要求组织好，再设置涨跌颜色、宽度、网格和标题。第二段是更偏金融分析的版本：先把日期列转成 `datetime` 并设为索引，再使用 `mplfinance` 的样式与颜色配置，把蜡烛图和成交量一起画出。

课程还提到一个实际问题：国外绘图库对中文字体支持不算友好，所以中文标题、标签或宋体显示可能需要额外处理。这属于量化可视化里的常见工程细节。

## 引用与数据

- 课程明确把 K 线图称为“蜡烛图”，并用它解释看涨、看跌及多空力量对比。
- 代码实践里重点提到两个库：`matplotlib` 和 `mplfinance`。
- 课程强调 `mplfinance` 对时间格式和数据类型要求较高，因此先做 `datetime` 转换和索引设置是必要步骤。

## 相关

- [[资料摘要：B站Python量化交易教程（BV1D52CBREpX）]]
- [[量化交易学习路径]]
- [[Wiki 目录]]
