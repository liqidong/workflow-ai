# 快速开始

这个页面只说明如何复制和合并。具体操作规则以根目录 [AGENTS.md](../AGENTS.md) 为准。

## 1. Clone

```bash
git clone https://github.com/liqidong/workflow-ai.git
cd workflow-ai
```

## 2. 阅读操作契约

打开 [AGENTS.md](../AGENTS.md)，先完整读一遍。

如果使用 Claude Code 或 Gemini CLI，仓库根目录也提供了只导入 `AGENTS.md` 的兼容入口文件。

## 3. 合并到自己的项目

如果你的项目没有 agent 说明文件，可以把 `AGENTS.md` 作为起点。

如果你的项目已经有 `AGENTS.md`、`CLAUDE.md` 或类似文件，手动复制需要的段落，不要直接覆盖。

## 4. 补充本地命令

这份模板不包含项目命令。你需要在自己的项目说明里补充：

- 测试命令。
- 构建或 lint 命令。
- 发布、部署或 smoke 命令。

## 5. 试用

建议先在一个中等复杂度任务上试用。试用后的判断标准很简单：

- 是否减少重复文档。
- 是否减少需求漂移。
- 是否让完成证据更清楚。
