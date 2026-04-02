<template>
  <div class="contact-page">
    <header class="header">
      <div class="container">
        <div class="logo">
          <h1>Vue3 App</h1>
        </div>
        <nav class="nav">
          <router-link to="/" class="nav-link">首页</router-link>
          <router-link to="/about" class="nav-link">关于</router-link>
          <router-link to="/services" class="nav-link">服务</router-link>
          <router-link to="/contact" class="nav-link active">联系</router-link>
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
          <h1 class="page-title">联系我们</h1>
          <p class="page-subtitle">我们期待与您合作，共同创造价值</p>
        </div>

        <div class="contact-content">
          <!-- 联系信息 -->
          <section class="contact-info">
            <div class="info-card">
              <div class="info-icon">📍</div>
              <h3 class="info-title">办公地址</h3>
              <p class="info-content">北京市朝阳区科技园区创新大厦A座18层</p>
              <p class="info-subtitle">交通便利，地铁10号线直达</p>
            </div>
            
            <div class="info-card">
              <div class="info-icon">📞</div>
              <h3 class="info-title">联系电话</h3>
              <p class="info-content">+86 123 4567 8900</p>
              <p class="info-subtitle">工作日 9:00-18:00</p>
            </div>
            
            <div class="info-card">
              <div class="info-icon">📧</div>
              <h3 class="info-title">电子邮箱</h3>
              <p class="info-content">contact@vue3app.com</p>
              <p class="info-subtitle">技术支持：support@vue3app.com</p>
            </div>
            
            <div class="info-card">
              <div class="info-icon">⏰</div>
              <h3 class="info-title">工作时间</h3>
              <p class="info-content">周一至周五 9:00-18:00</p>
              <p class="info-subtitle">周末及节假日休息</p>
            </div>
          </section>

          <!-- 联系表单 -->
          <section class="contact-form-section">
            <h2 class="section-title">发送消息</h2>
            <p class="section-subtitle">请填写以下表单，我们会尽快回复您</p>
            
            <form @submit.prevent="submitForm" class="contact-form">
              <div class="form-row">
                <div class="form-group">
                  <label for="name">姓名 *</label>
                  <input 
                    id="name" 
                    v-model="form.name" 
                    type="text" 
                    placeholder="请输入您的姓名" 
                    required
                  >
                </div>
                <div class="form-group">
                  <label for="email">邮箱 *</label>
                  <input 
                    id="email" 
                    v-model="form.email" 
                    type="email" 
                    placeholder="请输入您的邮箱" 
                    required
                  >
                </div>
              </div>
              
              <div class="form-group">
                <label for="phone">联系电话</label>
                <input 
                  id="phone" 
                  v-model="form.phone" 
                  type="tel" 
                  placeholder="请输入您的联系电话"
                >
              </div>
              
              <div class="form-group">
                <label for="subject">主题 *</label>
                <input 
                  id="subject" 
                  v-model="form.subject" 
                  type="text" 
                  placeholder="请输入消息主题" 
                  required
                >
              </div>
              
              <div class="form-group">
                <label for="message">消息内容 *</label>
                <textarea 
                  id="message" 
                  v-model="form.message" 
                  placeholder="请输入您的消息内容" 
                  rows="6"
                  required
                ></textarea>
              </div>
              
              <div class="form-actions">
                <button type="submit" class="btn btn-primary" :disabled="submitting">
                  {{ submitting ? '发送中...' : '发送消息' }}
                </button>
                <button type="button" class="btn btn-outline" @click="resetForm">
                  重置
                </button>
              </div>
            </form>
          </section>

          <!-- 地图位置 -->
          <section class="map-section">
            <h2 class="section-title">我们的位置</h2>
            <div class="map-placeholder">
              <div class="map-content">
                <span class="map-icon">🗺️</span>
                <p>北京市朝阳区科技园区</p>
                <p class="map-subtitle">点击查看详细地图</p>
              </div>
            </div>
            <div class="map-info">
              <p><strong>交通指引：</strong>地铁10号线科技园站C出口，步行5分钟即到</p>
              <p><strong>停车信息：</strong>园区提供地下停车场，前2小时免费</p>
            </div>
          </section>

          <!-- 常见问题 -->
          <section class="faq-section">
            <h2 class="section-title">常见问题</h2>
            <div class="faq-list">
              <div class="faq-item">
                <h3 class="faq-question">如何获取技术支持？</h3>
                <p class="faq-answer">您可以通过邮箱 support@vue3app.com 或拨打技术支持热线获取帮助。</p>
              </div>
              <div class="faq-item">
                <h3 class="faq-question">项目合作流程是怎样的？</h3>
                <p class="faq-answer">我们采用标准化的项目合作流程：需求沟通 → 方案制定 → 合同签订 → 项目实施 → 验收交付。</p>
              </div>
              <div class="faq-item">
                <h3 class="faq-question">响应时间需要多久？</h3>
                <p class="faq-answer">工作时间内，我们会在2小时内回复您的咨询；非工作时间，我们会在下一个工作日回复。</p>
              </div>
              <div class="faq-item">
                <h3 class="faq-question">是否提供上门服务？</h3>
                <p class="faq-answer">对于重要客户和复杂项目，我们可以提供上门沟通和技术支持服务。</p>
              </div>
            </div>
          </section>
        </div>
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
  name: 'Contact',
  data() {
    return {
      submitting: false,
      form: {
        name: '',
        email: '',
        phone: '',
        subject: '',
        message: ''
      }
    }
  },
  methods: {
    submitForm() {
      this.submitting = true
      
      // 模拟表单提交
      setTimeout(() => {
        console.log('表单提交:', this.form)
        alert('消息发送成功！我们会尽快回复您。')
        this.resetForm()
        this.submitting = false
      }, 1500)
    },
    resetForm() {
      this.form = {
        name: '',
        email: '',
        phone: '',
        subject: '',
        message: ''
      }
    }
  }
}
</script>

