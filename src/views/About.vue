<template>
  <div class="about-page">
    <header class="header">
      <div class="container">
        <div class="logo">
          <h1>Vue3 App</h1>
        </div>
        <nav class="nav">
          <router-link to="/" class="nav-link">首页</router-link>
          <router-link to="/about" class="nav-link active">关于</router-link>
          <router-link to="/services" class="nav-link">服务</router-link>
          <router-link to="/contact" class="nav-link">联系</router-link>
        </nav>
        <div class="user-actions">
          <button class="btn btn-primary" @click="$router.push('/login')">登录</button>
          <button class="btn btn-outline" @click="showSignupModal = true">注册</button>
        </div>
      </div>
    </header>

    <main class="main-content">
      <div class="container">
        <!-- 页面标题 -->
        <div class="page-header">
          <h1 class="page-title">关于我们</h1>
          <p class="page-subtitle">了解我们的使命、愿景和团队</p>
        </div>

        <!-- 公司介绍 -->
        <section class="company-intro">
          <div class="intro-content">
            <h2 class="section-title">我们的故事</h2>
            <p class="intro-text">
              我们是一家专注于前端技术创新的科技公司，成立于2020年。我们的团队由一群充满激情的开发者组成，致力于通过先进的技术为用户提供卓越的Web应用体验。
            </p>
            <p class="intro-text">
              从最初的小型项目到现在的企业级应用，我们始终坚持技术创新和用户体验至上的原则。我们相信，优秀的技术应该服务于人，让复杂的事情变得简单。
            </p>
          </div>
          <div class="intro-image">
            <div class="image-placeholder">
              <span class="icon">🏢</span>
              <p>公司总部</p>
            </div>
          </div>
        </section>

        <!-- 使命与愿景 -->
        <section class="mission-vision">
          <div class="mission-card">
            <div class="card-icon">🎯</div>
            <h3 class="card-title">我们的使命</h3>
            <p class="card-description">
              通过技术创新，为企业提供高效、可靠的前端解决方案，帮助客户在数字化时代取得成功。
            </p>
          </div>
          <div class="vision-card">
            <div class="card-icon">🔭</div>
            <h3 class="card-title">我们的愿景</h3>
            <p class="card-description">
              成为全球领先的前端技术提供商，推动Web技术的发展，创造更美好的数字世界。
            </p>
          </div>
        </section>

        <!-- 核心价值观 -->
        <section class="core-values">
          <h2 class="section-title">核心价值观</h2>
          <div class="values-grid">
            <div class="value-card">
              <div class="value-icon">💡</div>
              <h3 class="value-title">创新</h3>
              <p class="value-description">持续探索新技术，追求卓越的技术解决方案</p>
            </div>
            <div class="value-card">
              <div class="value-icon">🤝</div>
              <h3 class="value-title">协作</h3>
              <p class="value-description">团队合作，共同成长，实现共赢</p>
            </div>
            <div class="value-card">
              <div class="value-icon">🎯</div>
              <h3 class="value-title">专注</h3>
              <p class="value-description">专注于前端领域，深耕细作，追求极致</p>
            </div>
            <div class="value-card">
              <div class="value-icon">❤️</div>
              <h3 class="value-title">责任</h3>
              <p class="value-description">对客户负责，对产品负责，对社会负责</p>
            </div>
          </div>
        </section>

        <!-- 团队介绍 -->
        <section class="team-section">
          <h2 class="section-title">我们的团队</h2>
          <p class="section-subtitle">一群充满激情的技术专家</p>
          <div class="team-grid">
            <div class="team-member">
              <div class="member-avatar">
                <span class="avatar-icon">👨‍💻</span>
              </div>
              <h3 class="member-name">张明</h3>
              <p class="member-role">首席技术官</p>
              <p class="member-bio">10年前端开发经验，Vue.js专家</p>
            </div>
            <div class="team-member">
              <div class="member-avatar">
                <span class="avatar-icon">👩‍💻</span>
              </div>
              <h3 class="member-name">李娜</h3>
              <p class="member-role">产品总监</p>
              <p class="member-bio">用户体验专家，8年产品设计经验</p>
            </div>
            <div class="team-member">
              <div class="member-avatar">
                <span class="avatar-icon">👨‍💼</span>
              </div>
              <h3 class="member-name">王强</h3>
              <p class="member-role">项目经理</p>
              <p class="member-bio">敏捷开发专家，12年项目管理经验</p>
            </div>
            <div class="team-member">
              <div class="member-avatar">
                <span class="avatar-icon">👩‍🎨</span>
              </div>
              <h3 class="member-name">陈静</h3>
              <p class="member-role">UI设计师</p>
              <p class="member-bio">视觉设计专家，6年UI/UX设计经验</p>
            </div>
          </div>
        </section>

        <!-- 发展历程 -->
        <section class="timeline-section">
          <h2 class="section-title">发展历程</h2>
          <div class="timeline">
            <div class="timeline-item">
              <div class="timeline-date">2020年</div>
              <div class="timeline-content">
                <h3 class="timeline-title">公司成立</h3>
                <p class="timeline-description">在北京成立，专注于Vue.js技术开发</p>
              </div>
            </div>
            <div class="timeline-item">
              <div class="timeline-date">2021年</div>
              <div class="timeline-content">
                <h3 class="timeline-title">产品发布</h3>
                <p class="timeline-description">发布首个企业级Vue.js应用框架</p>
              </div>
            </div>
            <div class="timeline-item">
              <div class="timeline-date">2022年</div>
              <div class="timeline-content">
                <h3 class="timeline-title">团队扩张</h3>
                <p class="timeline-description">团队规模扩大至20人，服务客户超过50家</p>
              </div>
            </div>
            <div class="timeline-item">
              <div class="timeline-date">2023年</div>
              <div class="timeline-content">
                <h3 class="timeline-title">技术升级</h3>
                <p class="timeline-description">全面升级至Vue 3技术栈，推出新一代产品</p>
              </div>
            </div>
          </div>
        </section>
      </div>
    </main>

    <!-- 页脚 -->
    <footer class="footer">
      <div class="container">
        <div class="footer-content">
          <div class="footer-section">
            <h4 class="footer-title">Vue3 App</h4>
            <p class="footer-description">一个现代化的前端应用框架，帮助您快速构建优秀的Web应用。</p>
          </div>
          <div class="footer-section">
            <h4 class="footer-title">快速链接</h4>
            <ul class="footer-links">
              <li><router-link to="/">首页</router-link></li>
              <li><router-link to="/about">关于我们</router-link></li>
              <li><router-link to="/contact">联系我们</router-link></li>
            </ul>
          </div>
          <div class="footer-section">
            <h4 class="footer-title">技术支持</h4>
            <ul class="footer-links">
              <li><a href="#">文档中心</a></li>
              <li><a href="#">API参考</a></li>
              <li><a href="#">常见问题</a></li>
              <li><a href="#">社区论坛</a></li>
            </ul>
          </div>
          <div class="footer-section">
            <h4 class="footer-title">联系我们</h4>
            <p class="contact-info">
              <span>📧 contact@vue3app.com</span><br>
              <span>📞 +86 123 4567 8900</span><br>
              <span>📍 北京市朝阳区科技园区</span>
            </p>
          </div>
        </div>
        <div class="footer-bottom">
          <p class="copyright">© 2024 Vue3 App. 保留所有权利。</p>
          <div class="social-links">
            <a href="#" class="social-link">GitHub</a>
            <a href="#" class="social-link">Twitter</a>
            <a href="#" class="social-link">LinkedIn</a>
            <a href="#" class="social-link">WeChat</a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'About',
  data() {
    return {}
  }
}
</script>

