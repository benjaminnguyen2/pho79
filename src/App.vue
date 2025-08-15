<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import PhoFooter from './components/Pho79Footer.vue'
</script>

<template>
  <div class="layout">
    <div class="logo-grand-opening">
      <div style="display: inline-block">
        <RouterLink to="/"
          ><img alt="restaurant banner" class="home-logo" src="@/assets/logo/pho79WithShadows.png"
        /></RouterLink>
      </div>
      <div class="grand-opening-banner">Grand Opening! - August 29th, 2025</div>
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
.logo-grand-opening {
  display: flex;
  flex-direction: row;

  @media only screen and (max-width: 1200px) {
    display: flex;
    flex-direction: column;
  }
}
.layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.main-content {
  flex: 1;
}
.grand-opening-banner {
  text-align: center;
  font-size: 3rem;
  font-weight: 700;
  color: red;
  @media only screen and (max-width: 1024px) {
    font-size: 2rem;
  }
}
</style>
