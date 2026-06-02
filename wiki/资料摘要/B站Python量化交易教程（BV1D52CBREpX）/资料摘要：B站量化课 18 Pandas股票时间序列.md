---
title: "资料摘要：B站量化课 18 Pandas股票时间序列"
type: source
status: draft
tags: [量化交易, pandas, 案例]
aliases: []
created: 2026-06-02
updated: 2026-06-02
sources: []
domain: "量化交易"
confidence: high
summary: "本讲把 Pandas 引入股票时间序列分析，围绕日期处理、分组统计和涨跌幅计算做了入门实战。"
source_url: "https://www.bilibili.com/video/BV1D52CBREpX?p=18"
media: video
raw_path: "raw/量化交易/B站Python量化交易教程（BV1D52CBREpX）/18-18量化交易开发Pandas应用-股票分析实战_基于Pandas股票时.md"
source_kind: file
fetched_at: "2026-06-01T16:03:30Z"
---
> 这讲把重点从 NumPy 转到 Pandas，先说明时间序列为什么是金融里最重要的数据结构，再围绕日期处理、分组聚合和涨跌幅计算演示 Pandas 的基础用法。

## 核心要点

- 时间序列是金融数据分析的核心结构，股票、汇率等对象都可以按年、月、日、分钟甚至 tick 级组织和分析。
- Pandas 在时间序列场景中最关键的能力是日期转换、条件筛选和分组聚合。
- 课程通过 `info`、`describe`、`loc`、`groupby`、`diff`、`shift` 等操作，把数据读入、清洗、分组和计算串成一条完整小流程。
- 本讲的目标不是给出复杂策略，而是先让时间字段和 DataFrame 操作变成熟悉工具。

## 详细笔记

- 时间序列分析在课程中被概括成两类主要用途：趋势分析和相关性分析。
- 代码示例先把日期列转为 `datetime`，再提取年份和月份，便于后续分月统计。
- 课程演示了如何找到最小收盘价及其所在整行数据，以及如何按月份统计平均开盘价和平均收盘价。
- 最后通过 `diff` 和 `shift` 计算日涨跌额和涨跌幅比例，展示 Pandas 处理“前一日对当前日”的便利性。

## 引用与数据

- 原始链接：[B站视频第 18 讲](https://www.bilibili.com/video/BV1D52CBREpX?p=18)
- 本讲继续沿用股票代码、日期、开收高低价和成交量的基础样本结构。
- 课程把 `datetime`、`loc` 和 `groupby` 视作 Pandas 时间序列入门最值得先掌握的三类工具。

## 相关

- [[Wiki 目录]]
