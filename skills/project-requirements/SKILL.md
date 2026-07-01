---
name: project-requirements
description: "项目需求阶段技能：用于新项目立项、需求分析、产品需求文档、用户故事、业务规则、需求澄清、范围定义、需求变更和需求追踪。"
---

# 项目需求阶段

用于把原始想法、业务描述和用户反馈整理成可设计、可开发、可测试、可验收的需求资料。

## 输入

- `docs/00-project/PROJECT_OVERVIEW.md`
- `docs/01-requirements/PRODUCT_REQUIREMENTS.md`
- `docs/01-requirements/REQUIREMENT_TRACEABILITY.md`
- 用户最新说明、会议纪要、原型、截图或历史变更记录

## 工作流

1. 识别显性需求、隐性需求、目标用户、业务边界和非目标范围。
2. 提取关键词、核心术语、业务实体、外部依赖和关键约束。
3. 将需求拆成可编号条目，使用 `REQ-xxx` 标识。
4. 区分功能需求、非功能需求、业务规则、约束、假设和待确认问题。
5. 为每条需求写清触发条件、主流程、异常流程、输入输出和验收线索。
6. 对缺失信息使用 `TODO` 或“待确认问题”，不要补成事实。
7. 更新需求追踪矩阵，连接到设计、代码、测试和验收项。

## 输出

- 更新 `docs/01-requirements/PRODUCT_REQUIREMENTS.md`
- 更新 `docs/01-requirements/REQUIREMENT_TRACEABILITY.md`
- 必要时更新 `docs/00-project/SCOPE.md` 或 `docs/00-project/GLOSSARY.md`

## 质量门槛

- 每条需求都有唯一编号。
- 每条 P0/P1 需求都有可验证的验收线索。
- 非功能需求必须写明验证方式。
- 需求冲突必须列入待确认问题。
- 需求必须能支撑后续设计、测试和验收，不接受只有口号的需求。
- 输出应包含“已确认事实”和“待确认问题”，避免 AI 把假设当事实。
