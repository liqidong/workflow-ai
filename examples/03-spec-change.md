# 示例：规格驱动改动

## 请求

给已有应用增加 CSV 导出能力。

## Route

```text
Route: full
Spec layer: required
Spec control surface: <change-id>
Gate: design review only if UI interaction is non-trivial
Learning capture: n/a
Problem kind: none
Risk level: medium
Control surface: proposal / design / tasks
Reason: user-visible feature with behavior and error semantics
Verification required: targeted tests + smoke if UI exists
```

## 示例规格

```text
Why:
Users need a simple way to export visible table data for offline analysis.

What:
- Export the current filtered table view as CSV.
- Preserve existing permission checks.
- Return a clear error when export fails.

Non-goals:
- No scheduled exports.
- No background jobs.
- No new reporting dashboard.
```

## 示例任务

- [ ] Define CSV columns and empty-state behavior.
- [ ] Add serialization test.
- [ ] Implement export action.
- [ ] Add UI trigger if needed.
- [ ] Run targeted tests.
- [ ] Run review if risk warrants it.
