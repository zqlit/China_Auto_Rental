<template>
  <div id="app">
    <nav>
      <router-link to="/">首页页面</router-link>
      <router-link to="/query">网点查询</router-link>
      <router-link to="/login">登录页面</router-link>
    </nav>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

nav {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
}

nav a {
  margin: 0 15px;
  text-decoration: none;
  color: #42b983;
  font-weight: bold;
}

nav a.router-link-exact-active {
  color: #35495e;
}
</style></nav>