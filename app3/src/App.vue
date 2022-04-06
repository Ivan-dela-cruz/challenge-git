<template>
  <div id="app" class="container">
    <img alt="Vue logo" src="./assets/logo.png">
    <loginUser/>
  </div>
</template>

<script>
import loginUser from '@/components/shared/loginUser.vue'

export default {
  name: 'App',
  components: {
    loginUser
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
