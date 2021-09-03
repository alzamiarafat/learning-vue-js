<template>
  <div v-for="name in names" :key="name">
    <slot :fName="name.fName" :lName="name.lName"></slot>
  </div>
</template>

<script>
export default {
  name: 'NameList',
  data() {
    return {
      names: [
        {
          fName: 'al Zami',
          lName: 'arafat',
        },
        {
          fName: 'hasib',
          lName: 'arafat',
        },
      ]
    }
  }
}
</script>