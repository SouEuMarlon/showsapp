<script setup>
import GameOfThrones from './components/GameOfThronesCards.vue';
</script>

<template>
  <main>
    <h1>HERO</h1>
    <Suspense>
      <template #default>
        <GameOfThrones />
      </template>
      <template #fallback>
        <div class="loading_wrapper">
          <p class="loading_text">Loading <span class="loading_dots">...</span></p>
        </div>
      </template>
    </Suspense>
  </main>
</template>

<style scoped>
  .loading_text {
    font-size: 1.2rem;
  }

  .loading_dots {
    animation: loading 1s infinite;
  }

  @keyframes loading {
    0% {
      opacity: 0;
    }
    50% {
      opacity: 1;
    }
    100% {
      opacity: 0;
    }
  }
</style>
