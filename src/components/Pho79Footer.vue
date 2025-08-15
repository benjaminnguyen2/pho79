<template>
  <footer class="footer-1">
    <div class="content-wrapper">
      <div class="footer-info">
        <p class="footer-text-2 footer-left">© PHO 79 2025 - ALL RIGHTS RESERVED</p>
        <!-- <div class="footer-copyright footer-center">
          <div class="footer-social footer-center">
            <img
              src="@/assets/logo/instagramLogo.png"
              alt="instagram"
              class="footer-social-icon-instagram"
            />
            <img
              src="@/assets/logo/googleIcon.png"
              alt="google"
              class="footer-social-icon-google"
            />
            <img src="@/assets/logo/yelpLogo.png" alt="yelp" class="footer-social-icon-yelp" />
          </div>
        </div> -->
        <p class="footer-text-2 footer-right">
          <span class="footer-address-span">Pho 79</span>
          <span>
            <br />Vietnamese Cuisine<br />Unit 7 - 165 <br />Wellington Street West<br />Barrie, ON
            L4N 1L7
          </span>
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts"></script>

<style>
.footer {
  padding: 2.5rem;
  background-color: #0e0e0e;
  @media only screen and (max-width: 550px) {
    padding: 1.25rem;
  }
}

.footer-info {
  display: flex;
  flex-direction: row;
  justify-content: space-between !important;
  @media only screen and (max-width: 1024px) {
    align-items: center;
    flex-direction: column;
    width: 100%;
  }
}

.footer-copyright {
  display: flex;
  gap: 1.25rem;
  @media only screen and (max-width: 1024px) {
    width: 100%;
    flex-direction: column;
    text-align: center;
  }
  @media only screen and (max-width: 550px) {
    flex-direction: column;
  }
}
.footer-social {
  align-self: center;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 1.25rem;
  @media only screen and (max-width: 550px) {
    word-wrap: 100%;
  }
}
.footer-social-icon-instagram {
  height: 4.63rem;
  width: 40%;
  object-fit: contain;
  @media only screen and (max-width: 1024px) {
    width: 80%;
  }
}
.footer-social-icon-google {
  height: 4.63rem;
  width: 36%;
  object-fit: contain;
  @media only screen and (max-width: 1024px) {
    width: 70%;
  }
}
.footer-social-icon-yelp {
  height: 4.38rem;
  align-self: flex-end;
  width: 24%;
  object-fit: contain;
  @media only screen and (max-width: 1024px) {
    width: 60%;
  }
}
.footer-address-span {
  font-weight: 700;
}

.footer-1 {
  background-color: var(--black_900);
  padding: 2rem;
  @media only screen and (max-width: 550px) {
    padding: 1.25rem;
  }
}
.footer-address-2 {
  align-self: center;
  width: 20%;
  line-height: 1.81rem;
  @media only screen and (max-width: 1024px) {
    width: 100%;
  }
}
.footer-text-2 {
  color: #ffffff;
}
.footer-left {
  font-size: 1rem;
  width: 30%;
  text-align: left;
  @media only screen and (max-width: 1024px) {
    width: 100%;
    text-align: center !important;
  }
}
.footer-right {
  font-size: 1rem;
  width: 30%;
  @media only screen and (max-width: 1024px) {
    width: 100%;
    text-align: center !important;
  }
}
.footer-center {
  justify-content: center;

  width: 40%;
  margin: 0 10px;
  @media only screen and (max-width: 1024px) {
    text-align: center !important;
    justify-content: center;
  }
}
</style>
