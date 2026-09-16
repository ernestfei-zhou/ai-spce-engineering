# AI Space Engineering

研发部门 AI 数字员工与效能工程仓库。

当前交付物是架构规格，不是可运行服务。

## 架构规格

- 产品功能计划（现行）：[docs/superpowers/plans/2026-09-14-rd-digital-employee-product.md](docs/superpowers/plans/2026-09-14-rd-digital-employee-product.md)
- 早期规格（基座段落已作废说明）：[docs/superpowers/specs/2026-09-14-ai-digital-employee-design.md](docs/superpowers/specs/2026-09-14-ai-digital-employee-design.md)
- 分层索引：[docs/architecture/README.md](docs/architecture/README.md)

## 基座

**仅使用 AgentScope Java 2.0**（`ReActAgent` + `HarnessAgent`）作为 AI 运行时底座。

- 文档：[Harness 架构](https://java.agentscope.io/v2/zh/docs/harness/architecture.html)
- **不使用** [AgentScope Python 2.0](https://docs.agentscope.io/stable/en/index) 作为内核，不做 Python/Java 双栈推理。

## 作者

署名统一为 **ernestfei**（代码 `@author ernestfei`，文档 `作者：ernestfei`）。约定见 `.cursor/rules/authorship.mdc`。
