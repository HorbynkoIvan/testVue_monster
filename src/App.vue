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
    <successMessage :email="email"/>
  </div>
</template>

<script>
  import user from './User';
  import loginForm from './components/LoginForm';
  import successMessage from './components/SuccessMessage';

  export default {
    components: {
      myUser: user,
      loginForm,
      successMessage
    },
    data() {
      return {
        users: [
          {name: "Alex", description: "This is our admin"},
          {name: "Fritz", description: "This is our manager"},
          {name: "John", description: "This is our client"}
        ],
        email: ""
      }
    },
    methods: {
    /* 1 onLogin(data) {
        return console.log("child component return", data);
      } */
      onLogin(data) {
        this.email = data.email;
        return console.log("child component return", data);
      }
    }
  }
</script>
