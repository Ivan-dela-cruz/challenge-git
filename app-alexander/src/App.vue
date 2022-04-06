<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Login"/>
    <CardProduct />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import CardProduct from './components/shared/card-product.vue'


function data() {
  return {
    isLogging: false,
  }
}

/*
function created(){
  const token = localStorage.getItem('token')
  this.isLogging = token ? token : false
}*/

export default {
  name: 'App',
//  created,
  data,
  components: {
    HelloWorld,
    CardProduct,
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
