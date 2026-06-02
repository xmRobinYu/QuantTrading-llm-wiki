---
title: 资料摘要：B站量化课 27 Context 与 Position 对象
type: source
status: draft
tags: [教程, 基础, 量化交易, python]
aliases: []
created: 2026-06-02
updated: 2026-06-02
sources: []
domain: "量化交易"
confidence: medium
summary: "本讲讲解策略运行时最常见的两个对象：`context` 负责全局上下文，`position` 负责单个持仓信息。"
source_url: https://www.bilibili.com/video/BV1D52CBREpX?p=27
media: video
raw_path: raw/量化交易/B站Python量化交易教程（BV1D52CBREpX）/27-27量化策略编写-Python量化交易编程第一步_量化交易策略实战.md
source_kind: file
fetched_at: 2026-06-02T00:03:32Z
---

> 本讲讲解策略运行时最常见的两个对象：`context` 负责全局上下文，`position` 负责单个持仓信息。

## 核心要点

- `context` 是策略运行时的信息总入口，账户、时间、股票池、持仓等内容都能从这里拿到。
- 课程把 `portfolio`、`subportfolios`、`current_dt`、`previous_date`、`universe` 视为 `context` 里的常见属性。
- `position` 代表单个持仓对象，常看字段包括证券代码、最新价格、总仓位和建仓时间。
- 代码实践通过打印总资产、持仓金额、累计收益、可用资金等数据，让这两个对象从抽象概念变成可观察接口。

## 详细笔记

这讲的重点是“策略到底在什么上下文里运行”。前面的交易函数和订单对象更多关注动作，这里则开始建立策略状态视角。

`context` 可以理解为策略的运行现场。课程演示了如何从中读取总账户、子账户、当前时间、前一交易日和股票池，还展示了如何查看累计收益与可用资金。这说明绝大多数策略判断，最终都离不开 `context` 提供的数据入口。

`position` 则是持仓层面的最小观察单元。课程用下单后再遍历持仓的方式，展示如何看每个持仓的代码、仓位数量、当前价值和建仓时间。对后续做仓位控制、止盈止损或持仓诊断，这类对象是基础。

## 引用与数据

- 课程将 `context` 描述为“策略信息的总览”。
- 常见的 `context` 属性包括 `portfolio`、`subportfolios`、`current_dt`、`previous_date`、`universe`。
- `position` 对象演示字段包括证券代码、最新价格、总仓位与建仓时间。

## 相关

- [[资料摘要：B站Python量化交易教程（BV1D52CBREpX）]]
- [[量化交易学习路径]]
- [[Wiki 目录]]
