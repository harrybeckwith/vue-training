<template>
  <div class="progress">
    <div
      class="progress-bar"
      role="progressbar"
      v-bind:style="{width: (quotes.length * 10) + '%'}"
      aria-valuenow="50"
      aria-valuemin="0"
      aria-valuemax="100"
    >{{quotes.length}} / 10</div>
  </div>
</template>

<script>
export default {
  props: ["quotes"]
};
</script>

<style>
</style>