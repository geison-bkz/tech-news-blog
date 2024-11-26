<script setup>
import { RouterLink } from 'vue-router';
</script>
<template>
  <nav class="navbar navbar-expand-lg py-4">
    <div class="container">
      <RouterLink class="navbar-brand fw-bold" to="/">Technews</RouterLink>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item ms-0 ms-md-3">
            <RouterLink class="nav-link" aria-current="page" to="/">Home</RouterLink>
          </li>
          <li class="nav-item ms-0 ms-md-3">
            <RouterLink class="nav-link" to="/about">About </RouterLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.navbar-brand {
  font-size: 30px;
}

.nav-link {
  font-size: 18px !important;
  font-weight: 500;
}

.navbar-brand,
.text-primary {
  color: #0a58ca !important;
}

.btn-primary {
  background-color: #0a58ca !important;
  border: none;
}

.nav-link:hover {
  color: #0a58ca;
}
</style>
