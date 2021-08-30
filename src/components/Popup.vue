<template>
  <div>
    <h4>this is custom components</h4>
    <input type="text" v-model="name" /><br>
    <button @click="$emit('close',name)">Close</button>
  </div>
</template>

<script>
export default {
  name: 'Popup',
  data() {
    return {
      name: ''
    }
  },
  emits: ['close']

}
</script>