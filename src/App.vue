<template>
    <img alt="Vue logo" src="./assets/logo.png">
 <router-view />
</template>

<script>

export default {
  name: 'App',
  
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
.register input,.login input{
  width: 300px;
  height: 10px;
  padding: 15px;
  display: block;
  margin-bottom: 30px;
  margin-left: auto;
  margin-right: auto;
  border: 1px solid skyblue;
  border-radius: 10px;
  padding-bottom: 20px;
}
.register button,.login button{
  width: 300px;
  padding: 15px;
  height: 10px;
  color: white;
  background-color: skyblue;
  border: 1px solid black;
  font-size: 16px;
  text-align: center;
  padding-bottom: 30px;
  border-radius: 10px;
  cursor: pointer;
}
</style>
