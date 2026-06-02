---
title: 资料摘要：B站量化课 28 Portfolio 与 SubPortfolio 对象
type: source
status: draft
tags: [教程, 基础, 量化交易, python]
aliases: []
created: 2026-06-02
updated: 2026-06-02
sources: []
domain: "量化交易"
confidence: medium
summary: "本讲聚焦账户层对象，区分总账户 `portfolio` 和子账户 `subportfolio` 能看见的资产与资金字段。"
source_url: https://www.bilibili.com/video/BV1D52CBREpX?p=28
media: video
raw_path: raw/量化交易/B站Python量化交易教程（BV1D52CBREpX）/28-28量化策略编写-Python量化交易编程第一步_量化交易策略实战.md
source_kind: file
fetched_at: 2026-06-02T00:03:33Z
---

> 本讲聚焦账户层对象，区分总账户 `portfolio` 和子账户 `subportfolio` 能看见的资产与资金字段。

## 核心要点

- `portfolio` 代表总账户信息，更偏资产全景，如多头仓位、空头仓位、总权益、累计收益、初始资金和持仓市值。
- `subportfolio` 代表子账户信息，更偏资金维度，如累计出入金、可用资金、可取资金、挂单锁定资金和账户类型。
- A 股教学场景里，空头仓位通常为空，这也提醒学员区分平台对象能力与市场实际约束。
- 课程通过打印字段值，让“账户权益”和“资金状态”这两个视角被明确拆开。

## 详细笔记

前一讲的 `context` 更像总入口，这一讲则把入口里的账户对象继续拆细。`portfolio` 关注的是资产层面：你总共值多少钱、持仓价值多少、累计收益怎样、账户里有哪些多头或空头仓位。

`subportfolio` 则更贴近资金调度。它关心的不是总收益曲线，而是现金今天能不能用、能不能取、多少资金因为挂单被冻结，以及这个子账户属于股票、基金还是其他类型。对多账户、多资产类别策略而言，这一层拆分很重要。

课程虽然用的是入门场景，但这讲其实在为后面的组合管理和真实交易约束打基础。账户对象越理解清楚，越不容易把“回测赚钱”和“账户能不能执行”混为一谈。

## 引用与数据

- `portfolio` 演示字段包括 `long_positions`、`short_positions`、`total_value`、`returns`、`starting_cash`、`positions_value`。
- `subportfolio` 演示字段包括 `inout_cash`、`available_cash`、`transferable_cash`、`locked_cash`、`type`。
- 课程明确指出 A 股场景下空头仓位通常不存在或很少使用。

## 相关

- [[资料摘要：B站Python量化交易教程（BV1D52CBREpX）]]
- [[量化交易学习路径]]
- [[Wiki 目录]]