<style scoped>
.contact-page {
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

.btn-primary:hover:not(:disabled) {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(52, 152, 219, 0.3);
}

.btn-primary:disabled {
  opacity: 0.6;
  cursor: not-allowed;
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

/* 联系内容布局 */
.contact-content {
  display: flex;
  flex-direction: column;
  gap: 4rem;
}

/* 联系信息 */
.contact-info {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.info-card {
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: transform 0.3s;
}

.info-card:hover {
  transform: translateY(-5px);
}

.info-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.info-title {
  font-size: 1.25rem;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.info-content {
  color: #3498db;
  font-weight: 600;
  margin-bottom: 0.5rem;
}

.info-subtitle {
  color: #4a5568;
  font-size: 0.9rem;
}

/* 联系表单 */
.contact-form-section {
  background: white;
  padding: 3rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.section-title {
  font-size: 2rem;
  color: #2c3e50;
  margin-bottom: 1rem;
}

.section-subtitle {
  color: #4a5568;
  margin-bottom: 2rem;
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.form-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
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

.form-group input,
.form-group textarea {
  padding: 0.75rem;
  border: 1px solid #e2e8f0;
  border-radius: 8px;
  font-size: 1rem;
  transition: border-color 0.2s;
}

.form-group input:focus,
.form-group textarea:focus {
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

/* 地图位置 */
.map-section {
  background: white;
  padding: 3rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.map-placeholder {
  width: 100%;
  height: 300px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  margin-bottom: 1.5rem;
}

.map-content {
  text-align: center;
}

.map-icon {
  font-size: 4rem;
  display: block;
  margin-bottom: 1rem;
}

.map-subtitle {
  font-size: 0.9rem;
  opacity: 0.9;
}

.map-info {
  color: #4a5568;
  line-height: 1.6;
}

.map-info p {
  margin-bottom: 0.5rem;
}

/* 常见问题 */
.faq-section {
  background: white;
  padding: 3rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.faq-list {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.faq-item {
  border-bottom: 1px solid #e2e8f0;
  padding-bottom: 1.5rem;
}

.faq-item:last-child {
  border-bottom: none;
}

.faq-question {
  font-size: 1.25rem;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.faq-answer {
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
  
  .contact-info {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .form-row {
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
  .page-title {
    font-size: 2.5rem;
  }
  
  .section-title {
    font-size: 1.75rem;
  }
  
  .contact-info {
    grid-template-columns: 1fr;
  }
  
  .contact-form-section,
  .map-section,
  .faq-section {
    padding: 2rem;
  }
}
</style>
