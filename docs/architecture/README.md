# 研发 AI 数字员工架构索引

> **作者：** ernestfei  
> **完整规格：** [../superpowers/specs/2026-09-14-ai-digital-employee-design.md](../superpowers/specs/2026-09-14-ai-digital-employee-design.md)

本目录是导航层。设计决策、岗位定义、知识织物、工具治理与分期均以完整规格为准。

## 一句话

以 **AgentScope 2.0 Agent Service** 为数字员工操作系统内核：岗位是 Workspace 模板，能力是 Skill + MCP + Tool Group，知识是 RAG Service + OpenSearch 混合检索，治理是 Permission / HITL / 评测 / 审计。

## 推荐路线

不要做单超级助手，也不要做互相孤立的知识机器人 / 代码机器人。目标态是 **岗位化多数字员工 + Lead 调度**。

## 分层

```text
交互面  IDE / IM / MR / 工单 / Web
   ↓
网关    SSO · 路由 · Session · SSE/A2A/AG-UI
   ↓
内核    AgentScope 2.0 ReAct · Middleware · Team · Plan · Permission
   ↓
能力    Toolkit · Skill Hub · MCP Hub · Workspace/Sandbox
   ↓
知识    RAG Service（小库）+ OpenSearch 混合检索（组织级）+ ReMe 记忆
   ↓
系统    Git · CI · Wiki · 需求 · 观测 · 安全
   ↓
治理    审计 · 评测 · 配额 · 技能晋升 · HITL
```

## 预置岗位

| ID | 岗位 |
| --- | --- |
| `de.lead` | 调度官 |
| `de.biz` | 业务分析（业务 AI） |
| `de.arch` | 架构 |
| `de.code` | 编码 |
| `de.review` | 评审 |
| `de.qa` | 质量 |
| `de.sre` | 发布与排障 |
| `de.kb` | 知识管家 |
| `de.sec` | 安全合规 |

## 建设顺序

0. 内核 + 只读知识问答  
1. 组织级知识织物 + MR 预审  
2. 业务 AI（BizBrief）+ 沙箱编码  
3. 质量 / 发布 / 安全  
4. 团队协作与受控自进化  

## 子系统拆分

完整规格第 16 节。每个子系统独立 Spec → Plan → 实现，禁止一份计划打穿全平台。
