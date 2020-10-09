<template>
  <div class="title">
    <h1>{{ titleTextContent }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Title',
  props: {
    titleTextContent: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-family: monospace;
  font-size: 28px;
  text-align: center;
}
</style>
