# AI 编程薄工作流

这是给 AI 编程代理使用的通用项目级说明。把它合并到你的项目规则里，不要直接覆盖已有规则。

## 工作方式

- 优先正确、可复现、可验证的方案，不追求脆弱的聪明写法。
- 修改前先读最近的项目说明和相关配置。
- 修 bug 时先复现，再定位根因，再修复。
- 做功能和重构时先检查受影响模块，再改行为。
- 宣称完成前，先运行最小有意义验证，并说明实际检查了什么。

## Source Of Truth

- 规格层负责 WHAT 和 WHY。
- 实现计划、执行包、agent brief 只说明 HOW，不能覆盖验收标准。
- gate 按风险触发。只有任务需要时才使用产品、架构、设计、QA、安全或发布 gate。
- 不创建互相竞争的设计文档、任务台账或状态系统。

## Learning Capture

- 学习沉淀是事件驱动记录层，不是 always-on gate。
- 只有真实失败、用户纠正、重复 drift、或稳定的新流程改进出现时才记录。
- 记录应进入项目已有的单一学习日志或知识库。
- 学习记录不能成为第二套 source of truth，也不能阻塞当前 root-cause 修复。

## Route Modes

非平凡任务先选择最小安全 route：

- `assess`: 只读评估、研究、解释、状态检查、路线建议。
- `micro`: 极小低风险改动，配最小有用验证。
- `light`: 在已接受范围或 active spec 内实现、调试、硬化。
- `full`: 新功能、架构、契约、安全、部署、工作流或生产行为变化。
- `blocker`: 失败测试、失败 smoke、用户纠正、重复失败、不明回归或 drift。
- `landing`: review、PR、发布、部署、归档或 closeout。

硬门槛：

- 高风险工作不能走 `micro`。
- blocker、correction、repeated failure 必须先调查再实现。
- active spec implementation 默认继承 active change，除非 scope 变化。
- 工作流、指令、agent 文件属于 supply-chain sensitive。
- skipped verification 必须显式记录。

## Multi-Agent Rules

- 主线程负责需求、边界、验收、集成和最终决策。
- 默认一个 coherent milestone 只用一个 writer。
- 每个 checkpoint 使用一个新的只读 reviewer。
- explorer/docs agent 按需使用，通常只读。
- 并行 writer 必须有独立 worktree、互不重叠写集和明确 ownership。

## Evidence Rule

没有新鲜证据，不宣称完成。

如果跳过验证，必须报告：

```yaml
skipped_verification:
  check:
  reason:
  residual_risk:
  follow_up:
```

## Route Trace

非平凡任务报告：

```text
Route:
Spec layer:
Spec control surface:
Gate:
Learning capture: triggered only / n/a
Problem kind:
Risk level:
Control surface:
Reason:
Verification required:
```
