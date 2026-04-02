<template>
  <div class="home-page">
    <!-- 导航栏 -->
    <header class="header">
      <div class="container">
        <div class="logo">
          <h1>Vue3 App</h1>
        </div>
        <nav class="nav">
          <router-link to="/" class="nav-link active">首页</router-link>
          <router-link to="/about" class="nav-link">关于</router-link>
          <router-link to="/services" class="nav-link">服务</router-link>
          <router-link to="/contact" class="nav-link">联系</router-link>
        </nav>
        <div class="user-actions">
          <button class="btn btn-primary" @click="$router.push('/login')">登录</button>
          <button class="btn btn-outline" @click="showSignupModal = true">注册</button>
        </div>
      </div>
    </header>

    <!-- 英雄区域 -->
    <section class="hero">
      <div class="container">
        <div class="hero-content">
          <h2 class="hero-title">欢迎使用 Vue3 应用</h2>
          <p class="hero-subtitle">一个现代化的前端应用，使用 Vue 3、Vite 和最新技术栈构建</p>
          <div class="hero-actions">
            <button class="btn btn-large btn-primary" @click="startTutorial">开始教程</button>
            <button class="btn btn-large btn-outline" @click="viewDemo">查看演示</button>
          </div>
        </div>
        <div class="hero-image">
          <div class="image-placeholder">
            <div class="placeholder-content">
              <span class="icon">🚀</span>
              <p>应用界面预览</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 特性展示 -->
    <section class="features">
      <div class="container">
        <h2 class="section-title">核心特性</h2>
        <p class="section-subtitle">探索我们应用的主要功能和优势</p>
        <div class="features-grid">
          <div class="feature-card">
            <div class="feature-icon">⚡</div>
            <h3 class="feature-title">快速响应</h3>
            <p class="feature-description">基于 Vue 3 的响应式系统，提供流畅的用户体验和即时反馈。</p>
          </div>
          <div class="feature-card">
            <div class="feature-icon">🎨</div>
            <h3 class="feature-title">现代化设计</h3>
            <p class="feature-description">采用最新的设计语言和交互模式，界面美观且易于使用。</p>
          </div>
          <div class="feature-card">
            <div class="feature-icon">🔧</div>
            <h3 class="feature-title">易于定制</h3>
            <p class="feature-description">模块化架构设计，方便根据需求进行功能扩展和定制。</p>
          </div>
          <div class="feature-card">
            <div class="feature-icon">📱</div>
            <h3 class="feature-title">响应式布局</h3>
            <p class="feature-description">完美适配各种设备尺寸，从桌面到移动端都能获得最佳体验。</p>
          </div>
        </div>
      </div>
    </section>

    <!-- 内容区域 -->
    <section class="content">
      <div class="container">
        <div class="content-grid">
          <div class="content-card">
            <h3 class="content-title">最新动态</h3>
            <ul class="news-list">
              <li class="news-item">
                <span class="news-date">2024-03-15</span>
                <span class="news-text">发布 v1.2.0 版本，新增用户管理功能</span>
              </li>
              <li class="news-item">
                <span class="news-date">2024-03-10</span>
                <span class="news-text">优化了移动端界面体验</span>
              </li>
              <li class="news-item">
                <span class="news-date">2024-03-05</span>
                <span class="news-text">新增数据可视化图表组件</span>
              </li>
              <li class="news-item">
                <span class="news-date">2024-03-01</span>
                <span class="news-text">修复了已知的性能问题</span>
              </li>
            </ul>
          </div>
          <div class="content-card">
            <h3 class="content-title">统计数据</h3>
            <div class="stats">
              <div class="stat-item">
                <div class="stat-value">1,234</div>
                <div class="stat-label">活跃用户</div>
              </div>
              <div class="stat-item">
                <div class="stat-value">89%</div>
                <div class="stat-label">用户满意度</div>
              </div>
              <div class="stat-item">
                <div class="stat-value">24/7</div>
                <div class="stat-label">服务可用性</div>
              </div>
              <div class="stat-item">
                <div class="stat-value">99.9%</div>
                <div class="stat-label">系统稳定性</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

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

    <!-- 注册模态框 -->
    <div v-if="showSignupModal" class="modal-overlay" @click="showSignupModal = false">
      <div class="modal-content" @click.stop>
        <h3 class="modal-title">创建账户</h3>
        <form @submit.prevent="handleSignup" class="modal-form">
          <div class="form-group">
            <label for="email">邮箱地址</label>
            <input id="email" v-model="signupForm.email" type="email" placeholder="请输入邮箱" required>
          </div>
          <div class="form-group">
            <label for="password">密码</label>
            <input id="password" v-model="signupForm.password" type="password" placeholder="请输入密码" required>
          </div>
          <div class="form-group">
            <label for="confirmPassword">确认密码</label>
            <input id="confirmPassword" v-model="signupForm.confirmPassword" type="password" placeholder="请再次输入密码" required>
          </div>
          <div class="form-actions">
            <button type="button" class="btn btn-outline" @click="showSignupModal = false">取消</button>
            <button type="submit" class="btn btn-primary">注册</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      showSignupModal: false,
      signupForm: {
        email: '',
        password: '',
        confirmPassword: ''
      }
    }
  },
  methods: {
    startTutorial() {
      alert('开始教程功能开发中...')
    },
    viewDemo() {
      alert('演示功能开发中...')
    },
    handleSignup() {
      if (this.signupForm.password !== this.signupForm.confirmPassword) {
        alert('两次输入的密码不一致')
        return
      }
      // 这里应该调用注册API
      console.log('注册信息:', this.signupForm)
      alert('注册成功！')
      this.showSignupModal = false
      this.signupForm = {
        email: '',
        password: '',
        confirmPassword: ''
      }
    }
  }
}
</script>

