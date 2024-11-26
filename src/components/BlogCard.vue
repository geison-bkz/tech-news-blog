<template>
  <div class="card mb-6">
    <img :src="getImagePath(article.image)" class="card-img-top" alt="Imagem do artigo" />
    <div class="card-body">
      <h5 class="card-title">{{ article.title }}</h5>
      <p class="card-text">{{ article.excerpt }}</p>
      <button class="btn btn-primary" @click="$emit('select-article', article.id)">
        Read More
      </button>
    </div>
  </div>
</template>

<style scoped>
.card {
  width: 100%;
  height: 100%;
}
</style>

<script>
export default {
  props: {
    article: {
      type: Object,
      required: true,
    },
  },
  methods: {
    getImagePath(imageName) {
      try {
        console.log(imageName);
        return `src/assets/${imageName}`;
      } catch (e) {
        console.error('Imagem não encontrada:', imageName, e);
        return '';
      }
    },
  },
};
</script>
