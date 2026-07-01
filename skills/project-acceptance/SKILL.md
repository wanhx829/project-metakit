---
name: project-acceptance
description: "项目验收阶段技能：用于验收标准、验收用例、交付检查、测试结果评估、上线前质量门禁、交付准备度和完成度判断。"
---

# 项目验收阶段

用于判断项目或阶段交付是否满足需求、测试和交付标准。

## 输入

- `docs/01-requirements/PRODUCT_REQUIREMENTS.md`
- `docs/01-requirements/REQUIREMENT_TRACEABILITY.md`
- `docs/04-testing/TEST_REPORT.md`
- `docs/05-acceptance/ACCEPTANCE_CRITERIA.md`
- `docs/05-acceptance/DELIVERY_CHECKLIST.md`
- `docs/06-release/RELEASE_NOTES.md`

## 工作流

1. 按验收标准逐项检查需求覆盖、测试证据和交付材料。
2. 将每个验收项标记为通过、失败、阻塞、未验证或不适用。
3. 对失败项写清影响、原因、修复建议和是否阻塞发布。
4. 检查发布说明、部署说明、回滚方案和已知问题是否完整。
5. 检查用户文档、配置示例、运行说明和测试报告是否能支撑交付。
6. 输出明确结论：可验收、有条件验收、不可验收。
7. 更新交付检查清单。

## 输出

- 更新 `docs/05-acceptance/ACCEPTANCE_CRITERIA.md`
- 更新 `docs/05-acceptance/DELIVERY_CHECKLIST.md`
- 必要时新增或更新 `docs/05-acceptance/ACCEPTANCE_REPORT.md`

## 质量门槛

- 不以“代码已完成”替代验收通过。
- 缺少测试证据的验收项不能标记为通过。
- 阻塞问题必须明确标注。
- 有条件验收必须写清条件和风险。
- 验收结论必须能追溯到需求编号、测试证据和交付清单。
- 对未验证项必须说明原因和后续处理方式。
