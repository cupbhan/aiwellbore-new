+++
title = "在研项目"
description = "汇总课题组当前承担的在研项目，提供项目基本信息与进展概况，并支持按研究方向快速筛选。"
date = 2026-02-25T12:30:00+08:00
draft = false
+++

<div class="stats-row">
  <div class="stat-card"><div class="stat-num">12+</div><div class="stat-label">在研项目</div></div>
  <div class="stat-card"><div class="stat-num">4</div><div class="stat-label">研究方向</div></div>
  <div class="stat-card"><div class="stat-num">3+</div><div class="stat-label">合作单位</div></div>
  <div class="stat-card"><div class="stat-num">3</div><div class="stat-label">开放招生</div></div>
</div>

---

## 快速筛选（按研究方向）

<div class="quick-filter">
  <button class="qf-btn qf-active" onclick="filterProjects('all', this)">全部</button>
  <button class="qf-btn" onclick="filterProjects('wellbore', this)">🔬 井筒多相流</button>
  <button class="qf-btn" onclick="filterProjects('lift', this)">⚙️ 人工举升</button>
  <button class="qf-btn" onclick="filterProjects('ai', this)">🤖 智能化采油气</button>
  <button class="qf-btn" onclick="filterProjects('dewater', this)">💧 气井排采</button>
</div>

<script>
function filterProjects(dir, btn) {
  document.querySelectorAll('.qf-btn').forEach(b => b.classList.remove('qf-active'));
  btn.classList.add('qf-active');
  document.querySelectorAll('.project-card').forEach(card => {
    if (dir === 'all' || card.dataset.dir === dir) {
      card.style.display = '';
    } else {
      card.style.display = 'none';
    }
  });
}
</script>

