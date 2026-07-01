# 技能使用说明

本文件说明 AI 如何在项目生命周期中使用内置技能。

## 总规则

1. 先读 `AGENTS.md` 和 `docs/09-ai-context/AI_CONTEXT.md`。
2. 判断用户任务属于哪个生命周期阶段。
3. 阅读 `skills/<skill-name>/SKILL.md`。
4. 按技能的输入、工作流、输出和质量门槛执行。
5. 跨阶段任务应组合多个技能，并同步更新追踪矩阵。

## 阶段触发

| 用户意图 | 应使用技能 |
| --- | --- |
| 梳理想法、写 PRD、拆需求、问业务规则 | `project-requirements` |
| 设计架构、接口、数据模型、技术选型 | `project-design` |
| 写代码、改代码、修 bug、重构、接入服务 | `project-development` |
| 写测试方案、测试用例、自动化测试、测试报告 | `project-testing` |
| 判断是否完成、是否可交付、是否可上线 | `project-acceptance` |
| 发布、部署、回滚、故障、配置、变更影响分析 | `project-operations-change` |

## AI 默认读取路径

```text
AGENTS.md
README.md
docs/09-ai-context/AI_CONTEXT.md
docs/09-ai-context/SKILL_USAGE.md
skills/README.md
skills/<matched-skill>/SKILL.md
```

## 与提示词配合

生命周期技能用于规定“怎么做”，`prompts/` 用于启动具体任务。常见组合：

| 任务 | 技能 | 提示词 |
| --- | --- | --- |
| 生成项目上下文 | `project-requirements` | `prompts/01-project-context.md` |
| 澄清需求 | `project-requirements` | `prompts/02-requirement-analysis.md` |
| 标准化流程 | 对应阶段技能 | `prompts/03-process-standardization.md` |
| 架构设计 | `project-design` | `prompts/04-architecture-design.md` |
| 代码实现和审查 | `project-development` | `prompts/05-code-quality.md` |
| 测试和验收 | `project-testing`, `project-acceptance` | `prompts/06-testing-and-acceptance.md` |
| 测试方案和测试用例编写 | `project-testing` | `prompts/08-test-plan-and-case-authoring.md` |
| 变更影响分析 | `project-operations-change` | `prompts/07-change-impact-analysis.md` |

## 注意

这些内置技能是 Markdown 形式的项目能力说明。不同 AI 工具对自动发现本地 `skills/` 的支持不完全一致；即使工具不能自动加载，也可以通过 `AGENTS.md` 和本文件明确要求 AI 阅读对应技能。
