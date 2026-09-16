# 研发 AI 数字员工架构索引

> **作者：** ernestfei  
> **现行计划：** [../superpowers/plans/2026-09-14-rd-digital-employee-product.md](../superpowers/plans/2026-09-14-rd-digital-employee-product.md)  
> **早期规格：** [../superpowers/specs/2026-09-14-ai-digital-employee-design.md](../superpowers/specs/2026-09-14-ai-digital-employee-design.md)（其中 Python 内核假设已作废）

本目录是导航层。业务功能与拓扑以**产品计划**为准。

## 一句话

底层 AI 基座 **只使用 AgentScope Java 2.0**（`ReActAgent` + `HarnessAgent`），不是 Python 版。岗位、任务、工作流、知识、审批叠在这套 Java 底座上。

## 推荐路线

不要做单超级助手，也不要做互相孤立的知识机器人 / 代码机器人。目标态是 **岗位化多数字员工 + 工作台状态 + 可复用工作流**。

## 分层

```text
入口    桌面（本地/云端） / 浏览器（仅云端）
   ↓
八模块  工作台 · 数字员工 · 工作区 · 知识 · 技能与工具 · 工作流 · 审批 · 设置
   ↓
运行    员工实例 · 任务（独立/协同/工作流运行） · 审批单
   ↓
底座    AgentScope Java 2.0 HarnessAgent / ReActAgent（非 Python）
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
