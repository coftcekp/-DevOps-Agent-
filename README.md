# Enterprise DevOps Agent Cluster 🚀
> 基于大语言模型 (LLM) 驱动的云原生与 IT 基础设施自动化排障多 Agent 平台。

## 🎯 核心架构 (Core Architecture)
本项目专为复杂的虚拟化环境（如 openEuler, CentOS 集群）设计，采用多智能体协同架构：
* **Diagnostic Agent (诊断规划)**: 基于长链推理 (CoT) 动态拆解网络告警，下发连通性测试与配置扫描。
* **Decision Agent (决策引擎)**: 聚合多维观测数据（路由表、防火墙规则、端口状态），精准定位 Root Cause。
* **Fix Agent (修复与验证)**: 自动生成并安全执行 Bash/Python 修复脚本，并在修复后进行闭环连通性验证。

## 🔒 声明 (Notice)
由于本项目深度耦合公司内部网络拓扑与 Kubernetes 集群敏感配置，当前公开仓库仅提供 **核心 Agent 调度逻辑 (Core Logic Engine)** 与 **Prompt 框架** 的脱敏演示版本 (`agent_core.py`)。
完整业务代码及编排文件受公司安全合规限制，暂不开源。

## 🛠️ 技术栈 (Tech Stack)
- LLM: OpenAI / DeepSeek API (推理核心)
- Agent Framework: 自研多智能体路由框架
- OS/Env: openEuler, KVM, Firewalld, iptables
