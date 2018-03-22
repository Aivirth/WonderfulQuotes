<template>
    <div class="container">
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        <quote-grid :quotes="quotes"></quote-grid>
    </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
export default {
  data() {
    return {
      quotes: ["quote placeholder"],
      maxQuotes: 10
    };
  },
  components: {
    quoteGrid: QuoteGrid,
    appNewQuote: NewQuote
  },
  methods: {
    newQuote(quote) {
      this.quotes.push(quote);
    }
  }
};
</script>

<style>

</style>
