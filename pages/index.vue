<template>
  <div
    class="body"
    :class="[loading, isArticleVisible ? 'is-article-visible' : '']"
  >
    <div id="wrapper">
      <Header v-if="!timeout" @open-article="onOpenArticle" />
      <Main
        v-if="timeout"
        :article="article"
        :article-timeout="articleTimeout"
        @close-article="onCloseArticle"
      />
      <Footer v-if="!timeout" />
    </div>
    <div id="bg" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      isArticleVisible: false,
      timeout: false,
      articleTimeout: false,
      article: '',
      loading: 'is-loading',
    }
  },
  mounted() {
    this.$nextTick(function () {
      setTimeout(() => {
        this.loading = ''
      }, 100)
    })
  },
  methods: {
    onOpenArticle(article) {
      this.isArticleVisible = !this.isArticleVisible
      this.article = article

      setTimeout(() => {
        this.timeout = !this.timeout
      }, 325)

      setTimeout(() => {
        this.articleTimeout = !this.articleTimeout
      }, 350)
    },
    onCloseArticle(article) {
      this.articleTimeout = !this.articleTimeout

      setTimeout(() => {
        this.timeout = !this.timeout
      }, 325)
      setTimeout(() => {
        this.isArticleVisible = !this.isArticleVisible
        this.article = ''
      }, 350)
    },
  },
}
</script>
