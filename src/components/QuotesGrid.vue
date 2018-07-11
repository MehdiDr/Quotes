<template>
  <div class='row'>
    <app-quotes v-for='(quote, i) in quotes' @click.native='deleteQuote(i)'>{{ quote }}</app-quotes>
  </div>
</template>

<script>
  import Quotes from './Quotes.vue'
  export default {
    props: ['quotes'],
    components: {
      appQuotes: Quotes
    },
    methods: {
      deleteQuote(i) {
        this.$emit('quoteDeleted', i);
      }
    }
  }
</script>

<style>

</style>

