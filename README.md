<div align="center">

### 云梯 Yunti

AI 全栈工程师 · 一个人跑通大模型从 Demo 到生产的全链路

[changwanyi53@gmail.com](mailto:changwanyi53@gmail.com) · China · Beijing

</div>

---

十几个大模型生产系统，从 0 到 1 独立交付，覆盖银行、医疗、水务、能源这些最不能对出错宽容的行业。
前端、后端、数据与检索、模型层——一个人跑通全栈，不是只会调 API 的那种。

模型两年一换代，但让模型在生产里扛得住的那套工程能力——重试与降级、并发控制、状态一致性、
可观测性——不会跟着过时。这才是真正难的部分，也是我更在意的部分。

<details>
<summary>EN</summary>
<br>

AI full-stack engineer. I've independently shipped a dozen+ LLM systems from zero to production,
across industries with little tolerance for error — banking, healthcare, water utilities, energy.
Frontend, backend, data & retrieval, model layer: one person running the whole stack, not just
calling an API.

Models get replaced every couple of years. The engineering that keeps a model standing up in
production — retries, degradation, concurrency control, state consistency, observability — doesn't.
That's the hard part, and the part I actually care about.

</details>

---

### 工程实践

**文档智能与分布式任务编排**
- 用 Celery chord 实现 PDF 按页拆分并行 OCR 后聚合落盘的"动态裂变-聚合"任务编排
- 模型调用失败时在候选模型池中随机回退重试，做基础的多模型容灾降级
- Redis Stream（xadd / xread）做进度推送通道，断线靠 last_id 续传不丢进度

**RAG 与大模型应用工程**
- Milvus IVF_FLAT + COSINE 向量检索，答案引用能定位到原文 PDF 页码（按页切片生成可点击链接，而不只是给文件名）
- 用 Redis Lua 脚本实现会话级分布式锁 + 全局并发租约 + IP 限流的三层流控，支撑流式对话稳定性
- 客户端断连时把已生成的内容标记为 interrupted 并持久化，而不是直接丢弃

**智能外呼与实时语音交互**
- 用统一值对象适配两种外呼供应商协议（SSE 累积式 / OpenAI 兼容增量式），隔离协议语义差异
- 处理用户打断（barge-in）的上下文标记，以及流式输出中特殊控制 token 被截断的边界情况
- 多租户场景下的三层隔离：上下文注入 org_id、Service 签名强制携带、ORM 层自动追加租户条件
- 用"话术编译器"把可视化对话树渲染成缩进文本，让模型自己产出最终 system / user prompt，而不是直接拼模板

**MCP 生态与模型网关**
- 基于 Neo4j 原生向量索引做 MCP 知识图谱记忆服务（SSE transport + ContextVar 多租户鉴权）
- 手写多厂商 LLM 响应归一化层：finish_reason 映射、tool_calls 序列化、content blocks 展平、usage 字段补全、JSON Schema 清理，覆盖流式与非流式两条路径
- 从 Streamable HTTP + 统一网关迁移到更简单的 SSE 单一职责服务，踩过 Starlette 中间件在子应用挂载场景下的坑

**中后台基础设施**
- Redis 分布式锁实现多 worker 部署下的定时任务选主与故障自动转移
- Redis Streams 消费组构建带去重和悬挂消息认领的异步审计日志管道
- 自实现兼容 Quartz 语法（L / W / #）的 Cron 解析器

---

### 技术栈

语言用 Python、Go、TypeScript、Shell；后端 FastAPI + SQLAlchemy 2.0 Async + Alembic + Celery，调度配 APScheduler，偶尔上 Gin；前端 Vue 3 + Vite + Pinia + Element Plus。数据与检索层是 MySQL / PostgreSQL 存业务，Redis 做缓存与消息，Elasticsearch 和 Milvus 分管全文与向量检索，Neo4j 做知识图谱，MinIO 收文件。模型侧接 DeepSeek / Qwen / GPT，文档解析靠 PaddleOCR PPStructureV3，检索走 RAG 混合召回，系统集成靠 MCP。交付用 Docker + Nginx + GitHub Actions，以 Linux 为主，还有 CDP 驱动的浏览器自动化。

它们不是清单，实际项目里通常这样组合：FastAPI 出业务 API，SQLAlchemy 全异步读写，
Celery 跑文档解析这类长任务；Vue 3 + Element Plus 出中后台；
MySQL 存业务，Elasticsearch 和 Milvus 分管全文与向量检索，MinIO 收文件。
最后 Docker Compose 打包、Nginx 托管反代、Actions 做 CI 与 tag 发布 ——
交付到客户内网时，整套离线跑起来。

---

<div align="center">

工作机会、技术交流、合作，都欢迎邮件聊。

[changwanyi53@gmail.com](mailto:changwanyi53@gmail.com)

</div>

<!--
  ═══════════════════════════════════════════════════════════════
  待解锁区块 A：项目卡片
  启用条件：有可公开的原创项目后（首选 OcrPubSubWebsocket 脱敏开源）。
  星标徽章是实时的，会自动更新。
  ═══════════════════════════════════════════════════════════════

### 项目

- **[repo-name](https://github.com/yunti/repo-name)** <a href="https://github.com/yunti/repo-name"><img src="https://img.shields.io/github/stars/yunti/repo-name?style=social" alt="stars" height="16"></a> — 一句话说明它是什么、解决什么
-->

<!--
  ═══════════════════════════════════════════════════════════════
  待解锁区块 B：贡献上游
  启用条件：有 PR 被上游合并后。只列真实合并过的项目，fork 不算贡献。
  ═══════════════════════════════════════════════════════════════

### 贡献

- **[FastAPI-RuoYi-Vue3](https://github.com/insistence/FastAPI-RuoYi-Vue3)** <a href="https://github.com/insistence/FastAPI-RuoYi-Vue3"><img src="https://img.shields.io/github/stars/insistence/FastAPI-RuoYi-Vue3?style=social" alt="stars" height="16"></a> — 若依体系的 FastAPI 实现
-->
