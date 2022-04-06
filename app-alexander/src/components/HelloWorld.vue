<template>
  <div class="container">
    <div class="screen">
      <div class="login">
      <h1 class="title">{{ msg }}</h1>
      <input class="input input-email" type="email" placeholder="Ingrese su correo">
      <input class="input input-password" type="password" placeholder="Ingese su contraseña">
      <button class="btn btn-login" type="submit">Login</button>
    </div>
    </div>
  </div>

</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    email: String,
    password: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.container{
  display: flex;
  align-items: center;
  justify-content: center;
  min-width: 100vh;
}

.screen{
  position: relative;
  height: 600px;
  width: 360px;
  box-shadow: 0px 0;
}

.login{
  background-color: #42b983;
  border-radius: 20px;
  width: 420px;
}

.title{
  padding-top: 15px;
}

.input{
  border: 4px;
  border-radius: 20px;
  flex-direction: column;
  padding: 1em;
}

.input-email{
  margin: 4px;
  width: 290px;
}

.input-email:focus{
  border: none;
	background: #fff;
	padding: 10px;
	padding-left: 24px;
	font-weight: 700;
	width: 75%;
	transition: .2s;
}

.input-password{
  margin: 4px;
  width: 290px;
}

.input-password:focus{
  border: none;
  border-color: #fff solid 1px;
	background: #fff;
	padding: 10px;
	padding-left: 24px;
	font-weight: 700;
	width: 75%;
	transition: .2s;
}

.btn{
  border: 4px;
  border-radius: 10px;
  padding: .5em;
}

.btn-login{
  margin: 4px;
  background-color: #7FFFD4;
  width: 100px;
  text-align: center;
  
}

.btn-login:hover{
  background-color: #1d7c5d;
  color: #fff;
  cursor: pointer;
}
</style>
