<!-- 页面容器 -->
<div class="page-center">
  <!-- 技术模块 -->
  <div class="module-container">
    <a href="./technology/" class="module tech">
      <div class="module-content">
        <div class="icon-box">
          <div class="icon-tech"></div>
        </div>
        <h3>技术</h3>
        <div class="underline"></div>
      </div>
    </a>
  </div>

  <!-- 业务模块 -->
  <div class="module-container">
    <a href="./business/" class="module business">
      <div class="module-content">
        <div class="icon-box">
          <div class="icon-business"></div>
        </div>
        <h3>业务</h3>
        <div class="underline"></div>
      </div>
    </a>
  </div>

  <!-- 工作日常模块 -->
  <div class="module-container">
    <a href="./daily/" class="module daily">
      <div class="module-content">
        <div class="icon-box">
          <div class="icon-daily"></div>
        </div>
        <h3>工作日常</h3>
        <div class="underline"></div>
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

/* 页面居中容器 */
.page-center {
  min-height: 100vh;
  display: flex;
  justify-content: center; /* 水平居中 */
  align-items: center; /* 垂直居中 */
  padding: 20px;
  background: #ffffff;
}

/* 模块容器（三大模块整体居中） */
.page-center {
  gap: 60px; /* 模块之间的间距 */
}

/* 单个模块容器 */
.module-container {
  width: 220px; /* 固定宽度，确保对齐 */
}

/* 模块链接样式 */
.module {
  display: block;
  text-decoration: none;
}

/* 模块内容区 */
.module-content {
  padding: 45px 20px;
  text-align: center;
  border-radius: 14px;
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  border: 1px solid #f0f0f0;
}

/* 图标容器 */
.icon-box {
  width: 70px;
  height: 70px;
  margin: 0 auto 30px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
}

/* 图标样式 */
.icon-tech {
  width: 28px;
  height: 28px;
  background: #4263eb;
  clip-path: polygon(0 0, 100% 0, 100% 75%, 75% 75%, 75% 100%, 50% 75%, 0 75%);
}

.icon-business {
  width: 28px;
  height: 28px;
  background: #0ca678;
  clip-path: polygon(10% 25%, 35% 25%, 35% 0%, 65% 0%, 65% 25%, 90% 25%, 90% 50%, 65% 50%, 65% 100%, 35% 100%, 35% 50%, 10% 50%);
}

.icon-daily {
  width: 28px;
  height: 28px;
  background: #f76707;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}

/* 标题样式 */
.module h3 {
  font-family: 'Inter', sans-serif;
  font-size: 1.4rem;
  font-weight: 500;
  margin-bottom: 20px;
  transition: color 0.3s ease;
}

/* 下划线装饰 */
.underline {
  width: 30px;
  height: 2px;
  margin: 0 auto;
  transition: width 0.3s ease;
}

/* 技术模块配色 */
.tech .icon-box {
  background: #eef2ff;
}
.tech h3 {
  color: #1e3a8a;
}
.tech .underline {
  background: #4263eb;
}

/* 业务模块配色 */
.business .icon-box {
  background: #e6fcf5;
}
.business h3 {
  color: #087f5b;
}
.business .underline {
  background: #0ca678;
}

/* 工作日常模块配色 */
.daily .icon-box {
  background: #fff4e6;
}
.daily h3 {
  color: #c2410c;
}
.daily .underline {
  background: #f76707;
}

/* 悬停效果 */
.module:hover .module-content {
  transform: translateY(-6px);
  box-shadow: 0 12px 24px -8px rgba(0, 0, 0, 0.04);
  border-color: #eaeaea;
}

.module:hover .icon-box {
  transform: scale(1.05);
}

.module:hover .underline {
  width: 50px;
}

/* 响应式调整（确保小屏仍居中） */
@media (max-width: 768px) {
  .page-center {
    flex-direction: column; /* 小屏垂直排列 */
    gap: 40px;
    padding: 60px 20px;
  }

  .module-container {
    width: 100%;
    max-width: 280px; /* 小屏固定最大宽度 */
  }

  .module-content {
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