<style scoped>
.about-page {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* 导航栏样式 */
.header {
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 1000;
}

.header .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 20px;
}

.logo h1 {
  margin: 0;
  font-size: 1.5rem;
  color: #2c3e50;
  font-weight: 700;
}

.nav {
  display: flex;
  gap: 2rem;
}

.nav-link {
  color: #4a5568;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.2s;
}

.nav-link:hover,
.nav-link.active {
  color: #3498db;
}

.user-actions {
  display: flex;
  gap: 1rem;
}

/* 按钮样式 */
.btn {
  padding: 0.5rem 1.5rem;
  border-radius: 8px;
  border: none;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.2s;
}

.btn-primary {
  background: linear-gradient(90deg, #3498db 0%, #2980b9 100%);
  color: white;
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(52, 152, 219, 0.3);
}

/* 主内容区域 */
.main-content {
  flex: 1;
  padding: 3rem 0;
}

.page-header {
  text-align: center;
  margin-bottom: 4rem;
}

.page-title {
  font-size: 3rem;
  color: #2c3e50;
  margin-bottom: 1rem;
}

.page-subtitle {
  font-size: 1.25rem;
  color: #4a5568;
}

/* 公司介绍 */
.company-intro {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
  margin-bottom: 4rem;
}

.section-title {
  font-size: 2rem;
  color: #2c3e50;
  margin-bottom: 1.5rem;
}

.intro-text {
  color: #4a5568;
  line-height: 1.8;
  margin-bottom: 1rem;
}

.intro-image {
  display: flex;
  justify-content: center;
}

.image-placeholder {
  width: 100%;
  max-width: 400px;
  height: 250px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: white;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
}

.image-placeholder .icon {
  font-size: 4rem;
  margin-bottom: 1rem;
}

/* 使命与愿景 */
.mission-vision {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  margin-bottom: 4rem;
}

.mission-card,
.vision-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.card-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.card-title {
  font-size: 1.5rem;
  color: #2c3e50;
  margin-bottom: 1rem;
}

.card-description {
  color: #4a5568;
  line-height: 1.6;
}

/* 核心价值观 */
.core-values {
  margin-bottom: 4rem;
}

.values-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.value-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: transform 0.3s;
}

