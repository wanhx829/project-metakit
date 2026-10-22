# 04-testing 测试与质量保障中心

本目录归档端到端全链路测试规范、分级测试用例库以及自动化回归测试报告。

---

## 1. 用户视角与全栈用例矩阵 (核心索引)

| 测试用例库文档 | 测试视角与层级 | 核心覆盖范围 | 驱动工具链 |
| :--- | :--- | :--- | :--- |
| **[用户界面与体验(UI-UX)端到端全量测试用例库](file:///mnt/d/wsl/workspace/autoDevV3.0/docs/04-testing/2026-10-22-用户界面与体验(UI-UX)端到端全量测试用例库.md)** | **前端用户视角**<br>(第一公民) | 传输工具、运维控制台、微服务门户三大界面：加载渲染、表单交互、Loading反馈、防误触Modal、Drawer日志、表格分页 | `agent-browser`<br>(无头浏览器/Playwright) |
| **[自动化装机与底层脚本测试用例库](file:///mnt/d/wsl/workspace/autoDevV3.0/docs/04-testing/2026-10-22-自动化装机与底层脚本测试用例库.md)** | **基础底座视角**<br>(L0 ~ L1) | IP Ping 连通性门禁拦截、PXE 网络无人值守装机、SSH 22 连通、OS 内核基线、Local Registry 镜像仓库 | Bash / SSH / MCP |
| **[微服务与服务治理-测试项与场景用例库](file:///mnt/d/wsl/workspace/autoDevV3.0/docs/04-testing/2026-10-21-微服务与服务治理-测试项与场景用例库.md)** | **微服务业务视角**<br>(L3 ~ L4) | 网关路由转发、Nacos 动态注册发现、OAuth2 鉴权中心、Sentinel 限流熔断策略 | HTTP API / Python 探针 |
| **[自动化运维传输工具-测试项与场景用例库](file:///mnt/d/wsl/workspace/autoDevV3.0/docs/04-testing/2026-10-21-自动化运维传输工具-测试项与场景用例库.md)** | **网闸摆渡视角**<br>(隔离网传输) | 硬件 MAC 码鉴权、云端大文件断点续传（下载/推送）、MD5 完整性校验 | Local API / WS |

---

## 2. 验收与实测报告归档

- `docs/05-acceptance/2026-10-21-测试环境初次部署端到端闭环验收报告.md`
- `docs/05-acceptance/2026-10-22-微服务基础平台最新版部署验收报告.md`
- `docs/04-testing/2026-10-22-运维控制台与微服务产品横向功能测试全景报告.md`
- `docs/04-testing/2026-10-22-微服务平台与控制台纵向深度下钻探测报告.md`
