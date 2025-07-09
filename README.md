<!-- 容器 -->
<div class="modules-wrapper">
  <!-- 技术模块 -->
  <div class="module-item">
    <a href="./technology/" class="module tech">
      <div class="module-inner">
        <div class="module-icon">
          <div class="icon-shape"></div>
        </div>
        <h3>技术</h3>
        <div class="module-line"></div>
      </div>
    </a>
  </div>

  <!-- 业务模块 -->
  <div class="module-item">
    <a href="./business/" class="module business">
      <div class="module-inner">
        <div class="module-icon">
          <div class="icon-shape"></div>
        </div>
        <h3>业务</h3>
        <div class="module-line"></div>
      </div>
    </a>
  </div>

  <!-- 工作日常模块 -->
  <div class="module-item">
    <a href="./daily/" class="module daily">
      <div class="module-inner">
        <div class="module-icon">
          <div class="icon-shape"></div>
        </div>
        <h3>工作日常</h3>
        <div class="module-line"></div>
      </div>
    </a>
  </div>
</div>

<style>
/* 基础样式 */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: #ffffff;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 30px;
}

/* 模块容器 */
.modules-wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 50px;
  width: 100%;
  max-width: 1000px;
}

.module-item {
  width: 100%;
}

/* 模块链接样式 */
.module {
  display: block;
  text-decoration: none;
}

.module-inner {
  position: relative;
  padding: 50px 30px;
  text-align: center;
  border-radius: 16px;
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  border: 1px solid #f1f5f9;
}

/* 图标容器 */
.module-icon {
  width: 80px;
  height: 80px;
  margin: 0 auto 35px;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
}

/* 几何图标 */
.icon-shape {
  width: 30px;
  height: 30px;
  transition: all 0.3s ease;
}

/* 标题样式 */
.module h3 {
  font-family: 'Inter', sans-serif;
  font-size: 1.5rem;
  font-weight: 500;
  margin-bottom: 25px;
  transition: all 0.3s ease;
}

/* 底部装饰线 */
.module-line {
  width: 30px;
  height: 2px;
  border-radius: 1px;
  margin: 0 auto;
  transition: all 0.3s ease;
}

/* 技术模块配色 */
.tech .module-icon {
  background: #f0f9ff;
}
.tech .icon-shape {
  background: #3b82f6;
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%); /* 钻石形 */
}
.tech h3 {
  color: #1e40af;
}
.tech .module-line {
  background: #3b82f6;
}

/* 业务模块配色 */
.business .module-icon {
  background: #f0fdf4;
}
.business .icon-shape {
  background: #10b981;
  border-radius: 6px; /* 矩形 */
}
.business h3 {
  color: #065f46;
}
.business .module-line {
  background: #10b981;
}

/* 工作日常模块配色 */
.daily .module-icon {
  background: #fff7ed;
}
.daily .icon-shape {
  background: #f97316;
  border-radius: 50%; /* 圆形 */
}
.daily h3 {
  color: #c2410c;
}
.daily .module-line {
  background: #f97316;
}

/* 悬停交互效果 */
.module:hover .module-inner {
  transform: translateY(-8px);
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.05);
  border-color: #e2e8f0;
}
.module:hover .module-icon {
  transform: scale(1.05);
}
.module:hover .module-line {
  width: 50px;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .modules-wrapper {
    grid-template-columns: 1fr;
    gap: 30px;
  }
  .module-inner {
    padding: 40px 20px;
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