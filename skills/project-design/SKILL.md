---
name: project-design
description: "项目设计阶段技能：用于架构设计、模块设计、接口设计、数据模型、技术选型、ADR 决策记录、AI 应用、LLM 应用、RAG 系统和 MCP 集成设计。"
---

# 项目设计阶段

用于把需求转换成可实现、可测试、可演进的设计资料。

## 输入

- `docs/01-requirements/PRODUCT_REQUIREMENTS.md`
- `docs/01-requirements/REQUIREMENT_TRACEABILITY.md`
- `docs/02-design/ARCHITECTURE.md`
- `docs/02-design/API_SPEC.md`
- `docs/02-design/DATA_MODEL.md`
- `docs/08-decisions/ADR_TEMPLATE.md`

## 工作流

1. 从需求中提取核心场景、边界、数据、权限和非功能要求。
2. 设计系统边界、核心模块、模块职责、输入输出和依赖关系。
3. 先定义稳定接口，再考虑具体实现；接口应包含输入、输出、错误、权限和兼容性约束。
4. 设计数据模型、状态变化、数据生命周期和迁移策略。
5. 使用 Mermaid 或文字图描述核心数据流、控制流和时序关系。
6. 对关键技术选型写 ADR，记录背景、决策、影响和替代方案。
7. 如果项目涉及 AI 应用，补充提示词、工具结构、评估、日志、成本和安全约束。
8. 如果项目涉及 MCP，明确工具、资源、提示词的边界、参数结构、副作用和测试策略。
9. 更新需求追踪矩阵中的设计覆盖关系。

## 输出

- 更新 `docs/02-design/ARCHITECTURE.md`
- 更新 `docs/02-design/API_SPEC.md`
- 更新 `docs/02-design/DATA_MODEL.md`
- 必要时新增 `docs/08-decisions/ADR-xxxx-*.md`

## 质量门槛

- 每个核心需求都有设计覆盖。
- 每个模块职责边界清晰，不混合不相关职责。
- 接口和数据模型能支持测试用例生成。
- 重要技术取舍有 ADR 记录。
- 复杂设计必须写明风险、替代方案和验证方式。
- 设计应保持局部简单、整体可组合，避免无依据的过度抽象。
