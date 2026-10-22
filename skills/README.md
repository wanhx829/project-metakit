# 内置技能

本目录存放项目模板内置技能。下载本元数据项目后，AI 应根据任务阶段自动选择对应技能。

这些技能是项目生命周期级别的能力，不绑定具体技术栈。它们把需求、设计、开发、测试、验收和运维变更沉淀为 AI 可执行的阶段方法。

## 生命周期映射

| 阶段 | 内置技能 | 主要文档 |
| --- | --- | --- |
| 需求阶段 | `project-requirements` | `docs/01-requirements/` |
| 设计阶段 | `project-design` | `docs/02-design/`, `docs/08-decisions/` |
| 开发阶段 | `project-development` | `src/`, `tests/`, `docs/03-development/` |
| 测试阶段 | `project-testing` | `docs/04-testing/`, `tests/` |
| 验收阶段 | `project-acceptance` | `docs/05-acceptance/` |
| 运维/变更阶段 | `project-operations-change` | `docs/06-release/`, `docs/07-operations/` |

## 使用规则

AI 在处理任务前，应先判断任务属于哪个生命周期阶段，然后阅读对应的 `SKILL.md`。

如果任务跨多个阶段，按顺序使用多个技能。例如：

- “根据需求实现功能并补测试”：先用 `project-requirements`，再用 `project-development`，最后用 `project-testing`。
- “做上线前检查”：先用 `project-testing`，再用 `project-acceptance`，必要时用 `project-operations-change`。
- “修改接口并评估影响”：先用 `project-design`，再用 `project-development`、`project-testing` 和 `project-operations-change`。

## 内置原则

- 文档负责事实：项目背景、需求、设计、测试、验收和运维资料必须落到 `docs/`。
- 提示词负责启动任务：常见 AI 任务使用 `prompts/` 中的提示词模板。
- 技能负责阶段方法：复杂任务先读取对应生命周期技能，再执行。
- 缺失事实必须标记为 `TODO` 或“待确认问题”，不要让 AI 自动补成事实。
