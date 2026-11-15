# Java 后端开发工程师 | 2027 届应届生

<p align="center">
  <img src="https://readme-typing-svg.demolab.com/?font=Microsoft+YaHei&size=18&color=36BCF7&center=true&vCenter=true&width=800&height=35&lines=%E6%AD%A3%E5%9C%A8%E5%A4%87%E6%88%98+2026+%E7%A7%8B%E6%8B%9B%EF%BC%8C%E5%AF%BB%E6%89%BE+Java+%E5%90%8E%E7%AB%AF%E5%BC%80%E5%8F%91%E5%B2%97%E4%BD%8D%E3%80%82;%E6%9C%89%E5%9B%BD%E4%BC%81%E7%A9%BA%E8%B0%83%E6%9C%8D%E5%8A%A1%E5%B9%B3%E5%8F%B0%E5%90%8E%E7%AB%AF%E7%A0%94%E5%8F%91%E5%AE%9E%E4%B9%A0%E7%BB%8F%E5%8E%86;%E5%85%B3%E6%B3%A8%E5%B7%A5%E5%8D%95%E6%B5%81%E8%BD%AC%E4%B8%8E%E5%B9%B6%E5%8F%91%E6%8E%A7%E5%88%B6%E3%80%81%E7%BC%93%E5%AD%98%E4%BC%98%E5%8C%96;%E8%83%BD%E8%80%97%E4%BB%BF%E7%9C%9F%E7%AD%96%E7%95%A5%E4%B8%8E+AI+Agent+%E8%90%BD%E5%9C%B0%E5%AE%9E%E8%B7%B5%E3%80%82" alt="Intro" />
</p>

---

### 🛠️ 技术栈

<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <b>后端开发</b><br/><br/>
      <img src="https://img.shields.io/badge/-Java-007396?style=flat-square&logo=java&logoColor=white" alt="Java" />
      <img src="https://img.shields.io/badge/-Spring%20Boot-6DB33F?style=flat-square&logo=spring-boot&logoColor=white" alt="Spring Boot" />
      <img src="https://img.shields.io/badge/-MyBatis-000000?style=flat-square" alt="MyBatis" />
      <img src="https://img.shields.io/badge/-Spring%20Task-6DB33F?style=flat-square" alt="Spring Task" />
      <img src="https://img.shields.io/badge/-Spring%20Cache-6DB33F?style=flat-square" alt="Spring Cache" />
      <img src="https://img.shields.io/badge/-AOP-6DB33F?style=flat-square" alt="AOP" />
      <img src="https://img.shields.io/badge/-WebSocket-010101?style=flat-square" alt="WebSocket" />
      <img src="https://img.shields.io/badge/-JWT-000000?style=flat-square&logo=json-web-tokens&logoColor=white" alt="JWT" />
      <img src="https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
      <img src="https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
    </td>
    <td width="50%" valign="top">
      <b>数据库与中间件</b><br/><br/>
      <img src="https://img.shields.io/badge/-MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" alt="MySQL" />
      <img src="https://img.shields.io/badge/-Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" />
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <b>AI 与 Agent</b><br/><br/>
      <img src="https://img.shields.io/badge/-LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangChain" />
      <img src="https://img.shields.io/badge/-LangGraph-1C3C3C?style=flat-square" alt="LangGraph" />
      <img src="https://img.shields.io/badge/-RAG-4B8BBE?style=flat-square" alt="RAG" />
      <img src="https://img.shields.io/badge/-ChromaDB-FF6F61?style=flat-square" alt="ChromaDB" />
    </td>
    <td width="50%" valign="top">
      <b>工程化与工具</b><br/><br/>
      <img src="https://img.shields.io/badge/-Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git" />
      <img src="https://img.shields.io/badge/-AI%20Coding-412991?style=flat-square" alt="AI Coding" />
    </td>
  </tr>
</table>

---

### 💡 核心项目

<details>
  <summary><b>🏭 空调工单服务平台（国企甲方项目）</b> ｜ <code>Java / Spring Boot / MySQL</code></summary>
  <br/>
  
  - 负责工单流转模块研发，参与需求评审与业务规则梳理。
  - 研发基于配置表的通用审批流引擎，支撑 10+ 流转操作，复用驱动维修与巡检业务。
  - 采用「乐观校验 + 单机加锁 + 冗余清除」机制，解决并发办理时的重复接单与审批问题。
</details>

<details>
  <summary><b>🔋 建筑能耗预测仿真平台</b> ｜ <code>Python / FastAPI / NumPy</code></summary>
  <br/>
  
  - 参与 8760 小时仿真引擎及群控/MPC 控制策略模块开发。
  - 建立冷机/水泵/冷却塔物理模型，依据环境参数计算设备功率。
  - 实现群控寻优及 MPC 预测控制（动态规划求解含电价与启停惩罚），优化综合能效。
</details>

<details>
  <summary><b>🍜 餐饮商户外卖平台</b> ｜ <code>Java / Spring Boot / Redis / WebSocket</code></summary>
  <br/>
  
  - 项目包含小程序用户端与商家后台端，提供点单、接单与配送服务。
  - 基于 JWT + 拦截器 + ThreadLocal 实现双端身份验证与上下文传递。
  - 利用自定义注解结合 AOP 切面，实现公共字段自动填充。
  - 基于 WebSocket 实现来单提醒，Spring Task 处理订单超时取消。
  - 针对菜单读多写少场景，使用 Redis + Spring Cache 缓存，降低数据库压力。
</details>

<details>
  <summary><b>🔧 基于 Agent 的冷凝阀门仿真选型软件</b> ｜ <code>Python / LangGraph / RAG</code></summary>
  <br/>

  🔗 **源码**：[https://github.com/Alex-hjx520/-agent-](https://github.com/Alex-hjx520/-agent-)

  - 基于 LangGraph 构建“解析-检索-初选-仿真-调优”的智能决策闭环。
  - 结合 BGE 模型与 ChromaDB 搭建 RAG 知识库，融合多源数据实现候选型号去重与回填。
  - 利用 CoolProp 计算制冷剂物性与制冷量，实现膨胀阀容量扩展及过冷度/压降修正。
  - 实现 Agent 闭环决策，支持多设备批量仿真并自动执行调压/调温/换型等操作。
</details>

<details>
  <summary><b>⚖️ LCR-Agent · 法律合同审查 Agent</b> ｜ <code>Python / LangGraph / BM25</code></summary>
  <br/>

  🔗 **源码**：[https://github.com/Alex-hjx520/LCR-Agent](https://github.com/Alex-hjx520/LCR-Agent)

  - 基于 LangGraph 拆解审查链路为有状态图，节点支持独立测试与替换。
  - 采用“规则先行、LLM 兜底”策略，确保合规检查可复现、可审计。
  - 搭建 BM25 + Chroma 混合检索与 RRF 融合，输出可回溯的风险结论（citations）。
  - 设计分层解耦架构与无状态 Agent 签名，支持单测、重放、并行及人机协同。
  - 采用 Poetry + ruff + mypy + pytest 工程化落地，提供 CLI 与 API，支持离线降级。
</details>

---

### 📊 GitHub 统计

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Alex-520hjx&show_icons=true&theme=transparent&hide_border=true&count_private=true" alt="GitHub Stats" />
</p>

<br/>

---

### 📫 联系我

- 📧 **Email**：2861902988@qq.com
- 💼 **求职状态**：正在寻找 Java 后端开发岗位（秋招）
