<template>
  <div id="app">
    <Title titleTextContent="Fcc Markdown Previewer Editor"/>
  </div>
</template>

<script>
import Title from './components/Title'

export default {
  name: 'App',
  components: {
    Title
  },
  mounted() {
    console.log('app is monted') // !DEBUG
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 40px;
}
</style>
