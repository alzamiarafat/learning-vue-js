<template>
  <div>
    <h4>Component For C {{ username}}</h4>
  </div>
</template>

<script>
export default {
  name: 'ComponentC',

  inject: {
    username: ['username']
  }
}
</script>