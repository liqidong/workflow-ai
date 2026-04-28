# 为什么保持薄

## 背景

AI 编程工具已经能提供很多流程能力，例如规格、计划、TDD、review、QA、发布和复盘。

真正的问题通常不是缺少流程，而是流程很容易变成：

- 多套 source of truth。
- 多份设计和任务状态。
- always-on gate。
- 长期 agent 团队。
- 为流程本身维护控制平面。

## 决策

本仓库只定义薄层：

- route selection
- source-of-truth discipline
- conditional gates
- event-driven learning capture
- conservative multi-agent defaults
- evidence before completion

它不复制外部工具的完整生命周期，不实现 scheduler、ledger、lock service 或 agent runtime。

学习沉淀只在真实失败、用户纠正、重复 drift 或稳定新规则出现时记录。它不是 always-on gate，也不是第二套 source of truth。

## 好处

- 容易复制到不同项目。
- 小任务不会被流程拖慢。
- 大任务仍然有规格、gate 和证据。
- 用户可以替换工具而不替换理念。

## 代价

- 需要用户自己接入项目命令。
- 不会自动强制所有步骤。
- 团队需要在实践中决定哪些 gate 是必要的。
