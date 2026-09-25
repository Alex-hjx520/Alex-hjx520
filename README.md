![img](https://user-images.githubusercontent.com/74038190/225813708-98b745f2-7d22-48cf-9150-083f1b00d6c9.gif)

# Hi there 👋, I'm Alex!

### 🚀 Java 后端开发工程师 | 2027 届应届生
> 正在备战 2026 秋招，寻找 Java 后端开发岗位。热衷于高并发架构、性能优化与 AI Agent 落地实践。

---

### 🛠️ 技术栈 (Tech Stack)

**后端开发**
![Java](https://img.shields.io/badge/-Java-007396?style=flat-square&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/-Spring%20Boot-6DB33F?style=flat-square&logo=spring-boot&logoColor=white)
![MyBatis](https://img.shields.io/badge/-MyBatis-000000?style=flat-square)
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)

**数据库与中间件**
![MySQL](https://img.shields.io/badge/-MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/-Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![JWT](https://img.shields.io/badge/-JWT-000000?style=flat-square&logo=json-web-tokens&logoColor=white)

**AI 与 Agent**
![LangChain](https://img.shields.io/badge/-LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/-LangGraph-1C3C3C?style=flat-square)
![RAG](https://img.shields.io/badge/-RAG-4B8BBE?style=flat-square)
![ChromaDB](https://img.shields.io/badge/-ChromaDB-FF6F61?style=flat-square)

---

### 💡 核心项目 (Featured Projects)

#### 🏭 空调工单管理平台
`Java / Spring Boot / MySQL / Vue`

- 面向国企场景的工单管理平台，支撑 7 节点审批流（派单至完成）。
- 利用 `synchronized` + 事务机制解决并发流转问题，基于 JWT + Redis + RBAC 实现多端安全隔离与动态权限。
- 自建线程池结合 EasyExcel 实现报表异步导出，避免阻塞主流程。

#### 🔋 建筑能耗预测仿真平台
`Python / FastAPI / NumPy`

- 负责基于物理模型的能耗仿真接口开发与数据归档。
- 通过 NumPy 向量化优化，将全年 8760 小时逐时仿真耗时压缩至 **2.5s 以内**。

#### 🔧 [基于 Agent 的冷凝阀门仿真选型软件](https://github.com/Alex-hjx520/-agent-) `2026.08 - 2026.10`
`Python / FastAPI / LangChain / LangGraph / RAG / ChromaDB / CoolProp / MySQL / Vue3`

- 主导系统整体架构设计与核心开发，基于 LangGraph 构建“需求解析—多源检索—候选初选—批量仿真—Agent 调优—报告生成”的完整智能决策业务闭环。
- 基于 BGE 中文向量模型与 ChromaDB 搭建制冷设备 RAG 知识库，融合本地 PDF、MySQL 参数库、限定域名及全网搜索，实现候选型号去重与参数回填。
- 利用 CoolProp 实现制冷剂物性、焓差、质量流量及制冷量计算；针对 RFKH 热力膨胀阀实现多制冷剂容量扩展表、过冷度修正和压降修正算法。
- 基于 LangGraph 实现 Agent 闭环决策，对最多 5 个候选设备进行批量仿真，自动执行调节阀前压差、过冷度、过热度或换型等操作，直至满足达标数量或达到最大迭代次数。

#### ⚖️ [LCR-Agent · 法律合同审查 Agent](https://github.com/Alex-hjx520/LCR-Agent) `2026.08 - 2026.10`
`Python / LangGraph / FastAPI / Pydantic v2 / Chroma / BM25 / RAG`

- 主导系统架构设计与核心开发，基于 LangGraph 将合同审查链路拆解为「解析 → 切分 → 条款抽取 → 风险审查 → 合规检查 → 摘要 → 报告」的有状态图，每个节点均可独立测试与替换。
- 采用**规则先行、LLM 兜底**策略：正则定位条款边界保证不丢不越界，LLM 负责分类，模型不可用时自动回退关键词规则；合规检查由确定性正则引擎完成，可复现、可审计。
- 搭建 **BM25 + Chroma 混合检索**，用 RRF 融合稀疏与稠密召回，接入 CUAD 先例语料，为每条风险结论写入可回溯的 `citations`。
- 设计分层解耦架构（`schemas ← parsing ← knowledge ← agents ← graph ← api`）与无状态 Agent 签名 `run(state) -> dict`，支持单测、重放、并行及 HITL 人机协同。
- 工程化落地：Poetry + ruff + mypy + pytest，提供 CLI 与 FastAPI 全套接口，未配置密钥时自动降级为离线 stub，可先跑通全链路。
---

### 📊 GitHub 统计 (GitHub Stats)

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Alex-hjx520&theme=radical" alt="GitHub Streak" />
</div>

---

### 📫 联系我 (Connect with me)

- 📧 Email: 2861902988@qq.com
- 💼 求职状态：**正在寻找 Java 后端开发岗位（秋招）**
