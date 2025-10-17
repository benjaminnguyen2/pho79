
<!-- import heroSrc from '@/assets/hero/pho79-hero.jpg' -->

<template>
  <section class="hero-banner" aria-label="Pho 79 featured banner">
      <img class="hero-banner-img" src="@/assets/hero/pho79-hero.jpg" alt="Pho 79 featured dish" decoding="async" />
      <div class="hero-banner-overlay">
        <h1 class="banner-title">Authentic Vietnamese Cuisine</h1>
        <RouterLink to="/menu" class="banner-cta">View Menu</RouterLink>
      </div>
    </section>
  <section class="main-section">
    <!-- <div class="pho-bowl">
      <img src="@/assets/home/flower.png" alt="" class="flower" />
      <img src="@/assets/home/flower.png" alt="" class="flipped-flower" />
    </div> -->
    <div class="content-wrapper">


      <!-- <div style="text-align: center; margin-bottom: 2rem">
        <RouterLink to="/menu" class="active-nav"
          ><button class="button-pho">Check out our Menu</button></RouterLink
        >
      </div> -->
      <div class="hours-navigation">
        <div class="business-hours">
        <p style="font-weight: 700; font-size: 1.5rem;">Opening Hours</p>
        <ul style="list-style: none">
          <li>
            <p class="hours-day">Monday</p>
            <p>Closed</p>
          </li>
          <li>
            <p class="hours-day">Tuesday</p>
            <p>11AM - 8PM</p>
          </li>
          <li>
            <p class="hours-day">Wednesday</p>
            <p>11AM - 8PM</p>
          </li>
          <li>
            <p class="hours-day">Thursday</p>
            <p>11AM - 8PM</p>
          </li>
          <li>
            <p class="hours-day">Friday</p>
            <p>11AM - 8PM</p>
          </li>
          <li>
            <p class="hours-day">Saturday</p>
            <p>11AM - 8PM</p>
          </li>
          <li>
            <p class="hours-day">Sunday</p>
            <p>11AM - 8PM</p>
          </li>
        </ul>
      </div>
      <div class="navigation">
        <div class="navigation-header">
          <p class="navigation-title">Come visit us in Barrie!</p>
          <p class="navigation-description">
            We are located at 165 Wellington Street West - Unit 7
          </p>
        </div>

        <div class="navigation-maps">
          <div class="map-container">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2851.2615002296416!2d-79.70652763358241!3d44.386753458178696!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x882aa33761cc8da7%3A0xacf6c4ee782fcfb9!2zUGjhu58gNzk!5e0!3m2!1sen!2sca!4v1755295086956!5m2!1sen!2sca"
              width="600"
              height="450"
              style="border: 0"
              allow="fullscreen"
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
      </div>

    </div>
  </section>
</template>

<style>
.business-hours {
  align-items: center;
  justify-content: center;
  display: flex;
  flex-direction: column;
  z-index: 1;
}
.navigation {
  display: flex;
  flex-direction: column;
}
.navigation-header {
  align-content: center;
}
.navigation-title {
  font-size: 1.5rem;
  font-weight: 700;
  text-align: center;
  @media only screen and (max-width: 1024px) {
    width: 100%;
    font-size: 1.5rem;
    text-align: center;
  }
}
.navigation-description {
  font-size: 1.25rem;
  text-align: center;
  @media only screen and (max-width: 1024px) {
    font-size: 1rem;
  }
}

.navigation-maps {
  margin-top: 1rem;
  width: 100%;
  @media only screen and (max-width: 1024px) {
    width: 100%;
    text-align: center;
    height: auto;
  }
  .map-container {
    position: relative;
    width: 100%;
    padding-bottom: 56.25%; /* 16:9 aspect ratio */
    height: 0;
    overflow: hidden;
    border-radius: 12px;
  }

  .map-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
}
.pho-bowl {
  display: flex;
  justify-content: center;
  align-items: center;
}
.flower {
  width: 30%;
  position: absolute;
  left: 0;
  top: 120px;
  z-index: 0;
  @media only screen and (max-width: 1750px) {
    width: 30%;
  }
  @media only screen and (max-width: 1024px) {
    display: none;
  }
}
.flipped-flower {
  width: 30%;
  transform: scaleX(-1);
  position: absolute;
  right: 0px;
  top: 50px;
  z-index: 0;
  @media only screen and (max-width: 1750px) {
    width: 30%;
  }
  @media only screen and (max-width: 1024px) {
    display: none;
  }
}
ul {
  padding: 0;
}
li {
  display: flex;
  flex-direction: row;
}
.hours-day {
  width: 12rem;
  font-size: 1rem;
}
.hours-navigation{
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  @media only screen and (max-width: 1024px) {
    flex-direction: column;
    align-items: center;
    gap: 2rem;
  }
}
/* ===== Normal homepage hero banner (below nav) ===== */
.hero-banner {
  position: relative;
  top: 1rem;
  width: 100%;
  height: clamp(240px, 40vh, 520px);
  overflow: clip;
  background: #000;
  isolation: isolate;
  margin: 0; /* flush to nav */
  opacity: 0;                 /* fade in */
  animation: bannerFade .6s ease .15s forwards;
}
.hero-banner-img {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;    /* adjust focal point if needed */
  display: block;
}
.hero-banner::after {         /* gradient for legibility */
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(180deg, rgba(0,0,0,.15), rgba(0,0,0,.45));
  z-index: 0;
}
.hero-banner-overlay {
  position: relative;
  z-index: 1;
  height: 100%;
  display: grid;
  place-items: center;
  text-align: center;
  padding: 16px;
  color: #fff;
}
.banner-title {
  font-size: clamp(1.5rem, 3.2vw, 2.5rem);
  margin: 0 0 10px 0;
  line-height: 1.2;
  text-shadow: 0 2px 10px rgba(0,0,0,.4);
}
.banner-cta {
  display: inline-block;
  padding: 10px 18px;
  border-radius: 999px;
  border: 1px solid rgba(255,255,255,.7);
  background: rgba(255,255,255,.08);
  backdrop-filter: blur(6px);
  font-weight: 600;
  color: #fff !important;
  text-decoration: none !important;
}
.banner-cta:hover {
  background: rgba(255,255,255,.16);

}

@keyframes bannerFade { to { opacity: 1; } }
</style>
