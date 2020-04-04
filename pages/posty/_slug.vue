<template>
  <div class="container">
    <div class="section">
      <component :is="selectedArticle" />
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    attributes: {},
    selectedArticle: null,
  }),

  created() {
    const {
      params: { slug },
    } = this.$route;

    const markdown = require(`~/articles/${slug}.md`);
    this.attributes = markdown.attributes;
    this.selectedArticle = markdown.vue.component;
  },
};
</script>
