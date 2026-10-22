# AGENTS.md

本文件是 AI 协作入口。任何 AI 在分析、修改或生成本项目内容前，应先阅读本文件。

## 项目阅读顺序

1. 阅读 `README.md`，理解目录用途。
2. 阅读 `docs/09-ai-context/AI_CONTEXT.md`，获取 AI 协作规则和项目事实来源。
3. 阅读 `docs/09-ai-context/AI_WORKFLOW.md`，理解默认工作流。
4. 阅读 `docs/09-ai-context/SKILL_USAGE.md`，判断应使用的生命周期技能。
5. 阅读 `skills/README.md` 和对应阶段的 `SKILL.md`。
6. 如需启动具体任务，阅读 `prompts/README.md` 和对应提示词。
7. 阅读 `docs/00-project/PROJECT_OVERVIEW.md`，理解项目背景和目标。
8. 阅读 `docs/01-requirements/`，理解业务需求。
9. 阅读 `docs/02-design/`，理解系统设计。
10. 阅读 `src/` 和 `tests/`，理解实现和测试。
11. 阅读 `docs/04-testing/` 和 `docs/05-acceptance/`，理解验证标准。

## AI 工作规则

- 不要凭空补充业务事实；缺失信息应标记为 `TODO` 或向项目维护者确认。
- 修改代码前，应先检查相关需求、设计和测试文档。
- 新增功能时，应同步考虑需求、设计、测试、验收是否需要更新。
- 生成文档时，应保持结构清晰，优先使用 Markdown。
- 对重要假设、风险和待确认问题，应记录到对应文档中。
- 复杂任务应先选择生命周期技能，再选择任务提示词。
- 任务结束时应说明修改内容、验证结果、未完成项和风险。

## 项目事实优先级

当资料冲突时，按以下优先级判断：

1. 用户最新明确说明
2. `docs/09-ai-context/AI_CONTEXT.md`
3. `docs/09-ai-context/AI_WORKFLOW.md`
4. `docs/00-project/PROJECT_OVERVIEW.md`
5. 需求文档
6. 设计文档
7. 源码和测试
8. 历史记录或旧文档

## Agent skills

### Issue tracker

本地 Markdown 问题与规格跟踪机制，存储于 `.scratch/<feature>/`。详见 `docs/agents/issue-tracker.md`。

### Triage labels

标准 5 大分类角色标签（`needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`）。详见 `docs/agents/triage-labels.md`。

### Domain docs

单领域模型（Single-context），以根目录 `GLOSSARY.md` 为统一术语源，架构决策记录位于 `docs/adr/`。详见 `docs/agents/domain.md`。

