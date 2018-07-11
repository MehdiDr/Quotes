<template>
    <div class="container">
        <app-add-quotes @quoteAdded='addQuotes'></app-add-quotes>
        <app-quotes-grid :quotes='quotes' @quoteDeleted='deleteQuote'></app-quotes-grid>
        <div class='row'>
            <div class='col-sm-12'>
                <div class="alert alert-info"> Info: Click on a quote to delete it /</div>
            </div>
        </div>
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
          },
          deleteQuote(i) {
              this.quotes.splice(i, 1);
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
