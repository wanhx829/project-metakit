# Architecture Patterns

本文件记录通用架构模式和选择建议。具体项目应根据实际技术栈裁剪。

## 通用原则

- 先定义边界，再定义模块。
- 先定义接口，再实现细节。
- 稳定接口，不稳定实现。
- 高内聚、低耦合。
- 数据流、控制流和错误流都要可追踪。
- 复杂度不能消失，只能被隔离、命名和管理。

## 常见项目结构

### Web/API 项目

```text
src/
├── api/
├── core/
├── models/
├── services/
├── repositories/
├── integrations/
└── config/
```

适用于后端服务、REST API、内部平台。

### 全栈项目

```text
frontend/
backend/
shared/
docs/
tests/
```

适用于前后端分离应用。共享类型、接口约定和协议说明应放在 `shared/` 或 `docs/02-design/`。

### Monorepo 项目

```text
apps/
services/
packages/
libs/
infrastructure/
docs/
```

适用于多应用、多服务或团队协作项目。必须明确每个包的职责和依赖方向。

### 数据或 AI 项目

```text
src/
├── data/
├── features/
├── models/
├── evaluation/
├── pipelines/
└── serving/
```

适用于数据处理、机器学习、RAG、Agent 和模型服务。必须记录数据来源、评估集和实验结果。

## 设计检查清单

- 模块职责是否单一。
- 接口是否清晰表达输入、输出、错误和权限。
- 数据模型是否覆盖核心实体和关系。
- 是否有不可逆操作、数据迁移或外部依赖。
- 是否能从设计直接生成测试用例。
- 是否需要 ADR 记录技术决策。
