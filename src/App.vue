<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="banner">
    <div class="banner-content">
      <!-- <img class="image-right" src="@/assets/logo/flower.png" alt="" /> -->
      <img alt="restaurant banner" class="home-logo" src="@/assets/logo/pho79WithShadows.png" />
      <nav>
        <RouterLink to="/" class="active-nav">Home</RouterLink>
        <RouterLink to="/menu" class="active-nav">Menu</RouterLink>
        <RouterLink to="/about" class="active-nav">About</RouterLink>
        <RouterLink to="/gallery" class="active-nav">Gallery</RouterLink>
      </nav>
    </div>
  </div>
  <RouterView />
  <div class="scroll-test"></div>
  <div class="footer">
    <div class="content-wrapper">
      <div class="address-map">
        <div class="address-information">
          <p>
            Pho 79 <br />Vietnamese Cuisine <br />
            Unit 7 - 165 Wellington Street West <br />Barrie, ON L4N 1L7
          </p>
        </div>
      </div>
      <h4 class="copyright">© PHO 79 2025 - ALL RIGHTS RESERVED</h4>
    </div>
  </div>
</template>

<style scoped></style>
