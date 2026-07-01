# 项目上下文生成提示词

请基于当前仓库、已有文档和用户最新说明，生成或更新项目上下文。

## 读取顺序

1. `AGENTS.md`
2. `README.md`
3. `docs/09-ai-context/AI_CONTEXT.md`
4. `docs/00-project/PROJECT_OVERVIEW.md`
5. `docs/01-requirements/`
6. `docs/02-design/`
7. `docs/04-testing/`
8. `docs/05-acceptance/`

## 输出结构

```markdown
# 项目上下文

## 项目概要

## 当前目标

## 项目范围

## 非目标范围

## 关键实体与关系

## 功能模块

## 技术方向与关键决策

## 已确认事实

## 待确认问题

## 风险与下一步
```

## 规则

- 未明确的信息写为 `暂无信息` 或 `TODO`。
- 不虚构业务事实。
- 重要结论应能追溯到已有文档或用户说明。
- 生成后建议同步更新 `docs/09-ai-context/AI_CONTEXT.md`。