.value-card:hover {
  transform: translateY(-5px);
}

.value-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.value-title {
  font-size: 1.25rem;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.value-description {
  color: #4a5568;
  line-height: 1.6;
}

/* 团队介绍 */
.team-section {
  margin-bottom: 4rem;
}

.section-subtitle {
  text-align: center;
  color: #4a5568;
  margin-bottom: 3rem;
}

.team-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.team-member {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.member-avatar {
  width: 100px;
  height: 100px;
  background: linear-gradient(135deg, #3498db 0%, #2980b9 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1rem;
}

.avatar-icon {
  font-size: 3rem;
}

.member-name {
  font-size: 1.25rem;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.member-role {
  color: #3498db;
  font-weight: 600;
  margin-bottom: 0.5rem;
}

.member-bio {
  color: #4a5568;
  font-size: 0.9rem;
}

/* 发展历程 */
.timeline-section {
  margin-bottom: 4rem;
}

.timeline {
  position: relative;
  max-width: 800px;
  margin: 0 auto;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 50%;
  top: 0;
  bottom: 0;
  width: 2px;
  background: #3498db;
  transform: translateX(-50%);
}

.timeline-item {
  position: relative;
  margin-bottom: 3rem;
  display: flex;
  align-items: center;
}

.timeline-item:nth-child(odd) {
  flex-direction: row-reverse;
}

.timeline-date {
  flex: 0 0 120px;
  text-align: center;
  font-weight: 600;
  color: #3498db;
  background: white;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  border: 2px solid #3498db;
  position: relative;
  z-index: 1;
}

.timeline-content {
  flex: 1;
  background: white;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  margin: 0 2rem;
}

.timeline-title {
  font-size: 1.25rem;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.timeline-description {
  color: #4a5568;
  line-height: 1.6;
}

/* 页脚样式 */
.footer {
  background: #2c3e50;
  color: white;
  padding: 3rem 0 1.5rem;
  margin-top: auto;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 2rem;
  margin-bottom: 2rem;
}

.footer-title {
  font-size: 1.25rem;
  margin-bottom: 1rem;
  color: #3498db;
}

.footer-description {
  color: #a0aec0;
  line-height: 1.6;
}

.footer-links {
  list-style: none;
  padding: 0;
}

.footer-links li {
  margin-bottom: 0.5rem;
}

.footer-links a {
  color: #a0aec0;
  text-decoration: none;
  transition: color 0.2s;
}

.footer-links a:hover {
  color: #3498db;
}

.contact-info {
  color: #a0aec0;
  line-height: 1.8;
}

.footer-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 2rem;
  border-top: 1px solid #4a5568;
}

.copyright {
  color: #a0aec0;
  font-size: 0.9rem;
}

.social-links {
  display: flex;
  gap: 1rem;
}

.social-link {
  color: #a0aec0;
  text-decoration: none;
  transition: color 0.2s;
}

.social-link:hover {
  color: #3498db;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .header .container {
    flex-direction: column;
    gap: 1rem;
  }
  
  .nav {
    flex-wrap: wrap;
    justify-content: center;
    gap: 1rem;
  }
  
  .company-intro {
    grid-template-columns: 1fr;
    text-align: center;
  }
  
  .mission-vision {
    grid-template-columns: 1fr;
  }
  
  .timeline::before {
    left: 30px;
  }
  
  .timeline-item {
    flex-direction: row !important;
    align-items: flex-start;
  }
  
  .timeline-date {
    flex: 0 0 80px;
    margin-right: 1rem;
  }
  
  .timeline-content {
    margin: 0;
  }
  
  .footer-content {
    grid-template-columns: 1fr;
  }
  
  .footer-bottom {
    flex-direction: column;
    gap: 1rem;
    text-align: center;
  }
}

@media (max-width: 480px) {
  .page-title {
    font-size: 2.5rem;
  }
  
  .section-title {
    font-size: 1.75rem;
  }
  
  .values-grid,
  .team-grid {
    grid-template-columns: 1fr;
  }
}

a {
  color: #3498db;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}
</style>