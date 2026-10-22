# 提示词资产

本目录存放可复用的项目级提示词。它们用于启动 AI 任务，生命周期技能用于规定执行方法，`docs/` 用于保存项目事实。

## 使用顺序

1. 先读 `AGENTS.md`、`docs/09-ai-context/AI_CONTEXT.md` 和 `docs/09-ai-context/SKILL_USAGE.md`。
2. 判断当前任务属于哪个生命周期阶段。
3. 阅读对应 `skills/<skill-name>/SKILL.md`。
4. 选择本目录中匹配任务的提示词。
5. 执行后把结果写回 `docs/`、`src/`、`tests/` 或对应交付文件。

## 提示词清单

| 文件 | 用途 |
| --- | --- |
| `01-project-context.md` | 生成或刷新项目上下文 |
| `02-requirement-analysis.md` | 分析模糊需求并补全待确认项 |
| `03-process-standardization.md` | 把任务整理为标准流程 |
| `04-architecture-design.md` | 生成架构、模块、接口和测试策略 |
| `05-code-quality.md` | 指导高质量代码实现和审查 |
| `06-testing-and-acceptance.md` | 生成测试方案、测试用例和验收检查 |
| `07-change-impact-analysis.md` | 分析变更影响和更新范围 |
| `08-test-plan-and-case-authoring.md` | 面向测试人员编写测试方案和高质量测试用例 |

## 使用原则

- 不要把提示词输出当成项目事实，确认后写入 `docs/`。
- 不要一次加载所有提示词，只读取当前任务需要的文件。
- 提示词可以改写，但必须保持输出结构稳定，便于后续 AI 继续处理。
