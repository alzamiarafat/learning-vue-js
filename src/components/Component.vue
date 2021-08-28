<template>
  <div>
    <h3>Component</h3>
    <ComponentA />
    <h1>{{ username }}</h1>
  </div>
</template>

<script>
import ComponentA from './ComponentA'
export default {
  name: 'Component',
  components: {
    ComponentA
  },
  inject: ['username']
}
</script>