<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/evenness">平整度检测</router-link> |
    <router-link to="/crack">幕墙爆裂检测</router-link> |
    <el-button
      @click="goHome"
      size="small"
      color="#409EFF"
      style="color: white"
      round
    >
      返回主页
    </el-button>
  </nav>
  <router-view />
</template>

<script setup>
const goHome = () => {
  window.location.href = "http://localhost:3000";
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #1d719e;
    }
  }
}
</style>
