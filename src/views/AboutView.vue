<template>
  <div class="about-page">
    <h1>About Us</h1>
    <section>
      <h2>Our Mission</h2>
      <p>
        Our mission is to simplify and make the tech universe accessible. We aim to inspire and
        educate our readers, helping them to understand and keep up with the rapid changes in the
        tech industry.
      </p>
    </section>
    <section>
      <h2>What You Will Find Here</h2>
      <ul>
        <li>
          <strong>News and Trends</strong>: Stay updated with the latest tech news, from product
          launches to the latest market trends.
        </li>
        <li>
          <strong>Guides and Tutorials</strong>: Step-by-step guides to help you master new tools
          and technologies, whether you're a beginner or an experienced professional.
        </li>
        <li>
          <strong>Product Reviews</strong>: Honest and detailed reviews of gadgets, software, and
          services, so you can make informed decisions.
        </li>
        <li>
          <strong>Opinions and Insights</strong>: Opinion pieces and analyses that discuss the
          impact of new technologies on society and the future of work.
        </li>
      </ul>
    </section>
    <section>
      <h2>Our Team</h2>
      <p>
        We are a team of tech enthusiasts, developers, designers, and analysts who live and breathe
        innovation. Together, we combine our experience and passion to bring you relevant and
        high-quality content.
      </p>
    </section>
    <section>
      <h2>Contact Us</h2>
      <p>
        We love hearing from our readers! If you have suggestions, questions, or just want to chat
        about technology, feel free to reach out to us through our social media or by sending an
        email to <a href="mailto:contact@technewsblog.com">contact@technewsblog.com</a>.
      </p>
    </section>
  </div>

  <div class="container">
    <div class="row">
      <div class="col-6">
        <div class="card mb-6">
          <img src="/img/Erivelton.jpg" class="about-img" alt="Imagem do artigo" />
          <div class="card-body">
            <h5 class="card-title">Erivelton Silva de Araujo</h5>
            <p class="card-text">Gestão Financeira / USJT - Vila Leopoldina</p>
            <p class="card-text">4º Semestre</p>
          </div>
        </div>
      </div>
      <div class="col-6">
        <div class="card mb-6">
          <img src="/img/Micael.jpg" class="about-img" alt="Imagem do artigo" />
          <div class="card-body">
            <h5 class="card-title">Micael da Silva Morais</h5>
            <p class="card-text">Gestão Financeira / USJT - Vila Leopoldina</p>
            <p class="card-text">4º Semestre</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.about-page {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}
.about-page h1 {
  font-size: 2.5rem;
  margin-bottom: 20px;
  text-align: center;
}
.about-page h2 {
  font-size: 1.75rem;
  margin-top: 20px;
  margin-bottom: 10px;
}
.about-page p {
  font-size: 1rem;
  line-height: 1.6;
  margin-bottom: 10px;
}
.about-page ul {
  list-style-type: disc;
  margin-left: 20px;
}
.about-page li {
  margin-bottom: 10px;
}
.about-page a {
  color: #0070f3;
  text-decoration: underline;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

.row {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.col-6 {
  flex: 0 0 48%;
}

.card {
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  display: flex;
  flex-direction: column;
  height: 100%;
}

.card img {
  width: 100%;
  height: 700px;
  object-fit: cover;
  object-position: center;
  border-bottom: 1px solid #ddd;
  margin-bottom: -5px; /* Reduzir a margem inferior da imagem */
}

.card-body {
  padding: 8px; /* Reduzir o padding dentro do card body */
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}

.card-title {
  font-size: 1.5rem;
  margin-bottom: 4px; /* Reduzir a margem inferior do título */
}

.card-text {
  font-size: 1rem;
  color: #555;
  margin-bottom: 4px; /* Reduzir a margem inferior do texto */
}

/* Media Query para Dispositivos Móveis */
@media (max-width: 768px) {
  .col-6 {
    flex: 0 0 100%; /* Ocupar toda a largura da tela */
  }
  .card img {
    height: auto; /* Permitir que a imagem ajuste sua altura automaticamente */
  }
  .card-body {
    padding: 16px; /* Adicionar um pouco mais de espaço ao redor do texto */
  }
}
</style>
