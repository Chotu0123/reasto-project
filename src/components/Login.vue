<template>
<h1>Login</h1>
<h2>How may I help you</h2>
<div class="login">
    <input type="text" v-model="email" placeholder="Enter Email" />
    <input type="password" v-model="password" placeholder="Enter Password" />
    <button v-on:click="login"> Login</button>
    <p>
      <router-link to='/sign-up'>Sign-Up</router-link>
      </p>
  </div>
</template>
<script>
import axios from 'axios'
export default {
    name:'Login',
    data()
    {
        return{
            email:'',
            password:''
        }
    },
    methods:{
        async login()
        {
            let result =await axios.get(
                'http://localhost:3000/users?email=${this.email}&password=${thi.password}'
            )
            if (result.status == 200 && result.data.length>0) {
        localStorage.setItem("users-info", JSON.stringify(result.data[0]));
        this.$router.push({ name: "Home" });
      }
            console.warn(result)
        }
    }
}
</script>
