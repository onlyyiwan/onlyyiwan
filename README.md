<div align="center">

AI 全栈工程师

[changwanyi53@gmail.com](mailto:changwanyi53@gmail.com) · China · Beijing

</div>

---

别人造梯子是为了够着东西，我造梯子是为了爬进去——银行、医院、水务局，这些你以为进不去的地方。

十几个从 0 到 1 的大模型生产系统，没有一个是靠 Demo 糊弄过去的——这些行业但凡出错一次就是大新闻，
容错率比谁都低。前端、后端、数据检索、模型层，一个人全扛。

模型两年一换代，这套能让模型在生产里站住脚的工程能力，不会跟着过时。

<details>
<summary>EN</summary>
<br>

Others build ladders to reach things. I build ladders to climb in — banking, hospitals, water
utilities, the places you'd assume nobody gets into.

A dozen+ LLM systems shipped from zero to production, and none of them got there on a demo's charm —
these are industries where one mistake makes headlines, zero tolerance for error. Frontend, backend,
data & retrieval, model layer: one person running the whole stack.

Models get replaced every couple of years. The engineering that keeps one standing up in production
doesn't.

</details>

---

### 工程亮点

- 用 **Celery chord** 把 PDF 按页拆分并行 OCR 再聚合落盘，而不是单纯堆队列
- RAG 的引用能定位到 **原文 PDF 页码**，不是只给个文件名
- 外呼系统适配两家供应商的协议语义差异，处理 **用户打断（barge-in）** 的边界情况
- 基于 **Neo4j 向量索引** 做 MCP 知识图谱记忆服务
- **Redis 分布式锁**实现多 worker 定时任务选主与故障自动转移

---

### 技术栈

<div align="center">
<img src="https://skillicons.dev/icons?i=python,go,ts,fastapi,vue,redis,mysql,postgres,elasticsearch,docker,nginx,linux" alt="tech stack icons" />
</div>

模型层：**DeepSeek / Qwen / GPT** 统一编排 · 检索：**Milvus** 向量 + **Neo4j** 图谱 · 文档：**PaddleOCR** · 任务：**Celery** · 集成：**MCP**

组合方式：FastAPI 出 API，Celery 扛长任务，Docker Compose 打包，离线也能跑。

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
