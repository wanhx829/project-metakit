# Project MetaKit

**Project MetaKit** 是一套面向 AI 协作的软件项目元数据模板，用于沉淀需求、设计、开发、测试、验收、发布、运维和变更资料。

它的目标不是替代你的业务项目，而是作为每个项目的“元数据骨架”：当你下载这套目录并填入项目资料后，AI 可以按固定入口读取上下文，理解项目生命周期，并更稳定地生成文档、代码、测试和验收材料。

## 适合谁使用

- 希望用 AI 辅助完整软件开发流程的个人或团队。
- 希望把需求、设计、测试、验收等资料标准化管理的项目。
- 希望让 AI 每次进入项目时都有清晰上下文和读取顺序的开发者。
- 希望沉淀测试方案、测试用例、验收标准、发布和运维资料的团队。

## 核心能力

- 标准化项目文档目录。
- AI 友好的项目上下文入口。
- 需求、设计、开发、测试、验收、运维变更全生命周期结构。
- 内置生命周期 skills，指导 AI 在不同阶段按正确方法工作。
- 内置 prompts，支持项目上下文生成、需求分析、架构设计、代码质量、测试验收和变更影响分析。
- 专门强化测试人员视角的测试方案和测试用例编写模块。

## AI 阅读入口

AI 分析项目时，建议按以下顺序读取：

1. [AGENTS.md](./AGENTS.md)
2. [docs/09-ai-context/AI_CONTEXT.md](./docs/09-ai-context/AI_CONTEXT.md)
3. [docs/09-ai-context/AI_WORKFLOW.md](./docs/09-ai-context/AI_WORKFLOW.md)
4. [docs/09-ai-context/SKILL_USAGE.md](./docs/09-ai-context/SKILL_USAGE.md)
5. [skills/README.md](./skills/README.md)
6. [prompts/README.md](./prompts/README.md)
7. [docs/00-project/PROJECT_OVERVIEW.md](./docs/00-project/PROJECT_OVERVIEW.md)
8. [docs/01-requirements/README.md](./docs/01-requirements/README.md)
9. [docs/02-design/README.md](./docs/02-design/README.md)
10. [docs/03-development/README.md](./docs/03-development/README.md)
11. [docs/04-testing/README.md](./docs/04-testing/README.md)
12. [docs/05-acceptance/README.md](./docs/05-acceptance/README.md)

## 目录结构

```text
.
├── AGENTS.md
├── README.md
├── src/
├── tests/
├── scripts/
├── assets/
├── skills/
├── prompts/
└── docs/
    ├── 00-project/
    ├── 01-requirements/
    ├── 02-design/
    ├── 03-development/
    ├── 04-testing/
    ├── 05-acceptance/
    ├── 06-release/
    ├── 07-operations/
    ├── 08-decisions/
    └── 09-ai-context/
```

## 文档分层

| 目录 | 用途 |
| --- | --- |
| `docs/00-project/` | 项目概览、范围、术语 |
| `docs/01-requirements/` | 产品需求、需求追踪、变更请求 |
| `docs/02-design/` | 架构、接口、数据模型、架构模式 |
| `docs/03-development/` | 开发指南、编码规范、代码组织 |
| `docs/04-testing/` | 测试规范、测试流程、测试方案、测试用例、测试报告 |
| `docs/05-acceptance/` | 验收标准、验收报告、交付检查 |
| `docs/06-release/` | 发布说明、部署指南、回滚方案 |
| `docs/07-operations/` | 运维指南、故障响应 |
| `docs/08-decisions/` | 架构决策记录 ADR |
| `docs/09-ai-context/` | AI 上下文、工作流、技能使用和提示词规则 |
| `skills/` | 生命周期阶段技能 |
| `prompts/` | 可复用任务提示词 |

## 内置生命周期 Skills

| 阶段 | Skill | 作用 |
| --- | --- | --- |
| 需求阶段 | `project-requirements` | 需求分析、业务规则、需求追踪 |
| 设计阶段 | `project-design` | 架构、接口、数据模型、ADR |
| 开发阶段 | `project-development` | 代码实现、重构、测试同步 |
| 测试阶段 | `project-testing` | 测试方案、测试点拆解、测试用例、用例评审 |
| 验收阶段 | `project-acceptance` | 验收标准、交付检查、完成度判断 |
| 运维/变更阶段 | `project-operations-change` | 发布、回滚、故障响应、变更影响分析 |

## 内置 Prompts

| 文件 | 用途 |
| --- | --- |
| `prompts/01-project-context.md` | 生成或刷新项目上下文 |
| `prompts/02-requirement-analysis.md` | 分析模糊需求并补全待确认项 |
| `prompts/03-process-standardization.md` | 把任务整理为标准流程 |
| `prompts/04-architecture-design.md` | 生成架构、模块、接口和测试策略 |
| `prompts/05-code-quality.md` | 指导高质量代码实现和审查 |
| `prompts/06-testing-and-acceptance.md` | 生成测试方案、测试用例和验收检查 |
| `prompts/07-change-impact-analysis.md` | 分析变更影响和更新范围 |
| `prompts/08-test-plan-and-case-authoring.md` | 面向测试人员编写测试方案和高质量测试用例 |

## 测试模块

测试目录做了单独强化，适合测试人员输出更完整的测试资料：

- `docs/04-testing/TEST_POLICY.md`：测试规范。
- `docs/04-testing/TEST_PROCESS.md`：测试流程。
- `docs/04-testing/TEST_PLAN.md`：测试方案模板。
- `docs/04-testing/TEST_PLAN_AND_CASE_GUIDE.md`：测试方案与测试用例编写指南。
- `docs/04-testing/TEST_CASES.md`：测试用例模板。
- `docs/04-testing/TEST_CASE_REVIEW_CHECKLIST.md`：测试用例评审清单。
- `docs/04-testing/TEST_REPORT.md`：测试报告。

## 使用方式

1. 复制或下载本仓库。
2. 按项目实际情况填写 `docs/00-project/PROJECT_OVERVIEW.md`。
3. 补充需求文档、设计文档、测试方案和验收标准。
4. 让 AI 先阅读 `AGENTS.md` 和 `docs/09-ai-context/AI_CONTEXT.md`。
5. 根据任务阶段，让 AI 使用对应 `skills/` 和 `prompts/`。

建议优先填写：

1. `docs/00-project/PROJECT_OVERVIEW.md`
2. `docs/01-requirements/PRODUCT_REQUIREMENTS.md`
3. `docs/02-design/ARCHITECTURE.md`
4. `docs/04-testing/TEST_PLAN.md`
5. `docs/04-testing/TEST_CASES.md`
6. `docs/05-acceptance/ACCEPTANCE_CRITERIA.md`
7. `docs/09-ai-context/AI_CONTEXT.md`

## 维护原则

- 文档负责事实，提示词负责启动任务，技能负责阶段方法。
- 需求变化后，同步更新需求、设计、测试和验收资料。
- 重要技术决策记录到 `docs/08-decisions/`。
- AI 相关提示、约束、阅读顺序记录到 `docs/09-ai-context/`。
- 生命周期方法记录到 `skills/`，任务提示词记录到 `prompts/`。
- 不确定内容使用 `TODO` 或“待确认问题”标记，避免 AI 把未确认信息当成事实。

## 仓库地址

```text
https://github.com/wanhx829/project-metakit
```
