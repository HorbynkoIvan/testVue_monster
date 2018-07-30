<template>
  <div>
    <h3>{{upperCaseName()}}</h3>
    <p>{{description}}</p>
  </div>
</template>

<script>
  export default {
    /*props: ['name', 'description'], */
    props: {
      name: {
        type: String,
        default: 'Not set'
      },
      description: {
        type: String,
        required: true
      }
    },
    methods: {
      upperCaseName() {
        return this.name.toUpperCase()
      }
    }
  }
</script>
