<template>
  <main>
    <section>
      <div>Editor</div>
      <textarea id="editor" v-model="editor" spellcheck="false"></textarea>
    </section>
    <section>
      <div>Preview</div>
      <div id="preview" class="markdown-body" v-html="markedownize">
      </div>
    </section>
  </main>
</template>

<script>

import marked from 'marked'
import defaultEditorContent from '../modules/content'
import hljs from 'highlight.js'

marked.setOptions({
  gfm: true,
  breaks: true,
  highlight: function(code, language) {
    const validLanguage = hljs.getLanguage(language) ? language : 'plaintext'
    return hljs.highlight(validLanguage, code).value
  }
})

export default {
  name: 'Previewer',
  data() {
    return {
      editor: defaultEditorContent
    }
  },
  mounted() {
    console.log('Previewer mounted!') // !DEBUG
  },
  computed: {
    markedownize: function() {
      return marked(this.editor)
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/css/github-markdown.css';
@import '~highlight.js/styles/github.css';
main{
  margin-top: 40px;
  display: flex;
  justify-content: space-around;
  section{
    font-family: monospace;
    width: 49.85%;
    height: 78vh;
    div:first-of-type{
      padding: 20px;
      text-transform: uppercase;
      color:#828a9e;
      border: 1px solid #E7E7E7;
    }
  }
  textarea, #preview{
    width: 100%;
    height: 100%;
    padding: 20px;
    font-size: 20px;
    border: 1px solid #E7E7E7;
  }
  textarea{
    font-family: monospace;
    font-size: 14px;
    &:focus {
    outline: none !important;
    background-color: #fbfcff;
}
  }
  #preview{
    // white-space: pre-line;
    overflow: scroll;
    font-size: 14px !important;
  }
}
</style>
