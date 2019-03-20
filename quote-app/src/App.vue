<template>
  <div class="container">
    <progress-bar :quotes="quotes"></progress-bar>
    <quote-input :getQuote="getQuote" :quotes="quotes"></quote-input>
    <quote
      v-for="(quote, index) in quotes"
      :key="index"
      :quote="quote"
      :current="index"
      :removeQuote="removeQuote"
    ></quote>
  </div>
</template>

<script>
import ProgressBar from "./components/ProgBar.vue";
import QuoteInput from "./components/QuoteInput.vue";
import Quote from "./components/Quote.vue";
export default {
  data() {
    return {
      quotes: []
    };
  },
  components: {
    ProgressBar,
    QuoteInput,
    Quote
  },
  methods: {
    getQuote(q) {
      this.quotes.push(q);
      if (this.quotes.length === 10) {
        alert("max of ten please remove items");
      }
    },
    removeQuote(i) {
      this.quotes.splice(i, 1);
    }
  }
};
</script>

<style>
</style>
