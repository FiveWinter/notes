---
home: true
heroImage: ./images/logo.svg  # 替换为你的logo（建议用简约线条风格）
heroText: 工作知识库
tagline: 技术沉淀 · 业务解析 · 日常记录
---

<!-- 首页主内容 -->
<div class="home-container">
  <!-- 头部引言 -->
  <div class="intro">
    <p>这里沉淀了工作中的技术思考、业务逻辑与日常总结，</p>
    <p>以系统化的方式梳理经验，助力高效协作与个人成长。</p>
  </div>

  <!-- 三大板块卡片 -->
  <div class="card-grid">
    <!-- 技术板块 -->
    <a href="./technology/" class="card tech-card">
      <div class="card-icon">
        <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <rect x="2" y="3" width="20" height="14" rx="2" ry="2"></rect>
          <line x1="8" y1="21" x2="16" y2="21"></line>
          <line x1="12" y1="17" x2="12" y2="21"></line>
        </svg>
      </div>
      <div class="card-content">
        <h3>技术</h3>
        <p>架构设计、代码实践、工具教程与技术选型思考，构建系统化技术认知。</p>
      </div>
      <div class="card-arrow">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <line x1="5" y1="12" x2="19" y2="12"></line>
          <polyline points="12 5 19 12 12 19"></polyline>
        </svg>
      </div>
    </a>

    <!-- 业务板块 -->
    <a href="./business/" class="card business-card">
      <div class="card-icon">
        <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2"></path>
          <rect x="8" y="2" width="8" height="4" rx="1" ry="1"></rect>
        </svg>
      </div>
      <div class="card-content">
        <h3>业务</h3>
        <p>业务流程拆解、需求分析、场景落地与商业模式思考，打通业务与技术的边界。</p>
      </div>
      <div class="card-arrow">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <line x1="5" y1="12" x2="19" y2="12"></line>
          <polyline points="12 5 19 12 12 19"></polyline>
        </svg>
      </div>
    </a>

    <!-- 工作日常板块 -->
    <a href="./daily/" class="card daily-card">
      <div class="card-icon">
        <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect>
          <line x1="16" y1="2" x2="16" y2="6"></line>
          <line x1="8" y1="2" x2="8" y2="6"></line>
          <line x1="3" y1="10" x2="21" y2="10"></line>
        </svg>
      </div>
      <div class="card-content">
        <h3>工作日常</h3>
        <p>工作计划、会议纪要、问题复盘与效率工具，记录成长轨迹与团队协作点滴。</p>
      </div>
      <div class="card-arrow">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <line x1="5" y1="12" x2="19" y2="12"></line>
          <polyline points="12 5 19 12 12 19"></polyline>
        </svg>
      </div>
    </a>
  </div>

  <!-- 底部装饰 -->
  <div class="footer-accent"></div>
</div>

<style>
/* 全局样式重置 */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* 首页容器 */
.home-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 60px 20px 100px;
  font-family: 'Inter', system-ui, -apple-system, sans-serif;
  color: #333;
  background: linear-gradient(180deg, #fafafa 0%, #f5f7fa 100%);
  min-height: 100vh;
}

/* 头部引言 */
.intro {
  text-align: center;
  margin-bottom: 80px;
  line-height: 1.8;
  font-size: 1.2rem;
  color: #666;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
}

/* 卡片网格布局 */
.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 40px;
  margin-bottom: 100px;
}

/* 卡片基础样式 */
.card {
  text-decoration: none;
  background: #fff;
  border-radius: 12px;
  padding: 40px 30px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

/* 卡片悬停效果 */
.card:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
}

/* 卡片图标 */
.card-icon {
  width: 80px;
  height: 80px;
  margin-bottom: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 16px;
  transition: all 0.3s ease;
}

/* 卡片标题 */
.card h3 {
  font-size: 1.6rem;
  font-weight: 600;
  margin-bottom: 15px;
  transition: color 0.3s ease;
}

/* 卡片描述 */
.card p {
  color: #777;
  line-height: 1.6;
  font-size: 1rem;
  margin-bottom: 30px;
}

/* 卡片箭头 */
.card-arrow {
  position: absolute;
  bottom: 30px;
  right: 30px;
  opacity: 0.7;
  transition: all 0.3s ease;
}

/* 技术卡片样式 */
.tech-card {
  border-top: 4px solid #3b82f6;
}
.tech-card .card-icon {
  background: rgba(59, 130, 246, 0.1);
  color: #3b82f6;
}
.tech-card:hover .card-icon {
  background: #3b82f6;
  color: white;
}
.tech-card h3 {
  color: #3b82f6;
}

/* 业务卡片样式 */
.business-card {
  border-top: 4px solid #10b981;
}
.business-card .card-icon {
  background: rgba(16, 185, 129, 0.1);
  color: #10b981;
}
.business-card:hover .card-icon {
  background: #10b981;
  color: white;
}
.business-card h3 {
  color: #10b981;
}

/* 日常卡片样式 */
.daily-card {
  border-top: 4px solid #f59e0b;
}
.daily-card .card-icon {
  background: rgba(245, 158, 11, 0.1);
  color: #f59e0b;
}
.daily-card:hover .card-icon {
  background: #f59e0b;
  color: white;
}
.daily-card h3 {
  color: #f59e0b;
}

/* 卡片悬停时文字颜色变化 */
.card:hover h3 {
  color: #222;
}
.card:hover .card-arrow {
  opacity: 1;
  transform: translateX(5px);
}

/* 底部装饰 */
.footer-accent {
  height: 3px;
  background: linear-gradient(90deg, #3b82f6, #10b981, #f59e0b);
  border-radius: 3px;
  max-width: 800px;
  margin: 0 auto;
  opacity: 0.8;
}

/* 响应式调整 */
@media (max-width: 768px) {
  .home-container {
    padding: 40px 20px 80px;
  }
  .intro {
    margin-bottom: 50px;
    font-size: 1rem;
  }
  .card-grid {
    gap: 30px;
  }
  .card {
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