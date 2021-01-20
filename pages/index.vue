<template>
  <div id="wrapper" class="container">
    <Header @open-article="onOpenArticle" />
    <Footer />
  </div>
</template>

<script>
export default {
  methods: {
    onOpenArticle(label) {},
  },
}
</script>
