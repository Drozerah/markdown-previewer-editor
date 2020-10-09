<template>
  <div id="app">
    <Title titleTextContent="Fcc Markdown Previewer Editor"/>
    <Previewer/>
  </div>
</template>

<script>
import Title from './components/Title'
import Previewer from './components/Previewer'

export default {
  name: 'App',
  components: {
    Title,
    Previewer
  },
  mounted() {
    console.log('app is monted') // !DEBUG
  }
}
</script>

<style>
*{
  box-sizing: border-box;
  font-family: monospace;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 40px;
}
</style>
