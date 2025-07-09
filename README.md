<div class="clean-home">
  <!-- 三大核心模块 -->
  <div class="modules">
    <!-- 技术模块 -->
    <a href="./technology/" class="module tech">
      <div class="module-icon">
        <i class="fa fa-code"></i>
      </div>
      <h3>技术</h3>
      <div class="module-accent"></div>
    </a>

    <!-- 业务模块 -->
    <a href="./business/" class="module business">
      <div class="module-icon">
        <i class="fa fa-line-chart"></i>
      </div>
      <h3>业务</h3>
      <div class="module-accent"></div>
    </a>

    <!-- 工作日常模块 -->
    <a href="./daily/" class="module daily">
      <div class="module-icon">
        <i class="fa fa-calendar"></i>
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
  font-size: 2.5rem;
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