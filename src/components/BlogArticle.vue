<template>
  <div v-if="article" class="container my-4">
    <h1>{{ article.title }}</h1>
    <p><strong>Autor:</strong> {{ article.author }} | <strong>Data:</strong> {{ article.date }}</p>
    <!-- Renderiza a imagem da pasta assets -->
    <div class="blog-article-img-container">
      <img
        :src="getImagePath(article.image)"
        alt="Imagem do artigo"
        class="img-fluid mb-3 blog-article-img"
      />
    </div>
    <div v-html="article.content"></div>
    <button class="btn btn-secondary mt-3" @click="$emit('back')">Back</button>
  </div>
  <div v-else>
    <p>Selecione um artigo para visualizar.</p>
  </div>
</template>

<style scoped>
.blog-article-img-container {
  display: flex;
  justify-content: center;
}

.blog-article-img {
  width: 70%;
  height: 100%;
}
</style>

<script>
export default {
  props: {
    article: {
      type: Object,
      default: null,
    },
  },
  methods: {
    getImagePath(imageName) {
      try {
        return `src/assets/${imageName}`;
      } catch (e) {
        console.error('Imagem não encontrada:', imageName, e);
        return '';
      }
    },
  },
};
</script>
