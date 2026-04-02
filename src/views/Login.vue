<template>
  <div class="login-page">
    <div class="login-card">
      <div class="login-title">
        <h2>欢迎回来</h2>
        <p>请使用账号密码登录</p>
      </div>
      <form @submit.prevent="login" class="login-form">
        <div class="field">
          <label for="username">用户名</label>
          <input id="username" v-model="username" placeholder="请输入用户名" required autocomplete="username" />
        </div>
        <div class="field">
          <label for="password">密码</label>
          <input id="password" v-model="password" type="password" placeholder="请输入密码" required autocomplete="current-password" />
        </div>
        <button type="submit" class="login-btn">登录</button>
      </form>
      <div class="login-foot">
        <a href="#" @click.prevent>忘记密码？</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data() {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    login() {
      console.log('登录信息:', { username: this.username, password: this.password })
      alert('登录成功！')
    }
  }
}
</script>

<style scoped>
.login-page {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #5ebd7f 0%, #4b8af8 100%);
  padding: 2rem;
}

.login-card {
  width: min(420px, 100%);
  background: #ffffff;
  border-radius: 16px;
  box-shadow: 0 14px 30px rgba(16, 35, 66, 0.18);
  padding: 2rem;
  border: 1px solid rgba(255, 255, 255, 0.45);
}

.login-title h2 {
  margin: 0;
  color: #243b64;
  font-size: 1.8rem;
}

.login-title p {
  margin: 0.4rem 0 1.4rem;
  color: #677294;
}

.field {
  margin-bottom: 1rem;
}

.field label {
  display: block;
  margin-bottom: 0.35rem;
  font-weight: 600;
  color: #2f3f65;
}

.field input {
  width: 100%;
  padding: 10px 12px;
  border: 1px solid #dde4f0;
  border-radius: 10px;
  background: #fafbff;
  transition: border-color 0.2s ease, box-shadow 0.2s ease;
}

.field input:focus {
  outline: none;
  border-color: #5ebd7f;
  box-shadow: 0 0 0 4px rgba(94, 189, 127, 0.16);
}

.login-btn {
  width: 100%;
  padding: 11px;
  border: none;
  border-radius: 10px;
  background: linear-gradient(90deg, #46c6e8 0%, #35a0d7 100%);
  color: #fff;
  font-weight: 700;
  font-size: 1rem;
  cursor: pointer;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.login-btn:hover,
.login-btn:focus {
  transform: translateY(-1px);
  box-shadow: 0 10px 22px rgba(31, 104, 177, 0.25);
}

.login-foot {
  margin-top: 1.2rem;
  text-align: right;
}

.login-foot a {
  color: #4b8af8;
  text-decoration: none;
  font-size: 0.92rem;
}

.login-foot a:hover {
  text-decoration: underline;
}
</style>

<style>
html, body {
  height: 100%;
  margin: 0;
  padding: 0;
  overflow: hidden;
}
body {
  box-sizing: border-box;
  width: 100vw;
  height: 100vh;
}
/* 隐藏所有滚动条 */
body::-webkit-scrollbar, html::-webkit-scrollbar {
  display: none;
}
</style>