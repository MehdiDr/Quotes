<template>
    <div class="container">
        <app-quotes-grid :quotes='quotes'></app-quotes-grid>
    </div>
</template>

<script>
    import QuotesGrid from './components/QuotesGrid.vue'
    export default {
      data: function() {
          return {
              quotes: [
                  'Just a test quote'
              ],
              maxQuote: 20
          }
      },
      components: {
          appQuotesGrid: QuotesGrid
      }
    }
</script>

<style>
</style>
