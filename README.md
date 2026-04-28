# Workflow AI 薄工作流

这是一个可复制的 AI 编程薄工作流模板仓库。它是文档和 agent 指令模板，不是可运行的工作流工具。

唯一操作契约在 [AGENTS.md](AGENTS.md)。其他文件只解释如何阅读、复制和理解这份契约。

## 适合谁

- 已经在用 AI 编程代理，但不想让流程越来越重的人。
- 想把规格、执行纪律、质量 gate 分清楚的人。
- 想分享一份可以直接下载、阅读、合并的轻量 agent 规则的人。

## 文件

- [AGENTS.md](AGENTS.md): 唯一操作契约。
- [CLAUDE.md](CLAUDE.md): Claude Code 兼容入口，只导入 `AGENTS.md`。
- [GEMINI.md](GEMINI.md): Gemini CLI 兼容入口，只导入 `AGENTS.md`。
- [docs/quickstart.md](docs/quickstart.md): 如何把它合并到自己的项目。
- [docs/rationale.md](docs/rationale.md): 为什么保持薄。
- [examples/](examples): 七个阅读示例，覆盖六个 route 和事件驱动学习沉淀。

## 快速使用

```bash
git clone https://github.com/liqidong/workflow-ai.git
cd workflow-ai
```

阅读 [docs/quickstart.md](docs/quickstart.md)，然后手动把 [AGENTS.md](AGENTS.md) 中适合你的部分合并到自己的项目。

## 可选工具映射

这些只是常见实现，不是本仓库依赖：

- OpenSpec 可以作为规格层实现。
- Superpowers-like 技能可以作为执行层纪律。
- gstack 可以作为 gate 层实现。
- self-improvement-like agent 可以作为事件驱动学习沉淀层，记录仍应进入项目已有的单一学习日志或知识库。

如果你的团队已经有等价工具，保留角色分工即可。

## Agent 识别

| Agent / 工具 | 自动识别入口 |
| --- | --- |
| Codex、Copilot coding agent、Cursor、Cline、Windsurf 等支持 `AGENTS.md` 的工具 | `AGENTS.md` |
| Claude Code | `CLAUDE.md`，只导入 `AGENTS.md` |
| Gemini CLI | `GEMINI.md`，只导入 `AGENTS.md` |

`AGENTS.md` 仍然是唯一操作契约，兼容入口不复制规则。

## 仓库边界

本仓库不提供工具安装、自动化脚本、后台调度器或控制平面。

## License

MIT. See [LICENSE](LICENSE).
