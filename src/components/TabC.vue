<template>
  <h3>This is tab C component.</h3>
  <input type="text" v-model="name"/>
</template>

<script>
export default {
  name: "TabC",

  data() {
    return {
      name: ''
    }
  }
}
</script>

<style scoped>
h3{
  color: green;
}
</style>