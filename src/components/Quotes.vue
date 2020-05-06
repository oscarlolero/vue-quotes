<template>
  <section class="quotes">
    <quote v-for="(quote, index) in quotes" :key="index" @click.native="deleteQuote(index)">
      {{ quote }}
    </quote>
  </section>
</template>

<script>
    import Quote from "./Quote";

    export default {
        props: ['quotes'],
        components: {
            quote: Quote
        },
        methods: {
            deleteQuote(index) {
                this.$emit('onQuoteDelete', index);
            }
        }
    }
</script>

<style scoped>
  .quotes {
    display: flex;
    flex-wrap: wrap;
  }
</style>