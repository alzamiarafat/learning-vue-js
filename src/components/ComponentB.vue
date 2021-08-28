<template>
  <div>
    <h4>Component For B</h4>
    <ComponentC />
  </div>
</template>

<script>
import ComponentC from './ComponentC'
export default {
  name: 'ComponentB',

  components: {
    ComponentC
  }

}
</script>