<div align="center">

AI 全栈工程师

[changwanyi53@gmail.com](mailto:changwanyi53@gmail.com) · China · Beijing

</div>

---

AI 全栈工程师，独立交付过十几个从 0 到 1 的大模型生产系统。关于"AI 会不会让程序员失业"这个问题，
我的判断很明确：会淘汰的是只会写代码、不理解系统运行方式的人；不会淘汰的，是能把一个东西从能跑的
Demo 做成能扛生产流量、能经得起审计的系统的人。Codex、Copilot 这类工具把"写代码"这件事的门槛拉到
了地板，但同一个工具在不同人手里产出的系统质量天差地别——差的从来不是会不会用工具，是工程判断力。
我没有去训练模型，我把精力放在让模型在真实业务里活下来、不翻车的那一层：重试机制、权限边界、失败
兜底、数据合规。这是模型本身解决不了的问题，也是接下来几年不会被 AI 自己替代的工作。

<details>
<summary>EN</summary>
<br>

AI full-stack engineer. I've independently shipped a dozen+ LLM systems from zero to production.
On whether AI will put programmers out of work: my view is that it will replace people who can
only write code without understanding how systems run — not people who can take something from a
working demo to a system that holds up under production traffic and survives an audit. Codex and
Copilot have dropped the floor on "writing code," but the same tool produces wildly different
systems depending on who's holding it — the gap is engineering judgment, not tool proficiency. I
don't train models; I spend my time on the layer that keeps a model alive in real business use:
retries, permission boundaries, failure fallbacks, data compliance. That's a problem the model
itself doesn't solve, and it's not getting automated away anytime soon.

</details>

---

### 技术栈

<div align="center">
<img src="https://skillicons.dev/icons?i=python,go,ts,fastapi,vue,redis,mysql,postgres,elasticsearch,docker,nginx,linux" alt="tech stack icons" />
</div>

语言主要用 Python 和 Go，前端 TypeScript + Vue 3，脚本和部署用 Shell。后端框架是 FastAPI，全异步，
配 SQLAlchemy 2.0 Async 做 ORM，Alembic 管迁移；长任务和异步编排交给 Celery，调度用 APScheduler；
偶尔需要高并发场景会上 Go 的 Gin。前端用 Vue 3 + Vite + Pinia + Element Plus 出中后台界面。数据层：
MySQL / PostgreSQL 存业务数据，Redis 做缓存和分布式锁，Elasticsearch 做全文检索，Milvus 做向量检索，
Neo4j 存知识图谱，MinIO 存文件对象。模型层接 DeepSeek、Qwen、GPT，统一走一层编排，做容灾和限流；
文档解析用 PaddleOCR 的 PPStructureV3 做版面结构化。交付链路是 Docker + Docker Compose 打包，Nginx
做反向代理，GitHub Actions 做 CI/CD——大部分客户现场是离线内网环境，整套服务要能在没有互联网的机器
上独立跑起来。

---

### 业务侧

**智能外呼**：电话机器人与大模型对话编排，适配不同外呼供应商的协议差异，处理用户打断（barge-in）
等边界情况，支持多租户隔离部署。

**智能文档**：多模态文档解析，PaddleOCR 做版面结构识别，配合视觉模型理解嵌入图像；用 Celery chord
按页拆分并行处理再聚合；检索结果能定位到原文具体页码，不是只给文件名。

**RAG**：向量检索 + 混合召回 + 语义重排，服务企业内部知识问答，答案有依据可追溯，不是模型瞎编。

**MCP**：给大模型接外部工具和知识图谱做能力扩展，基于 Neo4j 做过向量索引的长期记忆服务。

**中台搭建**：OAuth2 + JWT + RBAC 三级权限体系，Redis 分布式锁做多实例定时任务选主和故障转移，
Redis Streams 做异步审计日志管道。

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

- **[repo-name](https://github.com/onlyyiwan/repo-name)** <a href="https://github.com/onlyyiwan/repo-name"><img src="https://img.shields.io/github/stars/onlyyiwan/repo-name?style=social" alt="stars" height="16"></a> — 一句话说明它是什么、解决什么
-->

<!--
  ═══════════════════════════════════════════════════════════════
  待解锁区块 B：贡献上游
  启用条件：有 PR 被上游合并后。只列真实合并过的项目，fork 不算贡献。
  ═══════════════════════════════════════════════════════════════

### 贡献

- **[FastAPI-RuoYi-Vue3](https://github.com/insistence/FastAPI-RuoYi-Vue3)** <a href="https://github.com/insistence/FastAPI-RuoYi-Vue3"><img src="https://img.shields.io/github/stars/insistence/FastAPI-RuoYi-Vue3?style=social" alt="stars" height="16"></a> — 若依体系的 FastAPI 实现
-->
