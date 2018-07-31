<template>
  <h3 v-if="email">Thanks for logging {{email}}</h3>
</template>

<script>
  export default {
    props: ['email']
  }
</script>
