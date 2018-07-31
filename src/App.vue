<template>
  <div>
    <h1>Hello world!</h1>
    <myUser
      v-for="user in users"

      v-bind:description="user.description" v-bind:name="user.name"
      v-bind:key="users.name"
    />
    <hr>
   <!-- 1 <loginForm @login="onLogin"/>-->
    <loginForm v-bind:onLogin="onLogin"/>
  </div>
</template>

<script>
  import user from './User';
  import loginForm from './components/LoginForm';

  export default {
    components: {
      myUser: user,
      loginForm
    },
    data() {
      return {
        users: [
          {name: "Alex", description: "This is our admin"},
          {name: "Fritz", description: "This is our manager"},
          {name: "John", description: "This is our client"}
        ]
      }
    },
    methods: {
    /* 1 onLogin(data) {
        return console.log("child component return", data);
      } */
      onLogin(data) {
        return console.log("child component return", data);
      }
    }
  }
</script>
