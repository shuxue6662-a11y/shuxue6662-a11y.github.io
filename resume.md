---
layout: default
title: 详细简历
---

<style>
/* ====== 简历整体容器 ====== */
.resume-wrapper {
  max-width: 900px;
  margin: 0 auto;
  padding: 20px 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Noto Sans SC", sans-serif;
  color: #2c3e50;
  line-height: 1.8;
}

/* ====== 顶部头卡片 ====== */
.resume-header {
  text-align: center;
  padding: 48px 32px 36px;
  background: linear-gradient(135deg, #0a0a23 0%, #1a1a40 50%, #2d2d6b 100%);
  border-radius: 16px;
  margin-bottom: 40px;
  position: relative;
  overflow: hidden;
}

.resume-header::before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle at 30% 70%, rgba(99, 132, 255, 0.08) 0%, transparent 50%),
              radial-gradient(circle at 70% 30%, rgba(0, 198, 255, 0.06) 0%, transparent 50%);
  pointer-events: none;
}

.resume-header h1 {
  font-size: 2.6em;
  font-weight: 700;
  color: #ffffff;
  margin: 0 0 20px 0;
  letter-spacing: 8px;
  position: relative;
}

.resume-header h1::after {
  content: '';
  display: block;
  width: 60px;
  height: 3px;
  background: linear-gradient(90deg, #6c8cff, #00c6ff);
  margin: 16px auto 0;
  border-radius: 2px;
}

.contact-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 12px 28px;
  position: relative;
}

.contact-item {
  color: rgba(255, 255, 255, 0.85);
  font-size: 0.95em;
  display: flex;
  align-items: center;
  gap: 6px;
}

.contact-item .icon {
  font-size: 1em;
  opacity: 0.7;
}

/* ====== 标签组 ====== */
.tag-group {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 20px;
  position: relative;
}

.tag {
  background: rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.15);
  color: rgba(255, 255, 255, 0.9);
  padding: 4px 16px;
  border-radius: 20px;
  font-size: 0.85em;
  backdrop-filter: blur(4px);
}

/* ====== 章节标题 ====== */
.section-title {
  font-size: 1.35em;
  font-weight: 700;
  color: #1a1a2e;
  margin: 48px 0 24px 0;
  padding-bottom: 12px;
  border-bottom: 2px solid #e8ecf1;
  display: flex;
  align-items: center;
  gap: 10px;
}

.section-title .emoji {
  font-size: 1.2em;
}

