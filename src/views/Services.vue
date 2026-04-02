<template>
  <div class="services-page">
    <header class="header">
      <div class="container">
        <div class="logo">
          <h1>Vue3 App</h1>
        </div>
        <nav class="nav">
          <router-link to="/" class="nav-link">首页</router-link>
          <router-link to="/about" class="nav-link">关于</router-link>
          <router-link to="/services" class="nav-link active">服务</router-link>
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
          <h1 class="page-title">我们的服务</h1>
          <p class="page-subtitle">专业的前端开发解决方案，满足您的业务需求</p>
        </div>

        <!-- 服务介绍 -->
        <section class="services-intro">
          <div class="intro-content">
            <h2 class="section-title">专业前端开发服务</h2>
            <p class="intro-text">
              我们提供全面的前端开发服务，从概念设计到产品上线，全程为您提供专业的技术支持。我们的团队拥有丰富的Vue.js开发经验，能够为您打造高性能、可扩展的Web应用。
            </p>
          </div>
        </section>

        <!-- 服务列表 -->
        <section class="services-list">
          <div class="service-card">
            <div class="service-icon">🎨</div>
            <h3 class="service-title">UI/UX设计</h3>
            <p class="service-description">
              专业的用户界面和用户体验设计，打造美观易用的产品界面。我们注重细节，追求完美的用户体验。
            </p>
            <ul class="service-features">
              <li>响应式设计</li>
              <li>交互设计</li>
              <li>视觉设计</li>
              <li>原型设计</li>
            </ul>
          </div>
          
          <div class="service-card">
            <div class="service-icon">⚡</div>
            <h3 class="service-title">Vue.js开发</h3>
            <p class="service-description">
              基于Vue.js框架的企业级应用开发，提供高性能、可维护的前端解决方案。
            </p>
            <ul class="service-features">
              <li>Vue 3 + Composition API</li>
              <li>Vue Router + Vuex/Pinia</li>
              <li>TypeScript支持</li>
              <li>组件化开发</li>
            </ul>
          </div>
          
          <div class="service-card">
            <div class="service-icon">📱</div>
            <h3 class="service-title">移动端开发</h3>
            <p class="service-description">
              跨平台移动应用开发，支持iOS和Android平台，提供原生般的用户体验。
            </p>
            <ul class="service-features">
              <li>PWA应用</li>
              <li>响应式布局</li>
              <li>移动端优化</li>
              <li>离线功能</li>
            </ul>
          </div>
          
          <div class="service-card">
            <div class="service-icon">🔧</div>
            <h3 class="service-title">技术咨询</h3>
            <p class="service-description">
              提供前端技术架构咨询，帮助您选择最适合的技术栈和解决方案。
            </p>
            <ul class="service-features">
              <li>技术选型</li>
              <li>架构设计</li>
              <li>性能优化</li>
              <li>代码审查</li>
            </ul>
          </div>
          
          <div class="service-card">
            <div class="service-icon">🚀</div>
            <h3 class="service-title">性能优化</h3>
            <p class="service-description">
              应用性能分析和优化，提升页面加载速度和用户体验。
            </p>
            <ul class="service-features">
              <li>加载性能优化</li>
              <li>渲染性能优化</li>
              <li>打包优化</li>
              <li>缓存策略</li>
            </ul>
          </div>
          
          <div class="service-card">
            <div class="service-icon">🛠️</div>
            <h3 class="service-title">维护支持</h3>
            <p class="service-description">
              提供长期的技术支持和维护服务，确保系统稳定运行。
            </p>
            <ul class="service-features">
              <li>Bug修复</li>
              <li>功能更新</li>
              <li>安全更新</li>
              <li>技术支持</li>
            </ul>
          </div>
        </section>

        <!-- 技术栈 -->
        <section class="tech-stack">
          <h2 class="section-title">技术栈</h2>
          <p class="section-subtitle">我们使用最前沿的技术栈</p>
          <div class="tech-grid">
            <div class="tech-item">
              <div class="tech-icon">V</div>
              <h3 class="tech-name">Vue.js</h3>
              <p class="tech-description">渐进式JavaScript框架</p>
            </div>
            <div class="tech-item">
              <div class="tech-icon">T</div>
              <h3 class="tech-name">TypeScript</h3>
              <p class="tech-description">类型安全的JavaScript超集</p>
            </div>
            <div class="tech-item">
              <div class="tech-icon">V</div>
              <h3 class="tech-name">Vite</h3>
              <p class="tech-description">下一代前端构建工具</p>
            </div>
            <div class="tech-item">
              <div class="tech-icon">P</div>
              <h3 class="tech-name">Pinia</h3>
              <p class="tech-description">Vue状态管理库</p>
            </div>
            <div class="tech-item">
              <div class="tech-icon">T</div>
              <h3 class="tech-name">Tailwind CSS</h3>
              <p class="tech-description">实用优先的CSS框架</p>
            </div>
            <div class="tech-item">
              <div class="tech-icon">J</div>
              <h3 class="tech-name">Jest</h3>
              <p class="tech-description">JavaScript测试框架</p>
            </div>
          </div>
        </section>

        <!-- 工作流程 -->
        <section class="workflow">
          <h2 class="section-title">工作流程</h2>
          <div class="workflow-steps">
            <div class="step">
              <div class="step-number">1</div>
              <h3 class="step-title">需求分析</h3>
              <p class="step-description">深入了解业务需求，制定技术方案</p>
            </div>
            <div class="step">
              <div class="step-number">2</div>
              <h3 class="step-title">原型设计</h3>
              <p class="step-description">设计产品原型，确认交互流程</p>
            </div>
            <div class="step">
              <div class="step-number">3</div>
              <h3 class="step-title">开发实现</h3>
              <p class="step-description">敏捷开发，持续交付</p>
            </div>
            <div class="step">
              <div class="step-number">4</div>
              <h3 class="step-title">测试验收</h3>
              <p class="step-description">全面测试，确保质量</p>
            </div>
            <div class="step">
              <div class="step-number">5</div>
              <h3 class="step-title">部署上线</h3>
              <p class="step-description">部署到生产环境</p>
            </div>
            <div class="step">
              <div class="step-number">6</div>
              <h3 class="step-title">维护支持</h3>
              <p class="step-description">持续维护和技术支持</p>
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
  name: 'Services',
  data() {
    return {}
  }
}
</script>

