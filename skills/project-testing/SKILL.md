---
name: project-testing
description: "项目测试阶段技能：用于测试规范、测试流程、测试方案编写、测试点拆解、测试用例设计、用例评审、自动化测试、回归测试、质量门禁、测试报告和 AI 生成测试校验。"
---

# 项目测试阶段

用于把需求、设计和实现转换成可执行、可追踪的测试资料和测试代码。

## 输入

- `docs/01-requirements/PRODUCT_REQUIREMENTS.md`
- `docs/01-requirements/REQUIREMENT_TRACEABILITY.md`
- `docs/02-design/`
- `docs/04-testing/TEST_POLICY.md`
- `docs/04-testing/TEST_PROCESS.md`
- `docs/04-testing/TEST_PLAN.md`
- `docs/04-testing/TEST_PLAN_AND_CASE_GUIDE.md`
- `docs/04-testing/TEST_CASES.md`
- `docs/04-testing/TEST_CASE_REVIEW_CHECKLIST.md`
- `src/`
- `tests/`

## 工作流

1. 从需求追踪矩阵中找出未覆盖或高优先级需求。
2. 先写测试方案，明确测试目标、范围、不测试范围、环境、数据、策略、准入准出标准。
3. 拆解测试点，覆盖主流程、异常流程、边界值、权限、数据一致性、兼容性、性能和安全。
4. 为每条核心需求设计正向、异常、边界和回归用例。
5. 按 `TEST_CASES.md` 字段写用例，确保前置条件、测试数据、步骤和预期结果可执行、可判断。
6. 使用 `TEST_CASE_REVIEW_CHECKLIST.md` 评审用例质量，删除重复、模糊、不可执行的用例。
7. 能自动化的优先生成自动化测试，不能自动化的写清手工步骤。
8. 对接口、数据模型、权限、安全、并发、性能进行专项检查。
9. 对 AI 相关功能补充评估集、不可接受失败、人工抽检和日志检查。
10. 执行可用测试命令并记录结果。
11. 更新需求追踪矩阵中的测试覆盖关系。

## 输出

- 更新 `docs/04-testing/TEST_PLAN.md`
- 更新 `docs/04-testing/TEST_PLAN_AND_CASE_GUIDE.md`，当项目测试方法需要特殊约定时
- 更新 `docs/04-testing/TEST_CASES.md`
- 更新 `docs/04-testing/TEST_CASE_REVIEW_CHECKLIST.md`
- 更新 `tests/`
- 必要时更新 `docs/04-testing/TEST_REPORT.md`

## 质量门槛

- P0/P1 需求必须有测试覆盖。
- 测试用例必须包含前置条件、步骤和预期结果。
- 测试用例必须关联需求编号、测试类型和优先级。
- 预期结果必须可观察、可判断，不使用“正常显示”等模糊表述。
- 自动化测试失败不能被忽略；无法执行时说明原因。
- 测试报告要区分通过、失败、阻塞和未执行。
- 测试结论必须基于证据，不能只写“看起来正常”。
- 缺陷应写明复现步骤、实际结果、预期结果和影响范围。
