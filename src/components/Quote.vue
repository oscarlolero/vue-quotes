<template>
  <div>
    <slot></slot>
  </div>
</template>

<script>
</script>

<style scoped>
  div {
    border: 2px solid gray;
    padding: 30px;
    margin: 10px;
  }
  div:hover {
    cursor: pointer;
    background-color: palevioletred;
  }
</style>