<style scoped>
.services-page {
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

/* 服务介绍 */
.services-intro {
  margin-bottom: 4rem;
  text-align: center;
}

.section-title {
  font-size: 2rem;
  color: #2c3e50;
  margin-bottom: 1.5rem;
}

.intro-text {
  color: #4a5568;
  line-height: 1.8;
  max-width: 800px;
  margin: 0 auto;
}

/* 服务列表 */
.services-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
  margin-bottom: 4rem;
}

.service-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.service-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
}

.service-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.service-title {
  font-size: 1.5rem;
  color: #2c3e50;
  margin-bottom: 1rem;
}

.service-description {
  color: #4a5568;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.service-features {
  list-style: none;
  padding: 0;
  margin: 0;
}

.service-features li {
  color: #3498db;
  padding: 0.25rem 0;
  border-bottom: 1px solid #e2e8f0;
}

.service-features li:last-child {
  border-bottom: none;
}

/* 技术栈 */
.tech-stack {
  margin-bottom: 4rem;
}

.section-subtitle {
  text-align: center;
  color: #4a5568;
  margin-bottom: 3rem;
}

.tech-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 1.5rem;
}

.tech-item {
  background: white;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.tech-icon {
  width: 60px;
  height: 60px;
  background: linear-gradient(135deg, #3498db 0%, #2980b9 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1rem;
  color: white;
  font-size: 1.5rem;
  font-weight: bold;
}

.tech-name {
  font-size: 1.25rem;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.tech-description {
  color: #4a5568;
  font-size: 0.9rem;
}

/* 工作流程 */
.workflow {
  margin-bottom: 4rem;
}

.workflow-steps {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 2rem;
}

.step {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
  position: relative;
}

.step::before {
  content: '';
  position: absolute;
  top: 50%;
  right: -1rem;
  width: 2rem;
  height: 2px;
  background: #3498db;
  transform: translateY(-50%);
}

.step:last-child::before {
  display: none;
}

.step-number {
  width: 40px;
  height: 40px;
  background: linear-gradient(135deg, #3498db 0%, #2980b9 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1rem;
  color: white;
  font-weight: bold;
}

.step-title {
  font-size: 1.25rem;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.step-description {
  color: #4a5568;
  font-size: 0.9rem;
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
  
  .services-list {
    grid-template-columns: 1fr;
  }
  
  .tech-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .workflow-steps {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .step::before {
    display: none;
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
  
  .tech-grid {
    grid-template-columns: 1fr;
  }
  
  .workflow-steps {
    grid-template-columns: 1fr;
  }
}
</style>
