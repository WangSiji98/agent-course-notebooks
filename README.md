# Agent Course Notebooks

从零开始学习如何构建 LLM Agent（大模型智能体）——前期**不借助任何框架**（不用 LangChain / LlamaIndex / smolagents），用最朴素的 Python + OpenAI 兼容 API 把原理弄清楚；后期再接入 AWS Bedrock 搭生产级 Agent。

## 课程线路图

### Phase 1 — 从零手搓（no framework）
- 01 — 什么是 Agent：与直接调 LLM 的区别，ReAct 循环
- 02 — Tool Use 的底层协议（OpenAI function calling / JSON schema）
- 03 — 手写一个 ReAct Agent（Thought → Action → Observation 循环）
- 04 — 多工具 + 工具路由
- 05 — Agent 的记忆：短期 vs 长期
- 06 — Planning：任务分解与 Plan-and-Execute
- 07 — 自反思 (Reflection) 与错误恢复
- 08 — Multi-Agent 协作（Manager / Worker 模式）
- 09 — 评测一个 Agent：成功率、步数、成本
- 10 — 安全与 Guardrails：不让 Agent 失控

### Phase 2 — 框架与生产（AWS Bedrock）
- 11 — 主流框架全景：LangGraph / smolagents / AutoGen 对比
- 12 — Bedrock Converse API + Tool Use（手搓版的 AWS 对应物）
- 13 — Bedrock Agents（托管）：Agent / Version / Alias / Trace
- 14 — Action Groups：给托管 Agent 装"手"（Function Schema + Lambda）
- 15 — Knowledge Bases：托管 RAG，挂给 Agent 或直接 query
- 16+ — Guardrails、Memory、观测、Multi-agent、成本调优（待写）

## 环境

- Python 3.11（conda env 名：`agent`）
- 本地 LLM：LM Studio @ `http://10.0.0.63:1234/v1`（OpenAI 兼容，Qwen 3.6 35b）
- 主要依赖：`openai`、`requests`、`pydantic`、`rich`、`ipykernel`、`jupyter`

## 学习方式

每节课是一个独立的 notebook，**从头到尾能跑**。先读讲解，再跑代码，再看输出里模型的 Thought / Action 字段。
