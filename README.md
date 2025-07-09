---
home: true
heroText: 工作知识库
tagline: 技术沉淀 · 业务解析 · 日常记录
---

<!-- 极简风格首页 -->
<div class="minimal-home">
  <!-- 顶部标题区 -->
  <div class="header">
    <h1>工作知识库</h1>
    <p class="subtitle">探索知识边界，记录成长轨迹</p>
  </div>

  <!-- 三大板块 -->
  <div class="sections-container">
    <!-- 技术板块 -->
    <a href="./technology/" class="section-link">
      <div class="section">
        <div class="section-icon">
          <i class="fa fa-code"></i>
        </div>
        <h2>技术</h2>
        <p>架构设计、代码实践、工具教程与技术选型思考</p>
      </div>
    </a>
    
    <!-- 业务板块 -->
    <a href="./business/" class="section-link">
      <div class="section">
        <div class="section-icon">
          <i class="fa fa-line-chart"></i>
        </div>
        <h2>业务</h2>
        <p>业务流程拆解、需求分析、场景落地与商业模式思考</p>
      </div>
    </a>
    
    <!-- 工作日常板块 -->
    <a href="./daily/" class="section-link">
      <div class="section">
        <div class="section-icon">
          <i class="fa fa-calendar"></i>
        </div>
        <h2>工作日常</h2>
        <p>工作计划、会议纪要、问题复盘与效率工具</p>
      </div>
    </a>
  </div>

  <!-- 底部信息 -->
  <div class="footer">
    <p>© 2025 工作知识库 | 持续更新中</p>
  </div>
</div>

<style>
/* 全局样式重置 */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Inter', sans-serif;
}

/* 首页容器 */
.minimal-home {
  background-color: #ffffff;
  min-height: 100vh;
  color: #333;
  display: flex;
  flex-direction: column;
}

/* 顶部标题区 */
.header {
  text-align: center;
  padding: 80px 20px 60px;
}

.header h1 {
  font-size: 2.5rem;
  font-weight: 600;
  margin-bottom: 20px;
  color: #222;
}

.subtitle {
  font-size: 1.2rem;
  color: #666;
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.6;
}

/* 三大板块容器 */
.sections-container {
  max-width: 1000px;
  margin: 0 auto;
  padding: 0 20px 100px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
}

/* 板块链接 */
.section-link {
  text-decoration: none;
  color: inherit;
  transition: all 0.3s ease;
}

/* 板块卡片 */
.section {
  padding: 40px 30px;
  border-radius: 12px;
  border: 1px solid #e2e8f0;
  text-align: center;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

/* 板块图标 */
.section-icon {
  font-size: 2.5rem;
  margin-bottom: 25px;
  color: #3b82f6;
  transition: all 0.3s ease;
}

/* 板块标题 */
.section h2 {
  font-size: 1.5rem;
  font-weight: 500;
  margin-bottom: 15px;
  color: #222;
}

/* 板块描述 */
.section p {
  color: #666;
  line-height: 1.6;
}

/* 悬停效果 */
.section-link:hover {
  transform: translateY(-5px);
}

.section:hover {
  box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.05), 0 10px 10px -5px rgba(0, 0, 0, 0.01);
  border-color: #cbd5e1;
}

.section:hover .section-icon {
  transform: scale(1.1);
  color: #1d4ed8;
}

/* 底部信息 */
.footer {
  text-align: center;
  padding: 20px;
  color: #94a3b8;
  font-size: 0.9rem;
  margin-top: auto;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .sections-container {
    grid-template-columns: 1fr;
    gap: 30px;
  }
  
  .header {
    padding: 60px 20px 40px;
  }
  
  .header h1 {
    font-size: 2rem;
  }
  
  .subtitle {
    font-size: 1rem;
  }
  
  .section {
    padding: 30px 20px;
  }
}

.content {
  margin-left: 0px;
  left: 0px;
}
.sidebar-toggle{
    display: none;
}
.sidebar{
    display: none;
}
</style>