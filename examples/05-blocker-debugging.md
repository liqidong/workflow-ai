# 示例：阻塞问题调试

## 请求

测试突然失败，且失败原因不清楚。

## Route

```text
Route: blocker
Spec layer: inherited / n/a
Spec control surface: <active-change-or-existing-behavior>
Gate: n/a
Learning capture: triggered only if root cause reveals a durable workflow lesson
Problem kind: failing test
Risk level: medium
Control surface: failing test and affected code
Reason: blocker requires investigation before implementation
Verification required: reproduction + root cause + regression check
```

## 示例说明

这个示例展示的是“先调查，再修复”。它避免在没有复现和根因时堆猜测性修改。

## 示例输出

```text
Symptom:
Reproduction:
Suspected cause:
Actual cause:
Fix:
Regression evidence:
Learning capture:
```

