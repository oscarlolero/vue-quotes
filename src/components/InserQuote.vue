<template>
  <section>
    <h5>Quote</h5>
    <div class="form-group">
      <textarea class="form-control" id="exampleFormControlTextarea1" rows="3" v-model="writtenQuote"></textarea>
      <button class="btn btn-success btn-sm mt-3" @click="saveQuote">Guardar</button>
    </div>
  </section>
</template>

<script>
    export default {
        data() {
            return {
                writtenQuote: ''
            }
        },
        methods: {
            saveQuote() {
                this.$emit('onQuoteAdded', this.writtenQuote);
            }
        }
    }
</script>

<style scoped>
  textarea {
    width: 400px;
  }
</style>