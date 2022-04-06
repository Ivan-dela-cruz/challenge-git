<template>
  <div id="app" class="container">
    <img alt="Vue logo" src="./assets/logo.png" v-if="token==''"> 
    <loginUser v-if="token==''"/>
    <listProduct/>
  </div>
</template>

<script>
import loginUser from '@/components/shared/loginUser.vue'
import listProduct from '@/components/shared/listProduct.vue'

function mounted(){
  this.token = localStorage.getItem('token');
}

function data(){
  return {
    token: ''
  }
}

export default {
  name: 'App',
  components: {
    loginUser,
    listProduct
  },
  mounted,
  data
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
