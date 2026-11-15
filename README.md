# 👋 Hi, I'm Alex

**Java 后端开发工程师 | 2027 届应届生**

正在备战 2026 秋招，寻找 Java 后端开发岗位。有国企空调服务平台后端研发实习经历，关注工单流转与并发控制、缓存优化、能耗仿真策略与 AI Agent 落地实践。

---

### 🛠️ 技术栈

- **后端开发**：Java · Spring Boot · MyBatis · Spring Task · Spring Cache · AOP · WebSocket · JWT · Python · FastAPI
- **数据库与中间件**：MySQL · Redis
- **AI 与 Agent**：LangChain · LangGraph · RAG · ChromaDB
- **工程化与工具**：Git · AI Coding

---

### 💡 核心项目

> 点击标题展开项目详情

<br/>

<details>
  <summary><b>🏭 空调工单服务平台（国企甲方项目）</b> ｜ <code>Java / Spring Boot / MySQL</code></summary>
  <br/>

  - 负责工单流程模块后端研发，深度参与甲方需求评审与业务规则梳理。
  - 研发基于配置表的通用审批流引擎，支撑派单、转派、回退、办结等 10+ 流转操作，单引擎复用驱动维修与巡检两条业务线。
  - 采用「节点权重乐观校验 + 关键方法单机加锁 + 同节点冗余待办清除」三层机制，缓解工单多人同时办理时的重复接单与重复审批问题。
</details>

<br/>

<details>
  <summary><b>🔋 建筑能耗预测仿真平台</b> ｜ <code>Python / FastAPI / NumPy</code></summary>
  <br/>

  - 参与仿真软件研发，参与设计 8760 小时仿真引擎、群控/MPC 控制策略模块的全流程开发。
  - 物理设备性能算法：建立冷水机组/水泵/冷却塔物理建模，根据湿球温度、冷负荷等参数为仿真引擎提供冷水机组/水泵/冷却塔风机的功率计算。
  - 仿真引擎策略算法：为实现系统综合能效优化，实现简单加减机、群控优化（枚举 2^N-1 台数组合寻优）及 MPC 预测控制（动态规划求解含分时电价与启停惩罚的滚动优化）。
</details>

<br/>

<details>
  <summary><b>🍜 餐饮商户外卖平台</b> ｜ <code>Java / Spring Boot / Redis / WebSocket</code></summary>
  <br/>

  - 项目背景：小型商户外卖平台服务于线下餐饮品牌，由微信小程序用户端与商家后台管理端组成。
  - C 端/B 端登录与身份验证：使用 JWT 生成令牌，配合拦截器进行身份拦截，ThreadLocal 实现用户身份的无侵入式上下文传递。
  - AOP 实现公共字段自动填充：针对频繁更新的公共字段，利用自定义注解结合 AOP 切面编程，在方法执行前实现数据自动填充。
  - WebSocket 实现来单提醒；利用 Spring Task 定时任务实现订单超时处理，超时自动取消订单。
  - 针对 C 端菜单读多写少场景，使用 Redis + Spring Cache 缓存菜品与套餐数据，写操作触发缓存失效，降低数据库读压力。
</details>

<br/>

<details>
  <summary><b>🔧 基于 Agent 的冷凝阀门仿真选型软件</b> ｜ <code>Python / LangGraph / RAG</code></summary>
  <br/>

  🔗 **源码**：[https://github.com/Alex-hjx520/-agent-](https://github.com/Alex-hjx520/-agent-)

  - 主导系统整体架构设计与核心开发，基于 LangGraph 构建“需求解析—多源检索—候选初选—批量仿真—Agent 调优—报告生成”的智能决策业务闭环。
  - 基于 BGE 中文向量模型与 ChromaDB 搭建制冷设备 RAG 知识库，融合本地 PDF、MySQL 参数库及全网搜索，实现候选型号去重与参数回填。
  - 利用 CoolProp 实现制冷剂物性、焓差、质量流量及制冷量计算；针对 RFKH 热力膨胀阀实现多制冷剂容量扩展表、过冷度修正和压降修正算法。
  - 基于 LangGraph 实现 Agent 闭环决策，对最多 5 个候选设备进行批量仿真，自动执行调节阀前压差、过冷度、过热度或换型等操作，直至达标。
</details>

<br/>

<details>
  <summary><b>⚖️ LCR-Agent · 法律合同审查 Agent</b> ｜ <code>Python / LangGraph / BM25</code></summary>
  <br/>

  🔗 **源码**：[https://github.com/Alex-hjx520/LCR-Agent](https://github.com/Alex-hjx520/LCR-Agent)

  - 基于 LangGraph 将审查链路拆解为「解析 → 切分 → 抽取 → 审查 → 合规检查 → 摘要 → 报告」的有状态图，节点可独立测试与替换。
  - 采用规则先行、LLM 兜底策略：正则定位边界，LLM 负责分类，模型不可用时自动回退；合规检查由确定性正则引擎完成，可复现可审计。
  - 搭建 BM25 + Chroma 混合检索，用 RRF 融合稀疏与稠密召回，为每条风险结论写入可回溯的 `citations`。
  - 设计分层解耦架构与无状态 Agent 签名 `run(state) -> dict`，支持单测、重放、并行及 HITL 人机协同。
  - 工程化落地：Poetry + ruff + mypy + pytest，提供 CLI 与 FastAPI 全套接口，未配置密钥时自动降级为离线 stub。
</details>

---

### 📊 GitHub 统计

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Alex-520hjx&show_icons=true&theme=transparent&hide_border=true&count_private=true" alt="Alex's GitHub stats" />
</p>

---

### 📫 联系我

- 📧 **Email**: 2861902988@qq.com
- 💼 **求职状态**：正在寻找 Java 后端开发岗位（秋招）
