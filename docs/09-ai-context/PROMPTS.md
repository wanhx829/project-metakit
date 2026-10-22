# Prompts

本文件保留常用提示词入口。完整任务提示词放在项目根目录 `prompts/`。

## 推荐入口

- `prompts/01-project-context.md`：项目上下文生成。
- `prompts/02-requirement-analysis.md`：需求分析。
- `prompts/03-process-standardization.md`：流程标准化。
- `prompts/04-architecture-design.md`：架构设计。
- `prompts/05-code-quality.md`：高质量代码。
- `prompts/06-testing-and-acceptance.md`：测试与验收。
- `prompts/07-change-impact-analysis.md`：变更影响分析。
- `prompts/08-test-plan-and-case-authoring.md`：测试方案与测试用例编写。

## 项目理解提示词

请按以下顺序阅读项目资料，并输出项目摘要、核心需求、架构要点、测试重点和待确认问题：

1. `AGENTS.md`
2. `README.md`
3. `docs/09-ai-context/AI_CONTEXT.md`
4. `docs/00-project/PROJECT_OVERVIEW.md`
5. `docs/01-requirements/`
6. `docs/02-design/`
7. `docs/04-testing/`
8. `docs/05-acceptance/`

## 需求到测试提示词

请根据 `docs/01-requirements/PRODUCT_REQUIREMENTS.md` 和 `docs/02-design/ARCHITECTURE.md` 生成测试方案和测试用例，并更新 `docs/04-testing/TEST_PLAN.md` 与 `docs/04-testing/TEST_CASES.md`。

## 变更影响分析提示词

请根据本次变更内容，分析影响到的需求、设计、源码、测试和验收文档，并列出必须同步更新的文件。
