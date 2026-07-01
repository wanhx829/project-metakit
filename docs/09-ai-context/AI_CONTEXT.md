# AI Context

## 项目事实来源

AI 分析项目时，应优先读取以下文件：

1. `AGENTS.md`
2. `README.md`
3. `docs/09-ai-context/AI_WORKFLOW.md`
4. `docs/09-ai-context/SKILL_USAGE.md`
5. `skills/README.md`
6. `prompts/README.md`
7. `docs/00-project/PROJECT_OVERVIEW.md`
8. `docs/01-requirements/PRODUCT_REQUIREMENTS.md`
9. `docs/02-design/ARCHITECTURE.md`
10. `docs/04-testing/TEST_PLAN.md`
11. `docs/05-acceptance/ACCEPTANCE_CRITERIA.md`

## AI 可执行任务

- 根据需求生成设计草案。
- 根据设计生成源码。
- 根据需求和设计生成测试用例。
- 根据测试结果生成测试报告。
- 根据验收标准判断交付是否完成。
- 根据变更内容分析影响范围。
- 根据项目阶段选择 `skills/` 中的生命周期技能。
- 根据任务类型选择 `prompts/` 中的提示词模板。

## AI 禁止行为

- 不要把 `TODO` 当成已确认事实。
- 不要删除未知用途的文档或代码。
- 不要在没有依据的情况下改变业务规则。
- 不要忽略需求、设计、测试、验收之间的一致性。
- 不要把提示词输出直接当成事实；确认后再写入项目文档。
- 不要一次性加载所有技能和提示词，只读取当前任务需要的内容。

## 生成内容要求

- 文档使用 Markdown。
- 表格字段应保持稳定，便于后续 AI 继续追加。
- 所有假设应写入“假设”或“待确认问题”部分。
- 涉及需求、设计、测试、验收时，应尽量标注关联编号。
- 阶段性工作结束后，应记录验证结果、未完成项和风险。
