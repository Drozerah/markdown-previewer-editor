<template>
  <div id="app">
    <Title titleTextContent="Markdown Previewer Editor"/>
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
  }
}
</script>

<style lang='scss'>
@import '../src/assets/css/reset.css';
*{
  box-sizing: border-box;
}
#app {
  margin-top: 40px;
}
</style>
