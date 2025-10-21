<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import PhoFooter from './components/Pho79Footer.vue'
</script>

<template>
  <div class="layout">
    <div class="logo-grand-opening">
      <div style="display: inline-block">
        <RouterLink to="/"
          ><img alt="home" class="home-logo" src="@/assets/logo/pho79WithShadows.png"
        /></RouterLink>
      </div>
      <a
        href="https://www.ubereats.com/ca/store/pho-79-unit-7-165-wellington-street-west/WG2zobrcUYikpZJthD8o2A?diningMode=DELIVERY"
        target="_blank"
        rel="noopener noreferrer"
        class="order-now-btn"
        aria-label="Order now on Uber Eats"
      >
        Order Now
      </a>
      <!-- <div class="grand-opening-banner">Grand Opening! - September 2025</div> -->
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

  /* @media only screen and (max-width: 580px) {
    display: flex;
    flex-direction: column;
  } */
}
.layout {
  display: flex;
  flex-direction: column;
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
.order-now-btn {
  display: inline-block;
  background: linear-gradient(135deg, #f44336, #ff7043);
  color: white;
  margin-top: 1rem;
  font-weight: 600;
  font-size: 1.1rem;
  padding: 0.9rem 2rem;
  border-radius: 9999px;
  text-decoration: none;
  transition: all 0.3s ease;
  box-shadow: 0 4px 12px rgba(244, 67, 54, 0.3);
  height: 50%;
  max-width: 160px;
  margin-right: 1rem;
  margin-left: auto;
  @media only screen and (max-width: 579px) {
    font-size: 1rem;
    height: 30%;
    max-width: 120px;
    padding: 0.5rem 1rem !important;
    margin-top: 0.5rem;
  }
  @media only screen and (max-width: 400px) {
    font-size: 0.75rem;
  }
}

.order-now-btn:hover {
  transform: scale(1.05);
  box-shadow: 0 6px 18px rgba(244, 67, 54, 0.5);
  background: linear-gradient(135deg, #ff5722, #ff8a65);
}
</style>
