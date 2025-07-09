<!-- 页面主容器 -->
<div class="page-wrapper">
  <!-- 技术模块（代码符号图标） -->
  <div class="module-container">
    <a href="./technology/" class="module tech">
      <div class="module-content">
        <div class="icon tech-icon">
          <div class="code-symbol">
            <span>&lt;/&gt;</span>
          </div>
        </div>
        <h3>技术</h3>
      </div>
    </a>
  </div>

  <!-- 业务模块（保持不变） -->
  <div class="module-container">
    <a href="./business/" class="module business">
      <div class="module-content">
        <div class="icon business-icon">
          <div class="target-ring"></div>
          <div class="target-core"></div>
        </div>
        <h3>业务</h3>
      </div>
    </a>
  </div>

  <!-- 工作日常模块（日历图标） -->
  <div class="module-container">
    <a href="./daily/" class="module daily">
      <div class="module-content">
        <div class="icon daily-icon">
          <div class="calendar">
            <div class="calendar-header"></div>
            <div class="calendar-body">
              <span>15</span>
            </div>
          </div>
        </div>
        <h3>工作日常</h3>
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
  padding: 40px 20px;
  font-family: 'Inter', sans-serif;
}

.page-wrapper {
  display: flex;
  gap: 50px;
  max-width: 1100px;
  width: 100%;
}

.module-container {
  flex: 1;
  min-width: 250px;
}

.module {
  display: block;
  text-decoration: none;
}

.module-content {
  padding: 50px 30px;
  border-radius: 18px;
  border: 1px solid #f0f0f0;
  box-shadow: 0 2px 10px rgba(0,0,0,0.01);
  transition: all 0.4s ease;
  background: white;
  position: relative;
  overflow: hidden;
}

.icon {
  width: 80px;
  height: 80px;
  margin: 0 auto 35px;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.4s ease;
  position: relative;
}

/* 技术图标（代码符号 &lt;/&gt;） */
.tech-icon {
  background: #f0f7ff;
}
.code-symbol span {
  font-family: 'Consolas', monospace;
  font-size: 2.2rem;
  font-weight: bold;
  color: #3b82f6;
}

/* 业务图标（保持不变） */
.business-icon {
  background: #f0fff4;
  position: relative;
}
.target-ring {
  width: 36px;
  height: 36px;
  border: 3px solid #10b981;
  border-radius: 50%;
  opacity: 0.6;
}
.target-core {
  position: absolute;
  width: 12px;
  height: 12px;
  background: #10b981;
  border-radius: 50%;
}

/* 工作日常图标（日历） */
.daily-icon {
  background: #fff8f0;
}
.calendar {
  width: 36px;
  height: 36px;
  position: relative;
}
.calendar-header {
  width: 36px;
  height: 8px;
  background: #f97316;
  border-radius: 3px 3px 0 0;
}
.calendar-body {
  width: 36px;
  height: 28px;
  border: 2px solid #f97316;
  border-radius: 0 0 3px 3px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.calendar-body span {
  font-size: 1rem;
  font-weight: 500;
  color: #f97316;
}

/* 标题样式 */
.module h3 {
  font-size: 1.6rem;
  font-weight: 500;
  color: #222;
  text-align: center;
  margin-bottom: 15px;
  transition: color 0.3s ease;
}

/* 配色方案 */
.tech .module-content { border-color: #e6f2ff; }
.business .module-content { border-color: #e6f9ec; }
.daily .module-content { border-color: #fff0e0; }

/* 悬停交互效果 */
.module:hover .module-content {
  transform: translateY(-10px);
  box-shadow: 0 15px 30px rgba(0,0,0,0.05), 0 8px 15px rgba(0,0,0,0.02);
  border-color: #e8e8e8;
}

.module:hover .icon { transform: scale(1.1); }
.module:hover h3 { color: #111; }

/* 卡片内部光效 */
.module-content::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 0;
  opacity: 0;
  transition: all 0.4s ease;
  pointer-events: none;
}

.tech .module-content::after { background: linear-gradient(to top, rgba(59, 130, 246, 0.05), transparent); }
.business .module-content::after { background: linear-gradient(to top, rgba(16, 185, 129, 0.05), transparent); }
.daily .module-content::after { background: linear-gradient(to top, rgba(249, 115, 22, 0.05), transparent); }

.module:hover .module-content::after { height: 40%; opacity: 1; }

/* 响应式设计 */
@media (max-width: 850px) {
  .page-wrapper { flex-direction: column; gap: 40px; padding: 30px 20px; }
  .module-content { padding: 45px 20px; }
  .module h3 { font-size: 1.4rem; }
}
</style>