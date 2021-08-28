<template>
  <h2>Full Name: {{ firstName }} {{ lastName }}</h2>
  <h3>Computed Full Name: {{ fullName }}</h3>
  <h2>From Component</h2>
</template>

<script>
export default {
  name: "Greet",
  props: ['firstName', 'lastName', 'fullName']
}
</script>