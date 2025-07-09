<!-- 页面主容器 -->
<div class="page-wrapper">
  <!-- 装饰元素 -->
  <div class="decor-top"></div>
  <div class="decor-bottom"></div>

  <!-- 技术模块 -->
  <div class="module-container">
    <a href="./technology/" class="module tech">
      <div class="module-bg"></div> <!-- 背景纹理 -->
      <div class="module-content">
        <div class="corner-mark"></div> <!-- 角落装饰 -->
        <div class="icon tech-icon">
          <!-- 技术图标：代码片段 -->
          <div class="code-line"></div>
          <div class="code-line"></div>
          <div class="code-line"></div>
        </div>
        <h3>技术</h3>
        <div class="glow-line"></div> <!-- 光效线条 -->
      </div>
    </a>
  </div>

  <!-- 业务模块 -->
  <div class="module-container">
    <a href="./business/" class="module business">
      <div class="module-bg"></div>
      <div class="module-content">
        <div class="corner-mark"></div>
        <div class="icon business-icon">
          <!-- 业务图标：柱状图表 -->
          <div class="bar bar-1"></div>
          <div class="bar bar-2"></div>
          <div class="bar bar-3"></div>
        </div>
        <h3>业务</h3>
        <div class="glow-line"></div>
      </div>
    </a>
  </div>

  <!-- 工作日常模块 -->
  <div class="module-container">
    <a href="./daily/" class="module daily">
      <div class="module-bg"></div>
      <div class="module-content">
        <div class="corner-mark"></div>
        <div class="icon daily-icon">
          <!-- 日常图标：日历 -->
          <div class="calendar-top"></div>
          <div class="calendar-grid">
            <span></span><span></span><span></span>
            <span></span><span></span><span></span>
            <span></span><span></span><span></span>
          </div>
        </div>
        <h3>工作日常</h3>
        <div class="glow-line"></div>
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
  position: relative;
  overflow-x: hidden;
}

/* 顶部/底部装饰 */
.decor-top, .decor-bottom {
  position: absolute;
  width: 100%;
  height: 4px;
  background: linear-gradient(90deg, transparent, #3b82f6, #10b981, #f97316, transparent);
  z-index: 1;
}
.decor-top { top: 0; }
.decor-bottom { bottom: 0; }

/* 主容器 */
.page-wrapper {
  display: flex;
  gap: 50px;
  position: relative;
  z-index: 2;
  max-width: 1100px;
  width: 100%;
}

/* 模块容器 */
.module-container {
  flex: 1;
  min-width: 250px;
}

/* 模块链接 */
.module {
  display: block;
  text-decoration: none;
  position: relative;
}

/* 模块背景纹理（微妙点阵） */
.module-bg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: radial-gradient(rgba(0,0,0,0.03) 1px, transparent 1px);
  background-size: 20px 20px;
  border-radius: 18px;
  z-index: 1;
}

/* 模块内容区 */
.module-content {
  position: relative;
  padding: 50px 30px;
  border-radius: 18px;
  border: 1px solid #f0f0f0;
  box-shadow: 0 2px 10px rgba(0,0,0,0.01);
  transition: all 0.4s ease;
  z-index: 2;
}

/* 角落装饰 */
.corner-mark {
  position: absolute;
  top: 20px;
  right: 20px;
  width: 12px;
  height: 12px;
  border-radius: 3px;
  transition: all 0.3s ease;
}

/* 图标容器 */
.icon {
  width: 80px;
  height: 80px;
  margin: 0 auto 35px;
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 6px;
  transition: all 0.4s ease;
}

/* 技术图标（代码片段） */
.tech-icon {
  background: #f0f7ff;
}
.code-line {
  width: 40px;
  height: 4px;
  background: #3b82f6;
  border-radius: 2px;
}
.code-line:nth-child(2) { width: 30px; }
.code-line:nth-child(3) { width: 35px; }

/* 业务图标（柱状图表） */
.business-icon {
  background: #f0fff4;
}
.bar {
  width: 8px;
  background: #10b981;
  border-radius: 3px;
}
.bar-1 { height: 30px; }
.bar-2 { height: 45px; margin: 0 6px; }
.bar-3 { height: 25px; }

/* 工作日常图标（日历） */
.daily-icon {
  background: #fff8f0;
}
.calendar-top {
  width: 40px;
  height: 6px;
  background: #f97316;
  border-radius: 3px;
  margin-bottom: 8px;
}
.calendar-grid {
  display: grid;
  grid-template-columns: repeat(3, 8px);
  gap: 4px;
}
.calendar-grid span {
  width: 8px;
  height: 8px;
  background: #f97316;
  border-radius: 2px;
}

/* 标题样式 */
.module h3 {
  font-size: 1.6rem;
  font-weight: 500;
  color: #222;
  text-align: center;
  margin-bottom: 25px;
  transition: color 0.3s ease;
}

/* 底部光效线条 */
.glow-line {
  width: 40px;
  height: 3px;
  margin: 0 auto;
  border-radius: 3px;
  transition: all 0.4s ease;
}

/* 配色方案 */
.tech .corner-mark { background: #3b82f6; opacity: 0.2; }
.tech .glow-line { 
  background: #3b82f6;
  box-shadow: 0 0 10px rgba(59, 130, 246, 0.3);
}

.business .corner-mark { background: #10b981; opacity: 0.2; }
.business .glow-line { 
  background: #10b981;
  box-shadow: 0 0 10px rgba(16, 185, 129, 0.3);
}

.daily .corner-mark { background: #f97316; opacity: 0.2; }
.daily .glow-line { 
  background: #f97316;
  box-shadow: 0 0 10px rgba(249, 115, 22, 0.3);
}

/* 悬停交互效果 */
.module:hover .module-content {
  transform: translateY(-10px);
  box-shadow: 0 15px 30px rgba(0,0,0,0.05), 0 8px 15px rgba(0,0,0,0.02);
  border-color: #e8e8e8;
}

.module:hover .icon {
  transform: scale(1.1);
}

.module:hover .corner-mark {
  transform: rotate(10deg);
  opacity: 0.4;
}

.module:hover h3 {
  color: #111;
}

.module:hover .glow-line {
  width: 60px;
  box-shadow: 0 0 15px rgba(59, 130, 246, 0.4); /* 增强光效 */
}

/* 响应式设计 */
@media (max-width: 850px) {
  .page-wrapper {
    flex-direction: column;
    gap: 40px;
    padding: 30px 20px;
  }
  
  .module-content {
    padding: 45px 20px;
  }
  
  .module h3 {
    font-size: 1.4rem;
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