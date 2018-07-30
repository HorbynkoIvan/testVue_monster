<template>
  <div>
    <h3>Login Form</h3>
    <div>
      <label>Email</label>
      <input type="email" v-model="email">
    </div>
    <div>
      <label>Password</label>
      <input type="password" v-model="password">
    </div>
    <button @click="login">Submit</button>
  </div>
</template>

<script>
export default {
  data(){
    return{
      email: "",
      password:""
    }
  },
  methods:{
    login(){
      console.log(`email: ${this.email} && password: ${this.password}`)
    }
  }
}
</script>