.section-title span {
  background: linear-gradient(90deg, #2d3561, #4a5899);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* ====== 经历卡片 ====== */
.exp-card {
  background: #fafbfd;
  border: 1px solid #eef0f5;
  border-radius: 12px;
  padding: 24px 28px;
  margin-bottom: 20px;
  transition: all 0.3s ease;
  position: relative;
}

.exp-card:hover {
  border-color: #d0d7e5;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.04);
  transform: translateY(-1px);
}

.exp-card-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 6px;
}

.exp-card-title {
  font-size: 1.12em;
  font-weight: 700;
  color: #1a1a2e;
  margin: 0;
}

.exp-card-role {
  font-size: 0.9em;
  color: #5a6a8a;
  margin: 2px 0 10px 0;
}

.exp-time {
  font-size: 0.82em;
  color: #8892a8;
  background: #f0f2f7;
  padding: 3px 12px;
  border-radius: 6px;
  white-space: nowrap;
  font-weight: 500;
}

.exp-card ul {
  margin: 0;
  padding-left: 0;
  list-style: none;
}

.exp-card ul li {
  position: relative;
  padding-left: 20px;
  margin-bottom: 8px;
  font-size: 0.93em;
  color: #4a5568;
  line-height: 1.75;
}

.exp-card ul li::before {
  content: '';
  position: absolute;
  left: 2px;
  top: 10px;
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: linear-gradient(135deg, #6c8cff, #4a5899);
}

/* ====== 教育经历特殊样式 ====== */
.edu-card {
  border-left: 3px solid #4a5899;
}

.edu-school {
  font-size: 1.15em;
  font-weight: 700;
  color: #1a1a2e;
}

.edu-badge {
  display: inline-flex;
  gap: 6px;
  margin-left: 8px;
}

.edu-badge span {
  background: linear-gradient(135deg, #4a5899, #6c8cff);
  color: white;
  font-size: 0.7em;
  padding: 2px 8px;
  border-radius: 4px;
  font-weight: 500;
}

.edu-major {
  color: #3d4f6f;
  font-weight: 600;
  font-size: 1em;
  margin: 4px 0;
}

/* ====== 荣誉表格 ====== */
.award-table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
  border-radius: 12px;
  overflow: hidden;
  border: 1px solid #eef0f5;
}

.award-table thead th {
  background: #f7f8fb;
  padding: 14px 20px;
  text-align: left;
  font-weight: 600;
  color: #3d4f6f;
  font-size: 0.9em;
  border-bottom: 2px solid #e8ecf1;
}

.award-table tbody td {
  padding: 14px 20px;
  font-size: 0.92em;
  color: #4a5568;
  border-bottom: 1px solid #f0f2f7;
}

.award-table tbody tr:last-child td {
  border-bottom: none;
}

.award-table tbody tr:hover {
  background: #f9fafc;
}

.award-icon {
  margin-right: 6px;
}

/* ====== 技能区域 ====== */
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 16px;
}

.skill-card {
  background: #fafbfd;
  border: 1px solid #eef0f5;
  border-radius: 10px;
  padding: 18px 22px;
  transition: all 0.3s ease;
}

.skill-card:hover {
  border-color: #d0d7e5;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.03);
}

.skill-name {
  font-weight: 700;
  color: #1a1a2e;
  font-size: 0.95em;
  margin-bottom: 4px;
}

.skill-desc {
  color: #6b7a96;
  font-size: 0.88em;
  margin: 0;
}

/* ====== 底部联系区 ====== */
.contact-footer {
  text-align: center;
  padding: 36px 24px;
  background: #f7f8fb;
  border-radius: 12px;
  margin-top: 48px;
  border: 1px solid #eef0f5;
}

.contact-footer-title {
  font-size: 1.1em;
  font-weight: 700;
  color: #1a1a2e;
  margin-bottom: 16px;
}

.contact-links {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 16px;
}

.contact-link {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 10px 24px;
  border-radius: 8px;
  font-size: 0.92em;
  text-decoration: none;
  font-weight: 500;
  transition: all 0.3s ease;
}

.contact-link.github {
  background: #24292e;
  color: white;
}

.contact-link.github:hover {
  background: #1a1e22;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(36, 41, 46, 0.3);
}

.contact-link.email {
  background: #4a5899;
  color: white;
}

.contact-link.email:hover {
  background: #3d4a82;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(74, 88, 153, 0.3);
}

/* ====== 响应式 ====== */
@media (max-width: 640px) {
  .resume-header {
    padding: 36px 20px 28px;
  }
  .resume-header h1 {
    font-size: 2em;
    letter-spacing: 4px;
  }
  .contact-grid {
    gap: 6px 16px;
  }
  .exp-card {
    padding: 18px 20px;
  }
  .exp-card-header {
    flex-direction: column;
  }
  .skills-grid {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="resume-wrapper">

  <!-- ==================== 顶部头卡片 ==================== -->
  <div class="resume-header">
    <h1>张 弘</h1>
    <div class="contact-grid">
      <div class="contact-item"><span class="icon">📱</span> 15625001647</div>
      <div class="contact-item"><span class="icon">📧</span> zhsxue@163.com</div>
      <div class="contact-item"><span class="icon">📍</span> 广州</div>
      <div class="contact-item"><span class="icon">🎂</span> 20岁</div>
    </div>
    <div class="tag-group">
      <span class="tag">中共预备党员</span>
      <span class="tag">华南理工大学</span>
      <span class="tag">应用数学 · 强基计划</span>
    </div>
  </div>

  <!-- ==================== 教育经历 ==================== -->
  <div class="section-title">
    <span class="emoji">🎓</span><span>教育经历</span>
  </div>

  <div class="exp-card edu-card">
    <div class="exp-card-header">
      <div>
        <div class="edu-school">
          华南理工大学
          <span class="edu-badge">
            <span>985</span><span>211</span><span>双一流</span>
          </span>
        </div>
        <div class="edu-major">应用数学（强基计划班）· 本科 · 数学学院</div>
      </div>
      <span class="exp-time">2023.09 - 2027.07</span>
    </div>
    <ul>
      <li>扎实掌握概率论、统计学及高等代数等核心理论，为建模分析奠定数学基础</li>
      <li>深入学习机器学习基础、数据结构及数据库原理，具备将业务问题转化为数学模型的能力</li>
    </ul>
  </div>

  <!-- ==================== 项目经历 ==================== -->
  <div class="section-title">
    <span class="emoji">🚀</span><span>项目经历</span>
  </div>

  <div class="exp-card">
    <div class="exp-card-header">
      <div class="exp-card-title">基于谱图理论的 Laplacian Eigenmaps 流形学习算法研究与实现</div>
      <span class="exp-time">2026.01 - 2026.02</span>
    </div>
    <div class="exp-card-role">算法开发</div>
    <ul>
      <li>进行流形学习算法研究，利用 Python 复现 LE 算法并进行性能优化</li>
      <li>通过 Scipy 稀疏矩阵技术，将算法空间复杂度降低至 O(nk)，提升计算效率</li>
      <li>建立参数敏感性框架，通过实验确立参数选择法则，确保模型在复杂场景下的鲁棒性</li>
    </ul>
  </div>

  <div class="exp-card">
    <div class="exp-card-header">
      <div class="exp-card-title">基于 Apriori 算法的购物篮关联规则挖掘</div>
      <span class="exp-time">2025.12</span>
    </div>
    <div class="exp-card-role">独立完成</div>
    <ul>
      <li>处理 54 万级大规模数据集，利用 Pandas 完成数据清洗与特征工程</li>
      <li>基于 Python 实现关联规则挖掘，通过参数调优获取 295 条核心业务规则</li>
      <li>将数据洞察转化为营销策略，设计智能推荐方案，预估提升客单价 200%</li>
    </ul>
  </div>

  <div class="exp-card">
    <div class="exp-card-header">
      <div class="exp-card-title">华南理工大学第二十四届数理大赛 —— 塞伦盖蒂生态系统种群动力学建模</div>
      <span class="exp-time">2025.11</span>
    </div>
    <div class="exp-card-role">队长（单人参赛）</div>
    <ul>
      <li>独立完成复杂系统建模分析，荣获数理大赛<strong>一等奖</strong>（前 8%）</li>
      <li>构建动力学模型体系，通过蒙特卡洛模拟进行 1000 次模型验证</li>
      <li>利用 Hopf 分岔分析识别系统边界，实现预测误差低于 2.3%</li>
    </ul>
  </div>

  <!-- ==================== 社团和组织经历 ==================== -->
  <div class="section-title">
    <span class="emoji">👥</span><span>社团与组织经历</span>
  </div>

  <div class="exp-card">
    <div class="exp-card-header">
      <div class="exp-card-title">华南理工大学数学学院 2023 强基计划班</div>
      <span class="exp-time">2024.09 - 至今</span>
    </div>
    <div class="exp-card-role">团支书 / 班长</div>
    <ul>
      <li>主导班级事务管理，建立基于数据反馈的运营机制，实现活动满意度 95% 以上</li>
      <li>统筹协调 30 人规模团队，展现出极强的逻辑思维与团队协作能力</li>
    </ul>
  </div>

  <div class="exp-card">
    <div class="exp-card-header">
      <div class="exp-card-title">华南理工大学学生科学技术协会</div>
      <span class="exp-time">2023.09 - 2024.11</span>
    </div>
    <div class="exp-card-role">干事 · 赛事策划部</div>
    <ul>
      <li>负责招新数据采集与清洗，利用 Excel / SQL 对 100+ 条信息进行多维分类</li>
      <li>基于历史数据进行趋势分析，为招新策略提供决策支持，优化渠道转化</li>
    </ul>
  </div>

  <!-- ==================== 荣誉奖项 ==================== -->
  <div class="section-title">
    <span class="emoji">🏆</span><span>荣誉奖项</span>
  </div>

  <table class="award-table">
    <thead>
      <tr>
        <th>奖项</th>
        <th style="width:140px;">时间</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="award-icon">🥈</span>第十三届 APMCM 亚太地区大学生数学建模竞赛决赛 <strong>二等奖</strong></td>
        <td>2023.12</td>
      </tr>
      <tr>
        <td><span class="award-icon">🥉</span>全国大学生数学建模竞赛广东省分赛 <strong>三等奖</strong></td>
        <td>2024.12</td>
      </tr>
    </tbody>
  </table>

  <!-- ==================== 专业技能 ==================== -->
  <div class="section-title">
    <span class="emoji">💻</span><span>专业技能</span>
  </div>

  <div class="skills-grid">
    <div class="skill-card">
      <div class="skill-name">🐍 Python</div>
      <p class="skill-desc">熟练使用 Pandas / NumPy / Scikit-learn，具备数据分析与机器学习建模能力</p>
    </div>
    <div class="skill-card">
      <div class="skill-name">🗄️ SQL</div>
      <p class="skill-desc">计算机三级水平，熟悉复杂查询与大规模数据提取</p>
    </div>
    <div class="skill-card">
      <div class="skill-name">📊 Excel</div>
      <p class="skill-desc">高级数据分析、VBA 自动化处理</p>
    </div>
    <div class="skill-card">
      <div class="skill-name">🌐 英语</div>
      <p class="skill-desc">CET-4 510+，可无障碍阅读英文技术文档与前沿论文</p>
    </div>
    <div class="skill-card">
      <div class="skill-name">📈 量化交易</div>
      <p class="skill-desc">自建回测框架与风险模型，持续探索量化策略</p>
    </div>
    <div class="skill-card">
      <div class="skill-name">🤖 数据科学</div>
      <p class="skill-desc">正在系统学习吴恩达机器学习等课程，持续精进</p>
    </div>
  </div>

  <!-- ==================== 底部联系 ==================== -->
  <div class="contact-footer">
    <div class="contact-footer-title">📬 期待与您的交流</div>
    <div class="contact-links">
      <a href="https://github.com/shuxue6662-a11y" target="_blank" class="contact-link github">
        <svg width="18" height="18" viewBox="0 0 16 16" fill="currentColor"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
        GitHub
      </a>
      <a href="mailto:zhsxue@163.com" class="contact-link email">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
        zhsxue@163.com
      </a>
    </div>
  </div>

</div>