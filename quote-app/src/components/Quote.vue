<template>
  <div class="card" @click="removeQuote(current)">
    <div class="card-body">{{quote}}</div>
  </div>
</template>

<script>
export default {
  props: ["quote", "removeQuote", "current"]
};
</script>

<style>
</style>
