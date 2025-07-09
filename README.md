<!-- 页面主容器 -->
<div class="page-wrapper">
  <!-- 技术模块 -->
  <div class="module-container">
    <a href="./technology/" class="module-link">
      <!-- 装饰层：第一个div -->
      <div class="decor-layer">
        <div class="corner-ornament tech"></div>
        <div class="subtle-pattern"></div>
      </div>
      <!-- 内容层：第二个div -->
      <div class="content-layer tech">
        <div class="icon-holder">
          <span class="code-icon">&lt;/&gt;</span>
        </div>
        <h3>技术</h3>
        <div class="bottom-glow"></div>
      </div>
    </a>
  </div>

  <!-- 业务模块 -->
  <div class="module-container">
    <a href="./business/" class="module-link">
      <div class="decor-layer">
        <div class="corner-ornament business"></div>
        <div class="subtle-pattern"></div>
      </div>
      <div class="content-layer business">
        <div class="icon-holder">
          <div class="target-ring"></div>
          <div class="target-dot"></div>
        </div>
        <h3>业务</h3>
        <div class="bottom-glow"></div>
      </div>
    </a>
  </div>

  <!-- 工作日常模块 -->
  <div class="module-container">
    <a href="./daily/" class="module-link">
      <!-- 装饰层：第一个div -->
      <div class="decor-layer">
        <div class="corner-ornament daily"></div>
        <div class="subtle-pattern"></div>
      </div>
      <!-- 内容层：第二个div -->
      <div class="content-layer daily">
        <div class="icon-holder">
          <div class="calendar-frame">
            <div class="calendar-top"></div>
            <div class="calendar-date">15</div>
          </div>
        </div>
        <h3>工作日常</h3>
        <div class="bottom-glow"></div>
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
  background: #fefefe;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 40px 20px;
  font-family: 'Inter', sans-serif;
}

.page-wrapper {
  display: flex;
  gap: 70px;
  max-width: 1400px;
  width: 100%;
  position: relative;
}

.module-container {
  flex: 1;
  min-width: 320px;
}

.module-link {
  display: block;
  text-decoration: none;
  position: relative;
}

/* 装饰层样式 */
.decor-layer {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  pointer-events: none;
}

/* 角落装饰 */
.corner-ornament {
  position: absolute;
  top: 25px;
  right: 25px;
  width: 22px;
  height: 22px;
  border-radius: 6px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  transition: all 0.5s cubic-bezier(0.2, 0.8, 0.2, 1);
  opacity: 0.2;
}

/* 背景纹理 */
.subtle-pattern {
  width: 100%;
  height: 100%;
  background-image: 
    radial-gradient(rgba(0,0,0,0.02) 1px, transparent 1px),
    radial-gradient(rgba(0,0,0,0.01) 1px, transparent 1px);
  background-size: 50px 50px;
  background-position: 0 0, 25px 25px;
}

/* 内容层样式（卡片主体） */
.content-layer {
  position: relative;
  padding: 80px 40px;
  border-radius: 24px;
  border: 1px solid #f0f0f0;
  background: linear-gradient(180deg, white 0%, #fcfcfc 100%);
  box-shadow: 
    0 8px 20px rgba(0,0,0,0.02),
    0 2px 5px rgba(0,0,0,0.01);
  transition: all 0.5s cubic-bezier(0.2, 0.8, 0.2, 1);
  z-index: 2;
  overflow: hidden;
}

/* 图标容器 */
.icon-holder {
  width: 110px;
  height: 110px;
  margin: 0 auto 55px;
  border-radius: 18px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.5s ease;
  position: relative;
  box-shadow: 0 4px 15px rgba(0,0,0,0.03);
}

/* 标题样式 */
.content-layer h3 {
  font-size: 2.2rem;
  font-weight: 500;
  color: #222;
  text-align: center;
  margin-bottom: 40px;
  transition: all 0.4s ease;
  position: relative;
  z-index: 2;
}

/* 底部光效 */
.bottom-glow {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 30%;
  opacity: 0;
  transition: all 0.6s ease;
  z-index: 1;
}

/* 技术模块配色 */
.corner-ornament.tech { background: #3b82f6; }
.content-layer.tech { border-color: #e6f2ff; }
.content-layer.tech .icon-holder { background: #f0f7ff; }
.code-icon {
  font-family: 'Consolas', monospace;
  font-size: 3rem;
  color: #3b82f6;
  font-weight: bold;
}
.content-layer.tech .bottom-glow {
  background: linear-gradient(to top, rgba(59, 130, 246, 0.1), transparent);
}

/* 业务模块配色 */
.corner-ornament.business { background: #10b981; }
.content-layer.business { border-color: #e6f9ec; }
.content-layer.business .icon-holder { background: #f0fff4; }
.target-ring {
  width: 48px;
  height: 48px;
  border: 4px solid #10b981;
  border-radius: 50%;
  opacity: 0.7;
}
.target-dot {
  position: absolute;
  width: 16px;
  height: 16px;
  background: #10b981;
  border-radius: 50%;
}
.content-layer.business .bottom-glow {
  background: linear-gradient(to top, rgba(16, 185, 129, 0.1), transparent);
}

/* 工作日常模块配色 */
.corner-ornament.daily { background: #f97316; }
.content-layer.daily { border-color: #fff0e0; }
.content-layer.daily .icon-holder { background: #fff8f0; }
.calendar-frame {
  width: 48px;
  height: 48px;
  position: relative;
}
.calendar-top {
  width: 48px;
  height: 10px;
  background: #f97316;
  border-radius: 4px 4px 0 0;
}
.calendar-date {
  width: 48px;
  height: 38px;
  border: 2px solid #f97316;
  border-radius: 0 0 4px 4px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.2rem;
  font-weight: 500;
  color: #f97316;
}
.content-layer.daily .bottom-glow {
  background: linear-gradient(to top, rgba(249, 115, 22, 0.1), transparent);
}

/* 悬停交互效果 */
.module-link:hover .content-layer {
  transform: translateY(-18px);
  box-shadow: 
    0 25px 50px rgba(0,0,0,0.08),
    0 10px 20px rgba(0,0,0,0.04);
  border-color: #e8e8e8;
}

.module-link:hover .icon-holder {
  transform: scale(1.12);
  box-shadow: 0 8px 25px rgba(59, 130, 246, 0.15);
}

.module-link:hover .content-layer h3 {
  color: #111;
  transform: translateY(-5px);
}

.module-link:hover .corner-ornament {
  transform: rotate(20deg) scale(1.8);
  opacity: 0.4;
}

.module-link:hover .bottom-glow {
  opacity: 1;
  height: 50%;
}

/* 响应式设计 */
@media (max-width: 900px) {
  .page-wrapper {
    flex-direction: column;
    gap: 70px;
    padding: 60px 20px;
  }
  
  .module-container {
    width: 100%;
    max-width: 420px;
  }
  
  .content-layer {
    padding: 70px 30px;
  }
  
  .content-layer h3 {
    font-size: 2rem;
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