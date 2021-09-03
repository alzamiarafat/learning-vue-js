<template>
  <div class="card">
    <div class="card-header">
      <slot name="header"></slot>
    </div>
    <div class="card-header">
      <slot><h1>This is default content</h1></slot>
    </div>
    <div class="card-footer">
      <slot name="footer"></slot>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Card',

}
</script>

<style>
.card{
  box-shadow: 1px 1px 10px gray;
  width: 30%;
  padding: 5px;
  margin-bottom: 50px;
}
</style>