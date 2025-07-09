<!-- 页面容器（居中布局） -->
<div class="page-center">
  <!-- 技术模块（代码符号图标） -->
  <div class="module-container">
    <a href="./technology/" class="module-link">
      <!-- 装饰层：第一个div -->
      <div class="decor">
        <div class="shine tech"></div>
      </div>
      <!-- 内容层：第二个div -->
      <div class="content tech">
        <div class="icon">
          <span class="code-symbol">&lt;/&gt;</span>
        </div>
        <h3>技术</h3>
        <div class="hover-indicator"></div>
      </div>
    </a>
  </div>

  <!-- 业务模块（保持不变） -->
  <div class="module-container">
    <a href="./business/" class="module-link">
      <!-- 装饰层：第一个div -->
      <div class="decor">
        <div class="shine business"></div>
      </div>
      <!-- 内容层：第二个div -->
      <div class="content business">
        <div class="icon">
          <div class="target-marker"></div>
        </div>
        <h3>业务</h3>
        <div class="hover-indicator"></div>
      </div>
    </a>
  </div>

  <!-- 工作日常模块（日历图标） -->
  <div class="module-container">
    <a href="./daily/" class="module-link">
      <!-- 装饰层：第一个div -->
      <div class="decor">
        <div class="shine daily"></div>
      </div>
      <!-- 内容层：第二个div -->
      <div class="content daily">
        <div class="icon">
          <div class="calendar-icon">
            <div class="cal-header"></div>
            <div class="cal-body">
              <span>15</span>
            </div>
          </div>
        </div>
        <h3>工作日常</h3>
        <div class="hover-indicator"></div>
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
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  background: #fafafa;
  font-family: 'Inter', sans-serif;
}

/* 居中容器 */
.page-center {
  display: flex;
  gap: 50px;
  width: 100%;
  max-width: 1000px;
  position: relative;
  height: 100%;
  display: flex;
}

.module-container {
  flex: 1;
  min-width: 250px;
  margin-top: auto;
  margin-bottom: auto;
}

.module-link {
  display: block;
  text-decoration: none;
  position: relative;
}

/* 装饰层（第一个div） */
.decor {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  pointer-events: none;
}

.shine {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 120%;
  height: 120%;
  transform: translate(-50%, -50%);
  border-radius: 50%;
  filter: blur(60px);
  opacity: 0.15;
  transition: all 0.6s ease;
}

/* 内容层（第二个div：卡片主体） */
.content {
  position: relative;
  padding: 60px 30px;
  border-radius: 20px;
  background: white;
  box-shadow: 
    0 4px 20px rgba(0,0,0,0.03),
    0 1px 3px rgba(0,0,0,0.02);
  transition: all 0.5s cubic-bezier(0.2, 0.8, 0.2, 1);
  z-index: 2;
  border: 1px solid rgba(0,0,0,0.05);
  height: 100%;
}

/* 图标容器 */
.icon {
  width: 80px;
  height: 80px;
  margin: 0 auto 35px;
  border-radius: 16px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.5s ease;
}

/* 标题样式 */
.content h3 {
  font-size: 1.8rem;
  font-weight: 500;
  color: #333;
  text-align: center;
  margin-bottom: 25px;
  transition: all 0.4s ease;
}

/* 底部指示器 */
.hover-indicator {
  width: 40px;
  height: 3px;
  margin: 0 auto;
  border-radius: 2px;
  transition: all 0.5s ease;
}

/* 技术模块（代码符号图标） */
.shine.tech { background: #3b82f6; }
.content.tech .icon { background: #f0f7ff; }
.code-symbol {
  font-family: 'Consolas', monospace;
  font-size: 2.6rem;
  font-weight: bold;
  color: #3b82f6;
}
.content.tech .hover-indicator { background: #3b82f6; }

/* 业务模块（保持不变） */
.shine.business { background: #10b981; }
.content.business .icon { background: #f0fff4; }
.target-marker {
  width: 36px;
  height: 36px;
  position: relative;
}
.target-marker::before {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  width: 28px;
  height: 28px;
  transform: translate(-50%, -50%);
  border: 3px solid #10b981;
  border-radius: 50%;
  opacity: 0.7;
}
.target-marker::after {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  width: 12px;
  height: 12px;
  transform: translate(-50%, -50%);
  background: #10b981;
  border-radius: 50%;
}
.content.business .hover-indicator { background: #10b981; }

/* 工作日常模块（日历图标） */
.shine.daily { background: #f97316; }
.content.daily .icon { background: #fff8f0; }
.calendar-icon {
  width: 36px;
  height: 36px;
  position: relative;
}
.cal-header {
  width: 36px;
  height: 8px;
  background: #f97316;
  border-radius: 3px 3px 0 0;
}
.cal-body {
  width: 36px;
  height: 28px;
  border: 2px solid #f97316;
  border-radius: 0 0 3px 3px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.cal-body span {
  font-size: 1.1rem;
  font-weight: 500;
  color: #f97316;
}
.content.daily .hover-indicator { background: #f97316; }

/* 悬停交互效果 */
.module-link:hover .content {
  transform: translateY(-10px) scale(1.02);
  box-shadow: 
    0 15px 35px rgba(0,0,0,0.06),
    0 5px 10px rgba(0,0,0,0.03);
  border-color: rgba(0,0,0,0.08);
}

.module-link:hover .icon {
  transform: scale(1.1) rotate(-3deg);
  box-shadow: 0 5px 15px rgba(59, 130, 246, 0.1);
}

.module-link:hover .content h3 {
  color: #111;
  letter-spacing: 0.5px;
}

.module-link:hover .hover-indicator {
  width: 70px;
}

.module-link:hover .shine {
  opacity: 0.25;
  transform: translate(-50%, -50%) scale(1.2);
}

/* 响应式（保持居中） */
@media (max-width: 768px) {
  .page-center {
    flex-direction: column;
    gap: 40px;
    padding: 50px 20px;
  }
  
  .module-container {
    width: 100%;
    max-width: 300px;
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

.markdown-section{
  height: 100%;
}
</style>