<style>
.qf-btn { cursor: pointer; border: 1.5px solid rgba(0,0,0,0.1); background: #fff; font-size: 0.88rem; font-weight: 500; padding: 7px 16px; border-radius: 999px; transition: all 0.2s; }
.qf-btn.qf-active, .qf-btn:hover { background: #003366; color: white; border-color: #003366; }
</style>

---

## 项目列表

<div class="project-list">

<div class="project-card" data-dir="lift">
  <div class="project-head">
    <h4><a href="./p01/">油气藏-井筒-管网动态仿真引擎软件</a></h4>
    <div class="badges"><span class="badge badge-national">省部级</span><span class="badge badge-active">在研</span><span class="badge badge-stu">学生参与</span></div>
  </div>
  <p class="muted">一句话目标：一体化耦合，人工举升，节点分析</p>
  <div class="meta">
    <span>方向：<span class="dir-tag dir-lift">人工举升</span></span>
    <span>📅 2023-2026</span>
    <span>👤 韩国庆</span>
    <span>阶段：总结验收</span>
  </div>
  <div class="tags"><span class="tag">一体化耦合</span><span class="tag">人工举升</span><span class="tag">节点分析</span></div>
</div>

<div class="project-card" data-dir="ai">
  <div class="project-head">
    <h4><a href="./p02/">海上光电液一体化智能完井设计与调控方法研究</a></h4>
    <div class="badges"><span class="badge badge-national">省部级</span><span class="badge badge-active">在研</span><span class="badge badge-stu">学生参与</span></div>
  </div>
  <p class="muted">一句话目标：智能完井，代理模型，双闭环优化</p>
  <div class="meta">
    <span>方向：<span class="dir-tag dir-ai">智能化采油气</span></span>
    <span>📅 2024-2026</span>
    <span>👤 韩国庆</span>
    <span>阶段：总结验收</span>
  </div>
  <div class="tags"><span class="tag">智能完井</span><span class="tag">代理模型</span><span class="tag">双闭环优化</span></div>
</div>

<div class="project-card" data-dir="ai">
  <div class="project-head">
    <h4><a href="./p03/">油井举升智能分析与优化管控模型服务化封装</a></h4>
    <div class="badges"><span class="badge badge-enterprise">企业</span><span class="badge badge-active">在研</span><span class="badge badge-stu">学生参与</span></div>
  </div>
  <p class="muted">一句话目标：智能分析，优化管控，代理模型，数字孪生</p>
  <div class="meta">
    <span>方向：<span class="dir-tag dir-ai">智能化采油气</span></span>
    <span>📅 2025-2026</span>
    <span>👤 韩国庆</span>
    <span>阶段：总结验收</span>
  </div>
  <div class="tags"><span class="tag">智能分析</span><span class="tag">优化管控</span><span class="tag">代理模型</span><span class="tag">数字孪生</span></div>
</div>

<div class="project-card" data-dir="dewater">
  <div class="project-head">
    <h4><a href="./p04/">油藏型储气库井筒携液机理研究及工艺优化技术服务</a></h4>
    <div class="badges"><span class="badge badge-enterprise">企业</span><span class="badge badge-active">在研</span><span class="badge badge-stu">学生参与</span></div>
  </div>
  <p class="muted">一句话目标：储气库井，排采，节点分析，携液规律</p>
  <div class="meta">
    <span>方向：<span class="dir-tag dir-dewater">气井排采</span></span>
    <span>📅 2025-2026</span>
    <span>👤 韩国庆</span>
    <span>阶段：在研</span>
  </div>
  <div class="tags"><span class="tag">储气库井</span><span class="tag">排采</span><span class="tag">节点分析</span><span class="tag">携液规律</span></div>
</div>

<div class="project-card" data-dir="dewater">
  <div class="project-head">
    <h4><a href="./p05/">宝岛21-1气田群高产水气井井筒流动规律及携液实验研究</a></h4>
    <div class="badges"><span class="badge badge-enterprise">企业</span><span class="badge badge-active">在研</span><span class="badge badge-open">开放招生</span></div>
  </div>
  <p class="muted">一句话目标：气举，积液，水合物</p>
  <div class="meta">
    <span>方向：<span class="dir-tag dir-dewater">气井排采</span></span>
    <span>📅 2025-2026</span>
    <span>👤 梁星原</span>
    <span>阶段：在研</span>
  </div>
  <div class="tags"><span class="tag">气举</span><span class="tag">积液</span><span class="tag">水合物</span></div>
</div>

<div class="project-card" data-dir="lift">
  <div class="project-head">
    <h4><a href="./p06/">中高含水期稠油井大排量举升不掺稀可行性研究</a></h4>
    <div class="badges"><span class="badge badge-enterprise">企业</span><span class="badge badge-active">在研</span><span class="badge badge-stu">学生参与</span></div>
  </div>
  <p class="muted">一句话目标：不掺稀，电泵井，油水流动规律</p>
  <div class="meta">
    <span>方向：<span class="dir-tag dir-lift">人工举升</span></span>
    <span>📅 2025-2026</span>
    <span>👤 梁星原</span>
    <span>阶段：在研</span>
  </div>
  <div class="tags"><span class="tag">不掺稀</span><span class="tag">电泵井</span><span class="tag">油水流动规律</span></div>
</div>

<div class="project-card" data-dir="dewater">
  <div class="project-head">
    <h4><a href="./p07/">致密储层合理排采工作制度优化研究</a></h4>
    <div class="badges"><span class="badge badge-enterprise">企业</span><span class="badge badge-active">在研</span><span class="badge badge-open">开放招生</span></div>
  </div>
  <p class="muted">一句话目标：气井排采，智能平台，合理制度，气井诊断</p>
  <div class="meta">
    <span>方向：<span class="dir-tag dir-dewater">气井排采</span></span>
    <span>📅 2025-2026</span>
    <span>👤 韩国庆</span>
    <span>阶段：初期</span>
  </div>
  <div class="tags"><span class="tag">气井排采</span><span class="tag">智能平台</span><span class="tag">合理制度</span><span class="tag">气井诊断</span></div>
</div>

<div class="project-card" data-dir="wellbore">
  <div class="project-head">
    <h4><a href="./p08/">车510井区多介质辅助蒸汽驱井筒流动规律模拟分析</a></h4>
    <div class="badges"><span class="badge badge-enterprise">企业</span><span class="badge badge-active">在研</span><span class="badge badge-stu">学生参与</span></div>
  </div>
  <p class="muted">一句话目标：蒸汽驱，多相流，换热</p>
  <div class="meta">
    <span>方向：<span class="dir-tag dir-wellbore">井筒多相流</span></span>
    <span>📅 2025-2026</span>
    <span>👤 韩国庆</span>
    <span>阶段：在研</span>
  </div>
  <div class="tags"><span class="tag">蒸汽驱</span><span class="tag">多相流</span><span class="tag">换热</span></div>
</div>

<div class="project-card" data-dir="ai">
  <div class="project-head">
    <h4><a href="./p09/">数据物理驱动的深井举升故障诊断与自动调优模块加工</a></h4>
    <div class="badges"><span class="badge badge-enterprise">企业</span><span class="badge badge-active">在研</span><span class="badge badge-stu">学生参与</span></div>
  </div>
  <p class="muted">一句话目标：物理驱动，深井，故障诊断，自动调优</p>
  <div class="meta">
    <span>方向：<span class="dir-tag dir-ai">智能化采油气</span></span>
    <span>📅 2025-2026</span>
    <span>👤 韩国庆</span>
    <span>阶段：总结验收</span>
  </div>
  <div class="tags"><span class="tag">物理驱动</span><span class="tag">深井</span><span class="tag">故障诊断</span><span class="tag">自动调优</span></div>
</div>

<div class="project-card" data-dir="lift">
  <div class="project-head">
    <h4><a href="./p10/">致密储层压后渗流规律和产能影响因素研究</a></h4>
    <div class="badges"><span class="badge badge-enterprise">企业</span><span class="badge badge-active">在研</span><span class="badge badge-open">开放招生</span></div>
  </div>
  <p class="muted">一句话目标：一体化耦合，分区渗流，分时流动</p>
  <div class="meta">
    <span>方向：<span class="dir-tag dir-lift">人工举升</span></span>
    <span>📅 2026-2027</span>
    <span>👤 韩国庆</span>
    <span>阶段：初期</span>
  </div>
  <div class="tags"><span class="tag">一体化耦合</span><span class="tag">分区渗流</span><span class="tag">分时流动</span></div>
</div>

<div class="project-card" data-dir="ai">
  <div class="project-head">
    <h4><a href="./p11/">数据驱动的油井故障预警与自动调优建模及测试分析</a></h4>
    <div class="badges"><span class="badge badge-enterprise">企业</span><span class="badge badge-active">在研</span><span class="badge badge-stu">学生参与</span></div>
  </div>
  <p class="muted">一句话目标：数据驱动，故障预警，自动调优</p>
  <div class="meta">
    <span>方向：<span class="dir-tag dir-ai">智能化采油气</span></span>
    <span>📅 2024-2026</span>
    <span>👤 韩国庆</span>
    <span>阶段：在研</span>
  </div>
  <div class="tags"><span class="tag">数据驱动</span><span class="tag">故障预警</span><span class="tag">自动调优</span></div>
</div>

</div>
