# Requirement Traceability

用于追踪需求到设计、代码、测试和验收的覆盖关系。当前正式需求主要来自 `docs/01-requirements/需求文档.md`，详细设计主要来自 `docs/02-design/设计文档.md`；`PRODUCT_REQUIREMENTS.md` 仍为模板，待后续同步。

| 需求编号 | 需求名称 | 设计文档 | 代码模块 | 测试用例 | 验收项 | 状态 |
| --- | --- | --- | --- | --- | --- | --- |
| BASE-01 | 底座系统版本升级 | `docs/01-requirements/需求文档.md` 3.2；`docs/02-design/设计文档.md` 3.3.1 | `src/kubernetes-manifests/`、云端打包相关模块 TODO | TC-SCN-001, TC-SCN-002 | 多 OS/架构兼容矩阵、部署包拆分、旧系统兼容 | 已设计测试 |
| BASE-02 | Bitnami 闭源中间件替代 | `docs/01-requirements/需求文档.md` 3.3；`docs/02-design/设计文档.md` 3.3.2 | `src/kubernetes-manifests/`、中间件部署脚本 TODO | TC-SCN-003, TC-ERR-001 | 官方二进制部署、校验值、旧系统过渡 | 已设计测试 |
| BASE-03 | Kubernetes 虚拟化能力 | `docs/01-requirements/需求文档.md` 3.4 | `src/empoworx-kubea/controller/vm.go`、`src/empoworx-kubea/service/vm.go` | TC-SCN-004, TC-AUTH-001 | 授权开启、VM 创建、状态跟踪、控制台可用 | 已设计测试 |
| PIPE-01 | 云端打包系统拆分与优化 | `docs/01-requirements/需求文档.md` 3.5；`docs/02-design/设计文档.md` 3.3.1 | 云端打包、Jenkins、制品目录相关模块 TODO | TC-SCN-005, TC-ERR-002, TC-PERF-001 | 最小首包、按需组件、前置依赖分析、制品校验 | 已设计测试 |
| PIPE-02 | 中间件模块化管理 | `docs/01-requirements/需求文档.md` 3.6；`docs/02-design/设计文档.md` 3.1.1、3.2.1 | PDM0660/PDM0611/PDM0620/PDM0311 相关模块 TODO | TC-SCN-006, TC-ERR-003, TC-SCN-007, TC-REG-001 | 模块登记、构建发布、云端通知、版本展示 | 已设计测试 |
| PIPE-03 | 流水线磁盘资源优化 | `docs/01-requirements/需求文档.md` 3.7；`docs/02-design/设计文档.md` 3.1.2、3.2.2 | PDM0620 磁盘告警、构建节点定时任务 TODO | TC-SCN-008, TC-SCN-009 | 阈值预警、企业微信通知、定时清理 | 已设计测试 |
| PIPE-04 | 项目资源评估 | `docs/01-requirements/需求文档.md` 3.8；`docs/02-design/设计文档.md` 3.1.3 | 构建计划产物配置、项目登记资源推荐 TODO | TC-SCN-010 | 推荐资源维护、项目汇总、默认中间件资源 | 已设计测试 |
| GOV-01 | 优雅上下线 | `docs/01-requirements/需求文档.md` 3.9；`docs/02-design/设计文档.md` 3.1.4、3.2.3 | `src/syncplant-auto-deployment/services/kubea_graceful.go`、`src/empoworx-kubea/controller/graceful.go` | TC-SCN-011, TC-ERR-004, TC-SCN-012, TC-REG-002 | Pod 上下线、Deployment 优雅重启、失败保护、审计 | 已设计测试 |
| GOV-02 | API 管控 | `docs/01-requirements/需求文档.md` 3.10；`docs/02-design/设计文档.md` 3.1.5、3.2.4 | ApiControlController/ApiAssetService/ApiMetricQueryService TODO | TC-SCN-013, TC-SCN-014, TC-SCN-015, TC-PERF-002 | 接口资产、指标聚合、监控开关、趋势分析 | 已设计测试 |
| GOV-03 | 限流、熔断降级 | `docs/01-requirements/需求文档.md` 3.11；`docs/02-design/设计文档.md` 3.1.6、3.2.5 | FlowLimitController、BreakerControlController、SentinelRuleService TODO | TC-SCN-016, TC-ERR-005, TC-ERR-006, TC-SCN-017, TC-SCN-018 | QPS 限流、Nacos 发布、手动熔断、批量启停 | 已设计测试 |
| GOV-04 | 灰度发布 | `docs/01-requirements/需求文档.md` 3.12 | 服务部署、灰度规则配置、微服务基础平台灰度能力 TODO | TC-SCN-019, TC-ERR-007, TC-SCN-020, TC-SCN-021, TC-PERF-003 | 灰度策略、版本分布、暂停继续、回退、性能影响 | 已设计测试 |
| GOV-05 | 第三方应用部署 | `docs/01-requirements/需求文档.md` 3.13；`docs/02-design/设计文档.md` 3.1.7、3.2.6 | ThirdAppController/ThirdAppPackageService/ThirdAppTaskService TODO | TC-SCN-022, TC-SEC-001, TC-SCN-023, TC-SCN-024, TC-ERR-008, TC-SCN-025 | 上传解析、安全校验、部署进度、日志、重启卸载 | 已设计测试 |
| PERF-01~PERF-05 | 非功能性能要求 | `docs/01-requirements/需求文档.md` 4.1 | 各功能相关模块 | TC-PERF-001, TC-PERF-002, TC-PERF-003 | 性能基线、指标聚合、灰度性能影响 | 已设计测试 |
| SEC-01 | 安全及保密要求 | `docs/01-requirements/需求文档.md` 4.2 | 权限、审计、Nacos、第三方包校验相关模块 | TC-SEC-001, TC-SEC-002, TC-SEC-003 | 权限控制、二次确认、敏感信息脱敏、安全基线 | 已设计测试 |
