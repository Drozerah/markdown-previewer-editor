<template>
  <main>
    <textarea name="markdown" id="editor" cols="30" rows="10"></textarea>
    <div id="preview">the preview</div>
  </main>
</template>

<script>
export default {
  name: 'Previewer',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
main{
  margin-top: 40px;
  display: flex;
  justify-content: space-around;
  textarea, #preview{
    width: 48%;
    height: 80vh;
    padding: 20px;
    font-size: 20px;
  }
  #preview{
    border: 1px solid;
  }
}
</style>
