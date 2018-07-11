<template>
    <div class="container">
        <app-add-quotes @quoteAdded='addQuotes'></app-add-quotes>
        <app-quotes-grid :quotes='quotes'></app-quotes-grid>
    </div>
</template>

<script>
    import QuotesGrid from './components/QuotesGrid.vue'
    import AddQuotes from './components/AddQuotes.vue'
    export default {
      data: function() {
          return {
              quotes: [
                  'Just a test quote'
              ],
              maxQuote: 20
          }
      },
      methods: {
          addQuotes(quote) {
              this.quotes.push(quote)
          }
      },
      components: {
          appQuotesGrid: QuotesGrid,
          appAddQuotes: AddQuotes
      }
    }
</script>

<style>
</style>
