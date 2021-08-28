<template>
  <div>
    <h4>Component For A</h4>
    <ComponentB />
  </div>
</template>

<script>
import ComponentB from './ComponentB'
export default {
  name: 'ComponentA',

  components: {
    ComponentB
  }

}
</script>