<template>
  <div>
    <h1>Hello world!</h1>
    <myUser
      v-for="user in users"

      v-bind:description="user.description"   v-bind:name="user.name"
      v-bind:key="users.name"
    />
  </div>
</template>

<script>
  import user from './User';

  export default {
    components: {
      myUser: user
    },
    data() {
      return {
        users: [
          {name: "Alex", description: "This is our admin"},
          {name: "Fritz", description: "This is our manager"},
          {name: "John", description: "This is our client"}
        ]
      }
    }
  }
</script>
