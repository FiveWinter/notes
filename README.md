<div class="page-container">
  <!-- 技术模块容器 -->
  <div class="module-container">
    <a href="./technology/" class="module tech">
      <div class="icon">💻</div>
      <h2>技术</h2>
    </a>
  </div>

  <!-- 业务模块容器 -->
  <div class="module-container">
    <a href="./business/" class="module business">
      <div class="icon">📊</div>
      <h2>业务</h2>
    </a>
  </div>

  <!-- 工作日常模块容器 -->
  <div class="module-container">
    <a href="./daily/" class="module daily">
      <div class="icon">📅</div>
      <h2>工作日常</h2>
    </a>
  </div>
</div>

<style>
/* 基础样式重置 */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* 页面容器 */
.page-container {
  background: white;
  min-height: 100vh;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
  padding: 60px 20px;
  max-width: 1000px;
  margin: 0 auto;
}

/* 模块容器（每个div只包含一个a标签） */
.module-container {
  width: 100%;
}

/* 模块链接样式 */
.module {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  padding: 50px 20px;
  border-radius: 12px;
  text-decoration: none;
  transition: all 0.3s ease;
}

/* 图标样式 */
.icon {
  font-size: 3rem;
  margin-bottom: 25px;
  transition: transform 0.3s ease;
}

/* 标题样式 */
.module h2 {
  font-family: 'Inter', sans-serif;
  font-size: 1.5rem;
  font-weight: 500;
}

/* 技术模块配色 */
.tech {
  color: #3b82f6;
  border: 1px solid #eff6ff;
}
.tech:hover {
  background: #f0f9ff;
  box-shadow: 0 8px 16px rgba(59, 130, 246, 0.05);
}
.tech:hover .icon {
  transform: scale(1.1);
}

/* 业务模块配色 */
.business {
  color: #10b981;
  border: 1px solid #ecfdf5;
}
.business:hover {
  background: #f0fdf4;
  box-shadow: 0 8px 16px rgba(16, 185, 129, 0.05);
}
.business:hover .icon {
  transform: scale(1.1);
}

/* 工作日常模块配色 */
.daily {
  color: #f97316;
  border: 1px solid #fff7ed;
}
.daily:hover {
  background: #fff7ed;
  box-shadow: 0 8px 16px rgba(249, 115, 22, 0.05);
}
.daily:hover .icon {
  transform: scale(1.1);
}

/* 响应式布局 */
@media (max-width: 768px) {
  .page-container {
    grid-template-columns: 1fr;
    gap: 25px;
    padding: 40px 20px;
  }
  
  .module {
    padding: 40px 20px;
  }
  
  .icon {
    font-size: 2.5rem;
    margin-bottom: 20px;
  }
  
  .module h2 {
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