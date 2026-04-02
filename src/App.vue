<template>
  <div id="app">
    <!-- Demo Element Plus button -->
    <div class="demo-banner">
      <el-button type="primary" @click="showMessage">Element Plus Button (Click me!)</el-button>
      <span class="demo-text">Less and Element Plus are installed and working!</span>
    </div>
    <router-view />
  </div>
</template>

<script>
import { ElMessage } from 'element-plus'

export default {
  name: 'App',
  methods: {
    showMessage() {
      ElMessage.success('Element Plus is working correctly!')
    }
  }
}
</script>

<style lang="less">
// Define Less variables
@primary-color: #409eff;
@secondary-color: #67c23a;
@text-color: #2c3e50;
@bg-color: #f5f7fa;
@scrollbar-width: 10px;
@border-radius: 5px;

/* Global styles */
html, body {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
}

body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: @text-color;
  overflow-y: auto; /* Ensure vertical scrolling works */
  overflow-x: hidden; /* Prevent horizontal scrolling */
  background-color: @bg-color;
}

#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

// Demo banner styling using Less features
.demo-banner {
  background: linear-gradient(135deg, @primary-color, lighten(@primary-color, 20%));
  padding: 15px 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
  
  .demo-text {
    color: white;
    font-weight: bold;
    font-size: 16px;
    
    // Nested selector with pseudo-class
    &:hover {
      text-shadow: 0 0 5px rgba(255, 255, 255, 0.8);
    }
  }
  
  // Using mixin-like pattern
  .el-button {
    box-shadow: 0 4px 12px rgba(@primary-color, 0.3);
    
    &:hover {
      transform: translateY(-2px);
      transition: transform 0.2s ease;
    }
  }
}

/* Custom scrollbar styling using Less variables */
::-webkit-scrollbar {
  width: @scrollbar-width;
  height: @scrollbar-width;
}

::-webkit-scrollbar-track {
  background: lighten(@primary-color, 40%);
  border-radius: @border-radius;
}

::-webkit-scrollbar-thumb {
  background: @primary-color;
  border-radius: @border-radius;
  
  &:hover {
    background: darken(@primary-color, 10%);
  }
}

/* Firefox scrollbar */
* {
  scrollbar-width: thin;
  scrollbar-color: @primary-color lighten(@primary-color, 40%);
}
</style>
