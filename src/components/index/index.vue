<template>
  <div class="container">
    <div class="button" @click="getHtml">获取HTML</div>
    <markdown ref="markdown"></markdown>
  </div>
</template>

<script>
  import Markdown from 'base/markdown/markdown'

  export default{
    props: {},
    data() {
      return {}
    },
    computed: {},
    methods: {
      getHtml() {
        this.$refs.markdown.getHtml()
      }
    },
    components: {
      Markdown
    }
  }
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
  .container {
    position: relative;
    .button {
      position: absolute;
      top: 0;
      left: 0;
      z-index: 99999999;
    }
  }
</style>
