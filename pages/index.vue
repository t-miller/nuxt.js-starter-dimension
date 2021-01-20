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

<style>
@import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro:ital,wght@0,300;0,600;1,300;1,600&display=swap');
</style>
