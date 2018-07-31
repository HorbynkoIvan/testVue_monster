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
    props: ['onLogin'],
    data() {
      return {
        email: "",
        password: ""
      }
    },
    methods: {
      login() {
        // console.log(`email: ${this.email} && password: ${this.password}`)
        //There is 3 methods to pass data from child to parent component
        //1) this.$emit. emit realized on publish/subscribe principe.
        /*1  this.$emit('login', {
            email: this.email,
            password: this.password
          })*/
        this.onLogin({
          email: this.email,
          password: this.password
        })
      }
    }
  }
</script>
