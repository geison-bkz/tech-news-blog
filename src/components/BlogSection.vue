<template>
  <div class="container my-5">
    <div v-if="!selectedArticleId">
      <div class="row">
        <div class="col-md-6" v-for="article in articles" :key="article.id">
          <BlogCard :article="article" @select-article="selectArticle" />
        </div>
      </div>
    </div>
    <div v-else>
      <BlogArticle :article="selectedArticle" @back="selectedArticleId = null" />
    </div>
  </div>
</template>

<script>
import BlogCard from './BlogCard.vue';
import BlogArticle from './BlogArticle.vue';
import blogData from '../../public/blogData.json';

export default {
  components: {
    BlogCard,
    BlogArticle,
  },
  data() {
    return {
      articles: blogData,
      selectedArticleId: null,
    };
  },
  computed: {
    selectedArticle() {
      return this.articles.find((article) => article.id === this.selectedArticleId);
    },
  },
  methods: {
    selectArticle(id) {
      this.selectedArticleId = id;
    },
  },
};
</script>
