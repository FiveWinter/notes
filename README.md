---
home: true
heroImage: ./images/logo.svg  # 替换为你的logo
heroText: 专业知识库
tagline: 技术沉淀 | 业务洞察 | 工作日常
---

<!-- 深色科技风格首页 -->
<div class="dark-home">
  <!-- 顶部导航栏 -->
  <div class="header">
    <div class="logo">
      <img src="./images/logo.svg" alt="Logo" />
      <span>工作知识库</span>
    </div>
  </div>

  <!-- 主内容区 -->
  <div class="content-wrapper">
    <h1 class="title">探索知识边界</h1>
    <p class="subtitle">汇聚技术、业务与日常工作的智慧结晶</p>
    
    <!-- 三大板块 -->
    <div class="sections-grid">
      <!-- 技术板块 -->
      <a href="./technology/" class="section-card tech-card">
        <div class="card-content">
          <div class="card-icon">
            <i class="fa fa-code"></i>
          </div>
          <h3>技术</h3>
          <p>架构设计、开发实践、前沿技术探索</p>
        </div>
        <div class="card-overlay"></div>
      </a>
      
      <!-- 业务板块 -->
      <a href="./business/" class="section-card business-card">
        <div class="card-content">
          <div class="card-icon">
            <i class="fa fa-line-chart"></i>
          </div>
          <h3>业务</h3>
          <p>商业模式、产品策略、市场分析</p>
        </div>
        <div class="card-overlay"></div>
      </a>
      
      <!-- 工作日常板块 -->
      <a href="./daily/" class="section-card daily-card">
        <div class="card-content">
          <div class="card-icon">
            <i class="fa fa-calendar"></i>
          </div>
          <h3>工作日常</h3>
          <p>项目管理、团队协作、经验分享</p>
        </div>
        <div class="card-overlay"></div>
      </a>
    </div>
    
    <!-- 底部信息 -->
    <div class="footer">
      <p>© 2025 工作知识库 | 持续更新中</p>
    </div>
  </div>
</div>

<style>
/* 全局样式 */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Inter', sans-serif;
}

/* 深色背景 */
.dark-home {
  background: #121826;
  min-height: 100vh;
  color: #fff;
}

/* 顶部导航栏 */
.header {
  padding: 30px 50px;
  display: flex;
  align-items: center;
}

.logo {
  display: flex;
  align-items: center;
}

.logo img {
  height: 30px;
  margin-right: 15px;
}

.logo span {
  font-size: 1.2rem;
  font-weight: 500;
  background: linear-gradient(90deg, #647dee, #7f53ac);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

/* 主内容区 */
.content-wrapper {
  max-width: 1200px;
  margin: 0 auto;
  padding: 50px 30px;
  text-align: center;
}

.title {
  font-size: 2.5rem;
  font-weight: 600;
  margin-bottom: 20px;
  background: linear-gradient(90deg, #3b82f6, #8b5cf6);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.subtitle {
  font-size: 1.2rem;
  color: #94a3b8;
  margin-bottom: 80px;
}

/* 三大板块网格 */
.sections-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
}

/* 板块卡片 */
.section-card {
  position: relative;
  height: 300px;
  border-radius: 16px;
  overflow: hidden;
  text-decoration: none;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
  transition: all 0.4s ease;
}

.section-card:hover {
  transform: translateY(-10px);
}

.card-content {
  position: relative;
  z-index: 2;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 30px;
}

.card-icon {
  font-size: 3rem;
  margin-bottom: 20px;
  transition: transform 0.3s ease;
}

.section-card:hover .card-icon {
  transform: scale(1.1);
}

.section-card h3 {
  font-size: 1.5rem;
  font-weight: 500;
  margin-bottom: 15px;
}

.section-card p {
  color: #cbd5e1;
  text-align: center;
  line-height: 1.6;
}

/* 卡片背景渐变 */
.card-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  transition: all 0.4s ease;
}

.tech-card .card-overlay {
  background: linear-gradient(135deg, #3b82f6 0%, #2563eb 100%);
}

.business-card .card-overlay {
  background: linear-gradient(135deg, #10b981 0%, #059669 100%);
}

.daily-card .card-overlay {
  background: linear-gradient(135deg, #f59e0b 0%, #d97706 100%);
}

/* 卡片悬停效果 */
.tech-card:hover .card-overlay {
  background: linear-gradient(135deg, #2563eb 0%, #1d4ed8 100%);
}

.business-card:hover .card-overlay {
  background: linear-gradient(135deg, #059669 0%, #047857 100%);
}

.daily-card:hover .card-overlay {
  background: linear-gradient(135deg, #d97706 0%, #b45309 100%);
}

/* 底部信息 */
.footer {
  margin-top: 100px;
  padding: 20px;
  color: #64748b;
  font-size: 0.9rem;
}

/* 响应式设计 */
@media (max-width: 992px) {
  .sections-grid {
    grid-template-columns: 1fr;
    gap: 30px;
  }
  
  .title {
    font-size: 2rem;
  }
  
  .subtitle {
    font-size: 1rem;
    margin-bottom: 50px;
  }
  
  .section-card {
    height: 250px;
  }
  
  .header {
    padding: 20px 30px;
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