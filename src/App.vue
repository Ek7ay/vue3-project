<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
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
  color: #2c3e50;
  overflow-y: auto; /* Ensure vertical scrolling works */
  overflow-x: hidden; /* Prevent horizontal scrolling */
}

#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

/* Custom scrollbar styling */
::-webkit-scrollbar {
  width: 10px;
  height: 10px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1;
  border-radius: 5px;
}

::-webkit-scrollbar-thumb {
  background: #c1c1c1;
  border-radius: 5px;
}

::-webkit-scrollbar-thumb:hover {
  background: #a8a8a8;
}

/* Firefox scrollbar */
* {
  scrollbar-width: thin;
  scrollbar-color: #c1c1c1 #f1f1f1;
}
</style>
