<template>
  <div class='row'>
    <app-quotes v-for='quote in quotes'>{{ quote }}</app-quotes>
  </div>
</template>

<script>
  import Quotes from './Quotes.vue'
  export default {
    props: ['quotes'],
    components: {
      appQuotes: Quotes
    }
  }
</script>

<style>

</style>

