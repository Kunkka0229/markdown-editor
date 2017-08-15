<template>
  <div class="markdown-content">
    <div class="markdown markdown-body">
      <textarea name="markdown" id="markdown"></textarea>
    </div>
  </div>
</template>

<script>
  import SimpleMDE from 'simplemde'

  export default{
    data() {
      return {}
    },
    created() {
      this.$nextTick(() => {
        /* eslint-disable no-unused-vars */
        this.simplemde = new SimpleMDE({
          element: document.getElementById('markdown'),
          autoDownloadFontAwesome: false,
          status: false
//          toolbar: ['bold', 'italic', 'strikethrough', '|', 'heading-1', 'heading-2', 'heading-3', '|', 'quote', 'table']
        })
      })
    },
    computed: {},
    methods: {
      getHtml() {
        console.log(this.simplemde)
        let testPlain = this.simplemde.value()
        let textMarkdown = this.simplemde.markdown(testPlain)
        console.log(textMarkdown)
      }
    },
    components: {}
  }
</script>

<style rel="stylesheet/scss" lang="scss">
  .markdown-content {
    position: fixed;
    top: 0;
    bottom: 0;
    width: 97%;
    padding: 20px;
    justify-content: center;
    align-items: center;
    .markdown, .effect {
      flex: 1;
      height: 100%;
    }
    .markdown {
      .editor-toolbar {
        border-top-right-radius: 0;
      }
      .CodeMirror {
        height: 90%;
      }
    }
  }
</style>
