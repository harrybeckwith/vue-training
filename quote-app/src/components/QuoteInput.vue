<template>
  <div>
    <textarea class="form-control" id="exampleFormControlTextarea1" rows="3" v-model="quote"></textarea>
    <button
      @click="gatherQuotes"
      v-if="quotes.length <= 9"
      type="submit"
      class="btn btn-primary"
    >Submit</button>
  </div>
</template>

<script>
export default {
  props: ["getQuote", "quotes"],
  data() {
    return {
      quote: ""
    };
  },
  methods: {
    gatherQuotes() {
      this.getQuote(this.quote);
      this.quote = "";
    }
  }
};
</script>

<style>
</style>
