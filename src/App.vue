<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import PhoFooter from './components/Pho79Footer.vue'
</script>

<template>
  <div class="layout">
    <div style="display: inline-block">
      <RouterLink to="/"
        ><img alt="restaurant banner" class="home-logo" src="@/assets/logo/pho79WithShadows.png"
      /></RouterLink>
    </div>

    <nav>
      <RouterLink to="/" class="active-nav">Home</RouterLink>
      <RouterLink to="/menu" class="active-nav">Menu</RouterLink>
      <RouterLink to="/about" class="active-nav">About</RouterLink>
      <!-- <RouterLink to="/gallery" class="active-nav">Gallery</RouterLink> -->
    </nav>
    <main class="main-content">
      <RouterView />
    </main>

    <PhoFooter />
  </div>
</template>

<style scoped>
.layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.main-content {
  flex: 1;
}
</style>
