<div class="clean-home">
  <!-- 三大核心模块 -->
  <div class="modules">
    <!-- 技术模块 -->
    <a href="./technology/" class="module tech">
      <div class="module-icon">
        <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <rect x="2" y="3" width="20" height="14" rx="2" ry="2"></rect>
          <line x1="8" y1="21" x2="16" y2="21"></line>
          <line x1="12" y1="17" x2="12" y2="21"></line>
        </svg>
      </div>
      <h3>技术</h3>
      <div class="module-accent"></div>
    </a>

    <!-- 业务模块 -->
    <a href="./business/" class="module business">
      <div class="module-icon">
        <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2"></path>
          <rect x="8" y="2" width="8" height="4" rx="1" ry="1"></rect>
        </svg>
      </div>
      <h3>业务</h3>
      <div class="module-accent"></div>
    </a>

    <!-- 工作日常模块 -->
    <a href="./daily/" class="module daily">
      <div class="module-icon">
        <svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect>
          <line x1="16" y1="2" x2="16" y2="6"></line>
          <line x1="8" y1="2" x2="8" y2="6"></line>
          <line x1="3" y1="10" x2="21" y2="10"></line>
        </svg>
      </div>
      <h3>工作日常</h3>
      <div class="module-accent"></div>
    </a>
  </div>

  <!-- 底部装饰 -->
  <div class="footer-dot"></div>
</div>

<style>
/* 全局样式 */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: #ffffff;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 20px;
}

/* 容器 */
.clean-home {
  width: 100%;
  max-width: 1000px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* 模块容器 */
.modules {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 60px;
  width: 100%;
  margin-bottom: 80px;
}

/* 单个模块 */
.module {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-decoration: none;
  padding: 40px 20px;
  border-radius: 16px;
  transition: all 0.3s ease;
  position: relative;
}

/* 模块图标 */
.module-icon {
  margin-bottom: 30px;
  transition: all 0.3s ease;
}

/* 模块标题 */
.module h3 {
  font-family: 'Inter', sans-serif;
  font-size: 1.4rem;
  font-weight: 500;
  transition: all 0.3s ease;
}

/* 模块底部装饰条 */
.module-accent {
  width: 40px;
  height: 3px;
  border-radius: 3px;
  margin-top: 25px;
  transition: all 0.3s ease;
}

/* 配色方案 */
.tech .module-icon,
.tech h3 {
  color: #4f46e5; /* 深紫蓝 */
}
.tech .module-accent {
  background: #4f46e5;
}

.business .module-icon,
.business h3 {
  color: #0ea5e9; /* 天青蓝 */
}
.business .module-accent {
  background: #0ea5e9;
}

.daily .module-icon,
.daily h3 {
  color: #f97316; /* 暖橙色 */
}
.daily .module-accent {
  background: #f97316;
}

/* 悬停效果 */
.module:hover {
  background: #fafafa;
  transform: translateY(-8px);
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.03);
}

.module:hover .module-icon {
  transform: scale(1.1);
}

.module:hover .module-accent {
  width: 60px;
}

/* 底部装饰点 */
.footer-dot {
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: #e5e7eb;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .modules {
    grid-template-columns: 1fr;
    gap: 40px;
    margin-bottom: 60px;
  }

  .module {
    padding: 30px 20px;
  }

  .module-icon {
    margin-bottom: 25px;
  }

  .module h3 {
    font-size: 1.3rem;
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