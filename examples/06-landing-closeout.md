# 示例：收尾和合并

## 请求

实现已经完成，需要判断是否可以合并、发布或归档。

## Route

```text
Route: landing
Spec layer: inherited / n/a
Spec control surface: <active-change-if-any>
Gate: review / release gate if risk warrants it
Learning capture: triggered only if this round produced a durable lesson
Problem kind: none
Risk level: medium
Control surface: final diff, checks, review findings
Reason: work is at closeout stage
Verification required: final checks + review/deploy/archive decision
```

## 示例说明

这个示例展示的是“收尾只回答收尾问题”。如果发现 blocking drift，应回到对应 route，而不是在 landing 阶段重新展开规划。

## 示例输出

```text
Summary:
Final checks:
Review result:
Archive / release decision:
skipped_verification:
  check:
  reason:
  residual_risk:
  follow_up:
Follow-up:
```
