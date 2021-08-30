<template>
  <div>
    <h4>this is custom components</h4>
    <button @click="$emit('close','al zami arafat')">Close</button>
  </div>
</template>

<script>
export default {
  name: 'Popup',
  emits: ['close']

}
</script>