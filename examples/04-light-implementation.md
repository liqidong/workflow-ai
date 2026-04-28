# 示例：已接受范围内实现

## 请求

在已有规格和任务清单下，实现一个已经确认的小功能切片。

## Route

```text
Route: light
Spec layer: inherited
Spec control surface: <active-change>
Gate: n/a
Learning capture: n/a
Problem kind: none
Risk level: medium
Control surface: active spec / accepted plan
Reason: scope already accepted, no behavior expansion
Verification required: targeted tests + smoke if behavior is user-visible
```

## 示例说明

这个示例展示的是“继承已有规格继续实现”。在这个场景里，没有 scope expansion，也没有额外 gate 被触发。

## 示例执行

- 读取 active spec 或 accepted plan。
- 确认本次只做一个 coherent milestone。
- 实现最小切片。
- 运行 targeted tests。
- 如有用户可见行为，补一个 smoke proof。
