# 领域术语表 (Domain Glossary)

本术语表定义了自动化运维与交付体系（AutoDev）各组件通用的核心概念与术语。AI 助手与研发/测试人员在编写需求、设计、用例及代码时，应严格遵循本表命名，避免使用未约定的同义词。

---

## 1. 系统与产品组件 (Systems & Components)

- **项目产品驾驶舱 (Product Cockpit)**：由“通用框架引擎”与“可插拔产品业务数据包”构成的智能协作中枢。通过人类输入业务知识领航，驱动 AI 探索产品、沉淀知识库，并执行端到端自动化测试与交付。
- **驾驶舱通用框架引擎 (Cockpit Framework Core)**：提供跨产品的元能力引擎，包含知识吸纳清洗、自然语言意图编排、测试用例自适应驱动、多协议执行适配器与闭环报告生成。
- **产品业务数据包 (Product Domain Pack)**：按标准规范组织的具体产品业务资产集合，包含该产品的 PRD 需求、接口契约、配置密码、拓扑结构与分级测试用例库。
- **运维平台项目产品驾驶舱 (Ops Platform Cockpit)**：挂载了运维交付体系（云端、传输工具、运维控制台、部署脚本）业务数据包的驾驶舱特化实例。
- **微服务基础平台驾驶舱 (Microservices Base Cockpit)**：挂载了微服务中台（网关、认证中心、平台服务、资源服务、前端门户）业务数据包的驾驶舱实例。
- **云端控制台 (Cloud Console)**：运行于云端或中心网络的运维管控母系统（如 `10.88.12.80:18880` / `devops.empoworx.net:13032`），负责项目规划、拓扑设计、软件模块编排、初次部署包生成与补丁发布。
- **自动化运维传输工具 (Implement Client / Transfer Tool)**：部署于物理隔离内外网边界机（如 Windows 便携终端 `:8880`）的网闸传输客户端，负责云端制品拉取、硬件 MAC 鉴权绑定、大文件断点续传推送至现场宿主机。
- **运维控制台 (Deployment Console / Auto-Deployment)**：部署于现场目标宿主机上的核心运维服务（Go Gin 单体 `:18880`），内嵌 SQLite 数据库，负责现场环境初始化引导、K8s/中间件纳管、微服务安装升级、Flyway 数据库版本迁移、限流熔断与告警治理。
- **底层部署与安装脚本 (Deploy & Bootstrapping Scripts)**：负责自动化交付的最底层逻辑，包括 PXE Kickstart 无人值守网络装机脚本、OS 内核基线调优脚本、容器运行时与 Cilium eBPF 初始化脚本、K8s 集群拉起脚本（`install.sh` / `start.sh`）。
- **微服务基础平台 (Microservices Base Platform)**：依托现场底座运行的业务中台组件，包含网关（`gateway`）、鉴权（`auth`）、前台门户（`web`）、系统平台（`system-pf`）、系统资源（`system-resource`）等核心服务。

---

## 2. 交付与运维概念 (Delivery & Operations Terms)

- **初次部署包 (Initial Deployment Package)**：云端针对特定项目生成的全量初始化压缩包（包含运维控制台二进制、K8s/Cilium 离线镜像、基础中间件离线镜像、初始化脚本）。
- **增量模块包 (Incremental Module Package)**：用于特定微服务或业务模块独立升级的轻量级介质包（包含服务 Docker 镜像、Flyway SQL 升级脚本、配置文件与版本元数据）。
- **硬件授权绑定 (Hardware MAC Binding)**：传输工具与云端通讯时，基于客户端网卡物理 MAC 地址的非对称签名授权机制。
- **服务上线 (Service Online)**：运维控制台解包模块介质、导入 Docker 镜像至本地 Registry（`:30500`）、执行 Flyway 数据表结构升级、更新 K8s Deployment/Service 并通过 Nacos 注册就绪的完整流程。
- **环境初始化状态 (isInitialization / deploymentInit)**：
  - `0`：未部署/未初始化；
  - `1`：控制台已安装完成但底座未初始化；
  - `2`：底座中间件已完成部署就绪。
- **Ping 连通性门禁 (IP Reachability Gate)**：装机前通过 ICMP 探测目标 IP，必须确保 100% 丢包（证明该 IP 未被局域网其他设备占用且电源处于待就绪状态）方可执行自动化 PXE 裸机安装。
