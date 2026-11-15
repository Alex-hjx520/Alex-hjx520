<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Projects · Alex-hjx520</title>
<style>
  :root { color-scheme: dark light; }
  * { box-sizing: border-box; }
  body {
    margin: 0; padding: 32px 16px;
    font: 15px/1.6 -apple-system, BlinkMacSystemFont, "Segoe UI", "PingFang SC", "Microsoft YaHei", sans-serif;
    background: #0d1117; color: #c9d1d9;
  }
  .wrap { max-width: 1000px; margin: 0 auto; }
  h1 { font-size: 22px; margin: 0 0 8px; color: #e6edf3; }
  .sub { color: #8b949e; margin-bottom: 24px; font-size: 14px; }
  /* —— 网格：两列，卡片统一高度 —— */
  .grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 16px;
  }
  @media (max-width: 640px) { .grid { grid-template-columns: 1fr; } }

  .card {
    display: flex; flex-direction: column; justify-content: space-between;
    min-height: 150px; padding: 18px 20px;
    background: #161b22;
    border: 1px solid #30363d; border-radius: 10px;
    cursor: pointer;
    transition: transform .15s ease, border-color .15s ease, box-shadow .15s ease;
  }
  .card:hover {
    transform: translateY(-2px);
    border-color: #58a6ff;
    box-shadow: 0 6px 20px rgba(88,166,255,.12);
  }
  .card .emoji { font-size: 26px; }
  .card .title { font-size: 16px; font-weight: 600; color: #e6edf3; margin: 6px 0 8px; }
  .card .stack { font-size: 12.5px; color: #8b949e; }
  .card .stack code {
    background: #21262d; border: 1px solid #30363d; border-radius: 4px;
    padding: 1px 6px; margin: 0 2px 2px 0; color: #c9d1d9;
    font-size: 12px; font-family: ui-monospace, SFMono-Regular, Menlo, monospace;
    display: inline-block;
  }

  /* —— 详情视图 —— */
  #grid.hidden, #detail.hidden { display: none; }
  .back {
    display: inline-flex; align-items: center; gap: 6px;
    margin-bottom: 20px; padding: 7px 14px;
    background: #21262d; color: #c9d1d9;
    border: 1px solid #30363d; border-radius: 8px;
    font-size: 14px; cursor: pointer;
  }
  .back:hover { border-color: #58a6ff; color: #e6edf3; }
  .detail-card {
    background: #161b22; border: 1px solid #30363d; border-radius: 12px;
    padding: 28px 32px;
  }
  .detail-card h2 { margin: 0 0 4px; font-size: 22px; color: #e6edf3; }
  .detail-card .period { color: #8b949e; font-size: 13px; margin-bottom: 16px; }
  .detail-card .stack-line { margin: 0 0 20px; }
  .detail-card .stack-line code {
    background: #21262d; border: 1px solid #30363d; border-radius: 4px;
    padding: 2px 7px; margin: 0 4px 4px 0; color: #c9d1d9;
    font-size: 12.5px; font-family: ui-monospace, SFMono-Regular, Menlo, monospace;
    display: inline-block;
  }
  .detail-card ul { margin: 0 0 18px; padding-left: 22px; }
  .detail-card li { margin-bottom: 10px; color: #c9d1d9; }
  .detail-card a { color: #58a6ff; text-decoration: none; }
  .detail-card a:hover { text-decoration: underline; }
</style>
</head>
<body>
<div class="wrap">
  <h1>💡 核心项目</h1>
  <div class="sub">点击卡片查看详情，点击返回回到列表</div>

  <div id="grid" class="grid"></div>

  <div id="detail" class="hidden">
    <button class="back" onclick="backToGrid()">← 返回项目列表</button>
    <div id="detailBody" class="detail-card"></div>
  </div>
</div>

<script>
  const projects = [
    {
      id: 'ac',
      emoji: '🏭',
      title: '空调工单服务平台',
      subtitle: '国企甲方项目 · 工单流转模块',
      period: '',
      stack: ['Java', 'Spring Boot', 'MySQL', 'MyBatis'],
      link: null,
      highlights: [
        '负责工单流程模块后端研发，深度参与甲方需求评审与业务规则梳理。',
        '研发基于配置表的通用审批流引擎，支撑派单、转派、回退、办结等 10+ 流转操作，单引擎复用驱动维修与巡检两条业务线。',
        '采用「节点权重乐观校验 + 关键方法单机加锁 + 同节点冗余待办清除」三层机制，缓解工单多人同时办理时的重复接单与重复审批问题。'
      ]
    },
    {
      id: 'energy',
      emoji: '🔋',
      title: '建筑能耗预测仿真平台',
      subtitle: '8760 小时仿真引擎 · 群控 / MPC 策略',
      period: '',
      stack: ['Python', 'FastAPI', 'NumPy'],
      link: null,
      highlights: [
        '参与仿真软件研发，参与设计 8760 小时仿真引擎、群控/MPC 控制策略模块的全流程开发。',
        '物理设备性能算法：建立冷水机组/水泵/冷却塔物理建模，根据湿球温度、冷负荷等参数为仿真引擎提供冷水机组/水泵/冷却塔风机的功率计算。',
        '仿真引擎策略算法：为实现系统综合能效优化，实现简单加减机、群控优化（枚举 2^N-1 台数组合寻优）及 MPC 预测控制（动态规划求解含分时电价与启停惩罚的滚动优化）。'
      ]
    },
    {
      id: 'takeout',
      emoji: '🍜',
      title: '餐饮商户外卖平台',
      subtitle: '小程序用户端 + 商家管理端',
      period: '',
      stack: ['Java SE', 'Spring Boot', 'MySQL', 'Redis', 'MyBatis', 'JWT', 'WebSocket', 'Spring Task', 'Spring Cache'],
      link: null,
      highlights: [
        '项目背景：小型商户外卖平台服务于线下餐饮品牌，由微信小程序用户端与商家后台管理端组成，为用户提供餐品浏览、菜品点单，同时为商家提供接单与配送服务。',
        'C 端/B 端登录与身份验证：使用 JWT 生成令牌，配合拦截器进行身份拦截，ThreadLocal 实现用户身份的无侵入式上下文传递，保障多线程环境下的数据安全。',
        'AOP 实现公共字段自动填充：针对表结构中频繁更新的公共字段（如创建时间、更新时间），利用自定义注解结合 AOP 切面编程，在方法执行前实现数据自动填充。',
        'WebSocket 实现来单提醒；利用 Spring Task 定时任务实现订单超时处理，超时自动取消订单。',
        '针对 C 端菜单读多写少场景，使用 Redis + Spring Cache 缓存菜品与套餐数据，写操作触发缓存失效，降低数据库读压力。'
      ]
    },
    {
      id: 'valve',
      emoji: '🔧',
      title: '冷凝阀门 Agent 选型系统',
      subtitle: 'Agent 闭环决策 · RAG 知识库',
      period: '2026.08 - 2026.10',
      stack: ['Python', 'FastAPI', 'LangChain', 'LangGraph', 'RAG', 'ChromaDB', 'CoolProp', 'MySQL', 'Vue3'],
      link: 'https://github.com/Alex-hjx520/-agent-',
      highlights: [
        '主导系统整体架构设计与核心开发，基于 LangGraph 构建"需求解析—多源检索—候选初选—批量仿真—Agent 调优—报告生成"的完整智能决策业务闭环。',
        '基于 BGE 中文向量模型与 ChromaDB 搭建制冷设备 RAG 知识库，融合本地 PDF、MySQL 参数库、限定域名及全网搜索，实现候选型号去重与参数回填。',
        '利用 CoolProp 实现制冷剂物性、焓差、质量流量及制冷量计算；针对 RFKH 热力膨胀阀实现多制冷剂容量扩展表、过冷度修正和压降修正算法。',
        '基于 LangGraph 实现 Agent 闭环决策，对最多 5 个候选设备进行批量仿真，自动执行调节阀前压差、过冷度、过热度或换型等操作，直至满足达标数量或达到最大迭代次数。'
      ]
    },
    {
      id: 'lcr',
      emoji: '⚖️',
      title: 'LCR-Agent 合同审查',
      subtitle: 'BM25 + 向量混合检索 · 可审计',
      period: '2026.08 - 2026.10',
      stack: ['Python', 'LangGraph', 'FastAPI', 'Pydantic v2', 'Chroma', 'BM25', 'RAG'],
      link: 'https://github.com/Alex-hjx520/LCR-Agent',
      highlights: [
        '主导系统架构设计与核心开发，基于 LangGraph 将合同审查链路拆解为「解析 → 切分 → 条款抽取 → 风险审查 → 合规检查 → 摘要 → 报告」的有状态图，每个节点均可独立测试与替换。',
        '采用规则先行、LLM 兜底策略：正则定位条款边界保证不丢不越界，LLM 负责分类，模型不可用时自动回退关键词规则；合规检查由确定性正则引擎完成，可复现、可审计。',
        '搭建 BM25 + Chroma 混合检索，用 RRF 融合稀疏与稠密召回，接入 CUAD 先例语料，为每条风险结论写入可回溯的 citations。',
        '设计分层解耦架构（schemas ← parsing ← knowledge ← agents ← graph ← api）与无状态 Agent 签名 run(state) -> dict，支持单测、重放、并行及 HITL 人机协同。',
        '工程化落地：Poetry + ruff + mypy + pytest，提供 CLI 与 FastAPI 全套接口，未配置密钥时自动降级为离线 stub，可先跑通全链路。'
      ]
    }
  ];

  const gridEl = document.getElementById('grid');
  const detailEl = document.getElementById('detail');
  const detailBody = document.getElementById('detailBody');
  const esc = s => s.replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));

  function renderGrid() {
    gridEl.innerHTML = projects.map(p => `
      <div class="card" data-id="${p.id}">
        <div>
          <div class="emoji">${p.emoji}</div>
          <div class="title">${esc(p.title)}</div>
        </div>
        <div class="stack">${p.stack.slice(0, 4).map(s => `<code>${esc(s)}</code>`).join('')}</div>
      </div>
    `).join('');
    gridEl.querySelectorAll('.card').forEach(c => {
      c.addEventListener('click', () => openDetail(c.dataset.id));
    });
  }

  function openDetail(id) {
    const p = projects.find(x => x.id === id);
    if (!p) return;
    detailBody.innerHTML = `
      <h2>${p.emoji} ${esc(p.title)}</h2>
      <div class="period">${esc(p.subtitle)}${p.period ? ' · ' + esc(p.period) : ''}</div>
      <div class="stack-line">${p.stack.map(s => `<code>${esc(s)}</code>`).join('')}</div>
      <ul>${p.highlights.map(h => `<li>${esc(h)}</li>`).join('')}</ul>
      ${p.link ? `<a href="${p.link}" target="_blank" rel="noopener">🔗 查看项目源码 →</a>` : ''}
    `;
    gridEl.classList.add('hidden');
    detailEl.classList.remove('hidden');
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }

  function backToGrid() {
    detailEl.classList.add('hidden');
    gridEl.classList.remove('hidden');
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }

  renderGrid();
</script>
</body>
</html>
