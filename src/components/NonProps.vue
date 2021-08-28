<template>
  <div>
    <h2 v-bind="$attrs">This is Non Properties</h2>
  </div>
</template>

<script>
export default {
  name: 'NonProps',

  inheritAttrs : false
}
</script>