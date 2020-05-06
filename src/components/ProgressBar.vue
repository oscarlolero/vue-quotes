<template>
  <section class="mb-4">
    <h2>Quotes added</h2>
    <div class="progress w-50">
      <div class="progress-bar" role="progressbar" :style="{width: quotesCount*(100/maxQuotes) + '%'}">{{ quotesCount }}/{{maxQuotes}}</div>
    </div>
  </section>
</template>

<script>
    export default {
        props: ['quotesCount', 'maxQuotes']
    }
</script>

<style scoped>
  .progress {
    margin-top: 20px !important;
  }
</style>