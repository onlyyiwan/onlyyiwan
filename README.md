### Hi，我是 Yiwan

常驻北京。

邮箱 [changwanyi53@gmail.com](mailto:changwanyi53@gmail.com) ·
[博客园](https://www.cnblogs.com/changwan) ·
[掘金](https://juejin.cn/user/2663443925044906) ·
[CSDN](https://blog.csdn.net/m0_73848096)

---

### 一点看法

一个 AI 项目里，真正和模型直接相关的代码可能不到两成。剩下八成是：数据怎么进来、结果怎么验、
失败了怎么兜、权限怎么管、断网了还跑不跑。这八成不写，Demo 永远只是 Demo。

Demo 三天能跑通，进生产要三个月——差的从来不是模型能力，是中间这段没人愿意干的脏活。
我干的就是这段。

<details>
<summary>EN</summary>
<br>

In an AI project, maybe 20% of the code actually touches the model. The other 80% is: how data gets
in, how results get verified, what happens when it fails, who's allowed to do what, and whether it
still runs with the network cable pulled. Skip that 80% and the demo stays a demo.

A demo takes three days; production takes three months. The gap was never model capability — it's
the unglamorous work in between. That's the part I do.

</details>

---

### 技术栈

<div align="center">
<img src="https://skillicons.dev/icons?i=python,go,ts,fastapi,vue,redis,mysql,postgres,elasticsearch,docker,nginx,linux" alt="tech stack" />
</div>

| | |
| :-- | :-- |
| **语言** | Python · Go · TypeScript · Shell |
| **后端** | FastAPI 全异步 · SQLAlchemy 2.0 Async · Alembic · Celery · APScheduler · Gin |
| **前端** | Vue 3 · Vite · Pinia · Element Plus |
| **数据** | MySQL / PostgreSQL · Redis · Elasticsearch 全文 · Milvus 向量 · Neo4j 图谱 · MinIO 对象 |
| **模型** | DeepSeek / Qwen / GPT 统一编排（容灾 + 限流）· PaddleOCR PPStructureV3 |
| **交付** | Docker Compose · Nginx · GitHub Actions — 客户现场多为离线内网，整套要能断网独立跑 |

---

### 主要做什么

**智能外呼**

电话机器人与大模型对话编排，适配不同供应商的协议差异（SSE 累积式 / OpenAI 兼容增量式），
处理用户打断（barge-in）的上下文标记与流式输出中控制 token 被截断的边界情况，多租户隔离部署。

**智能文档**

PaddleOCR PPStructureV3 做版面结构识别，配合视觉模型理解嵌入图像；Celery chord 按页拆分并行
处理再聚合落盘；Redis Stream 推送实时进度，断线靠 last_id 续传。检索结果能定位到原文页码。

**RAG 知识库**

Milvus 向量检索 + 混合召回 + 语义重排，服务企业内部知识问答。答案有依据可追溯，不是模型瞎编。

**MCP 能力扩展**

给大模型接外部工具与知识图谱，基于 Neo4j 原生向量索引做长期记忆服务；多厂商 LLM 响应归一化层，
处理 finish_reason 映射、tool_calls 序列化、content blocks 展平这类兼容性问题。

**中台底座**

OAuth2 + JWT + RBAC 三级权限（菜单 / 按钮 / 数据范围）；Redis 分布式锁做多实例定时任务选主与
故障自动转移；Redis Streams 消费组构建带去重和悬挂消息认领的异步审计日志管道。

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