<style scoped>
/* 基础样式 */
.home-page {
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

.btn-outline {
  background: transparent;
  border: 2px solid #3498db;
  color: #3498db;
}

.btn-outline:hover {
  background: #3498db;
  color: white;
}

.btn-large {
  padding: 0.75rem 2rem;
  font-size: 1.1rem;
}

/* 英雄区域样式 */
.hero {
  padding: 4rem 0;
  background: white;
}

.hero .container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.hero-title {
  font-size: 3rem;
  color: #2c3e50;
  margin-bottom: 1rem;
  line-height: 1.2;
}

.hero-subtitle {
  font-size: 1.25rem;
  color: #4a5568;
  margin-bottom: 2rem;
  line-height: 1.6;
}

.hero-actions {
  display: flex;
  gap: 1rem;
}

.hero-image {
  display: flex;
  justify-content: center;
}

.image-placeholder {
  width: 100%;
  max-width: 400px;
  height: 300px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
}

.placeholder-content {
  text-align: center;
}

.placeholder-content .icon {
  font-size: 4rem;
  display: block;
  margin-bottom: 1rem;
}

/* 特性区域样式 */
.features {
  padding: 4rem 0;
  background: #f8fafc;
}

.section-title {
  text-align: center;
  font-size: 2.5rem;
  color: #2c3e50;
  margin-bottom: 1rem;
}

.section-subtitle {
  text-align: center;
  color: #4a5568;
  margin-bottom: 3rem;
  font-size: 1.1rem;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.feature-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.feature-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
}

.feature-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.feature-title {
  font-size: 1.5rem;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.feature-description {
  color: #4a5568;
  line-height: 1.6;
}

/* 内容区域样式 */
.content {
  padding: 4rem 0;
  background: white;
}

.content-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.content-card {
  background: #f8fafc;
  padding: 2rem;
  border-radius: 12px;
  border: 1px solid #e2e8f0;
}

.content-title {
  font-size: 1.5rem;
  color: #2c3e50;
  margin-bottom: 1.5rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid #3498db;
}

.news-list {
  list-style: none;
  padding: 0;
}

.news-item {
  display: flex;
  justify-content: space-between;
  padding: 0.75rem 0;
  border-bottom: 1px solid #e2e8f0;
}

.news-item:last-child {
  border-bottom: none;
}

.news-date {
  color: #718096;
  font-size: 0.9rem;
}

.news-text {
  color: #2c3e50;
}

.stats {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
}

.stat-item {
  text-align: center;
}

.stat-value {
  font-size: 2rem;
  font-weight: 700;
  color: #3498db;
  margin-bottom: 0.25rem;
}

.stat-label {
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

/* 模态框样式 */
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 2000;
}

.modal-content {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  width: 90%;
  max-width: 400px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
}

.modal-title {
  font-size: 1.5rem;
  color: #2c3e50;
  margin-bottom: 1.5rem;
  text-align: center;
}

.modal-form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.form-group label {
  color: #4a5568;
  font-weight: 500;
}

.form-group input {
  padding: 0.75rem;
  border: 1px solid #e2e8f0;
  border-radius: 8px;
  font-size: 1rem;
  transition: border-color 0.2s;
}

.form-group input:focus {
  outline: none;
  border-color: #3498db;
  box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.1);
}

.form-actions {
  display: flex;
  justify-content: flex-end;
  gap: 1rem;
  margin-top: 1rem;
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
  
  .hero .container {
    grid-template-columns: 1fr;
    text-align: center;
  }
  
  .hero-title {
    font-size: 2.5rem;
  }
  
  .hero-actions {
    justify-content: center;
  }
  
  .features-grid {
    grid-template-columns: 1fr;
  }
  
  .content-grid {
    grid-template-columns: 1fr;
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
  .hero-title {
    font-size: 2rem;
  }
  
  .section-title {
    font-size: 2rem;
  }
  
  .btn-large {
    padding: 0.5rem 1.5rem;
    font-size: 1rem;
  }
}
</style>
