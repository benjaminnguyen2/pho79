<script setup lang="ts">
import { ref } from 'vue';

const active = ref(0)

function next () {
    active.value++;
    if (active.value > 5) {
        active.value = 0
    }
}

function prev () {
    active.value--;
    if (active.value < 0) {
        active.value = 5
    }
}

function currentSlide(input: number) {
    active.value = input - 1
}
</script>

<template>
  <div class="main-section">
    <div class="content-wrapper">
      <h1 style="font-weight: 700; padding-bottom: 1rem">About Pho 79</h1>
      <p style="padding-bottom: 0.5rem">
        Sharing home-cooked meals during Tết, birthdays, and family celebrations has always been a
        way for us to connect and create lasting memories. The joy of bringing loved ones together
        inspired us to open our doors to the community, so everyone can experience the warmth, love,
        and tradition in every dish we serve.
      </p>
      <p>
        Pho 79 is more than just a Vietnamese restaurant—it’s a story of perseverance and new
        beginnings. Our head chef, inspired by his sister’s family, embarked on a journey filled
        with challenges to create new opportunities for his children in Canada while staying deeply
        connected to his Vietnamese roots. His story is one of hard work, family, and the pursuit of
        a brighter future.
      </p>
      <!-- <div class="item">
        <div class="polaroid">
          <img src="@/assets/about/family.jpg" alt="" />
        </div>
      </div> -->

      <!-- Container for the image gallery -->
      <div class="container">
        <button class="prev" @click="prev">&#10094;</button>
        <!-- Full-width images with number text -->
        <!-- <div class="card" v-for="card in cards" :key="card">
            {{card}}
        </div> -->
        <div :class="active == 0 ? 'mySlides' : 'hideSlide'">
          <img src="@/assets/about/pho.jpg" class="slideImage" />
        </div>

        <div :class="active == 1 ? 'mySlides' : 'hideSlide'">
          <img src="@/assets/about/com.jpg" class="slideImage" />
        </div>

        <div :class="active == 2 ? 'mySlides' : 'hideSlide'">
          <img src="@/assets/about/bunbohue.jpg" class="slideImage" />
        </div>

        <div :class="active == 3 ? 'mySlides' : 'hideSlide'">
          <img src="@/assets/about/bunchagio.jpg" class="slideImage" />
        </div>

        <div :class="active == 4 ? 'mySlides' : 'hideSlide'">
          <img src="@/assets/about/banhmi.jpg" class="slideImage" />
        </div>

        <div :class="active == 5 ? 'mySlides' : 'hideSlide'">
          <img src="@/assets/about/cafe.jpg" class="slideImage" />
        </div>

        <!-- Next and previous buttons -->
        <button class="next" @click="next">&#10095;</button>

        <!-- Image text -->
        <div class="caption-container">
          <p id="caption" class="numbertext">{{ active+1 }} / 6</p>
        </div>

        <!-- Thumbnail images -->
        <div class="row">
            
          <div class="column">
            <img
              class="demo cursor"
              src="@/assets/about/pho.jpg"
              style="width: 100%"
              @click="currentSlide(1)"
              alt="Pho"
            />
          </div>
          <div class="column">
            <img
              class="demo cursor"
              src="@/assets/about/com.jpg"
              style="width: 100%"
              @click="currentSlide(2)"
              alt="Com"
            />
          </div>
          <div class="column">
            <img
              class="demo cursor"
              src="@/assets/about/bunbohue.jpg"
              style="width: 100%"
              @click="currentSlide(3)"
              alt="Bun Bo Hue"
            />
          </div>
          <div class="column">
            <img
              class="demo cursor"
              src="@/assets/about/bunchagio.jpg"
              style="width: 100%"
              @click="currentSlide(4)"
              alt="Bun Cha Gio"
            />
          </div>
          <div class="column">
            <img
              class="demo cursor"
              src="@/assets/about/banhmi.jpg"
              style="width: 100%"
              @click="currentSlide(5)"
              alt="banh mi"
            />
          </div>
          <div class="column">
            <img
              class="demo cursor"
              src="@/assets/about/cafe.jpg"
              style="width: 100%"
              @click="currentSlide(6)"
              alt="coffee"
            />
          </div>
          
        </div>
      </div>
    </div>
  </div>
</template>
<style>
* {
  box-sizing: border-box;
}

.polaroid {
  display: flex;
  justify-self: center;
  align-items: center;
  background: #fff;
  padding: 1rem;
  box-shadow: 0 0.2rem 1.2rem rgba(0, 0, 0, 0.2);
}
.polaroid > img {
  max-width: 100%;
  height: auto;
}
.caption {
  font-size: 1.8rem;
  text-align: center;
  line-height: 2em;
}
.item {
  width: 50%;
  display: flex;
  justify-content: center; /* Center horizontally */
  align-items: center; /* Optional: center vertically inside its container */
  margin: 2rem auto; /* Center with auto margins */
  @media only screen and (max-width: 1024px) {
    min-width: 350px;
  }
}

.item .polaroid:before {
  content: '';
  position: absolute;
  z-index: -1;
  transition: all 0.35s;
}
.item:nth-of-type(4n + 1) {
  transform: scale(0.8, 0.8) rotate(5deg);
  transition: all 0.35s;
}
.item:nth-of-type(4n + 1) .polaroid:before {
  transform: rotate(6deg);
  height: 20%;
  width: 47%;
  bottom: 30px;
  right: 12px;
  box-shadow: 0 2.1rem 2rem rgba(0, 0, 0, 0.4);
}
.item:nth-of-type(4n + 2) {
  transform: scale(0.8, 0.8) rotate(-5deg);
  transition: all 0.35s;
}
.item:nth-of-type(4n + 2) .polaroid:before {
  transform: rotate(-6deg);
  height: 20%;
  width: 47%;
  bottom: 30px;
  left: 12px;
  box-shadow: 0 2.1rem 2rem rgba(0, 0, 0, 0.4);
}
.item:nth-of-type(4n + 4) {
  transform: scale(0.8, 0.8) rotate(3deg);
  transition: all 0.35s;
}
.item:nth-of-type(4n + 4) .polaroid:before {
  transform: rotate(4deg);
  height: 20%;
  width: 47%;
  bottom: 30px;
  right: 12px;
  box-shadow: 0 2.1rem 2rem rgba(0, 0, 0, 0.3);
}
.item:nth-of-type(4n + 3) {
  transform: scale(0.8, 0.8) rotate(-3deg);
  transition: all 0.35s;
}
.item:nth-of-type(4n + 3) .polaroid:before {
  transform: rotate(-4deg);
  height: 20%;
  width: 47%;
  bottom: 30px;
  left: 12px;
  box-shadow: 0 2.1rem 2rem rgba(0, 0, 0, 0.3);
}
.item:hover {
  filter: none;
  transform: scale(1, 1) rotate(0deg) !important;
  transition: all 0.35s;
}
.item:hover .polaroid:before {
  content: '';
  position: absolute;
  z-index: -1;
  transform: rotate(0deg);
  height: 90%;
  width: 90%;
  bottom: 0%;
  right: 5%;
  box-shadow: 0 1rem 3rem rgba(0, 0, 0, 0.2);
  transition: all 0.35s;
}

/* Photo Container */
* {
  box-sizing: border-box;
}

/* Position the image container (needed to position the left and right arrows) */
.container {
  position: relative;
  margin: 2rem auto 2rem auto;
  width: 50%;
}

/* Hide the images by default */
.mySlides {
  display: inline-block;
}

.hideSlide {
  display: none;
}

.slideImage {
  width: 100%;
}

/* Add a pointer when hovering over the thumbnail images */
.cursor {
  cursor: pointer;
}

/* Next & previous buttons */
.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 40%;
  width: auto;
  padding: 16px;
  margin-top: -50px;
  color: white;
  background-color: rgba(0, 0, 0, 0.3);
  font-weight: bold;
  font-size: 20px;
  border-radius: 0 3px 3px 0;
  user-select: none;
  -webkit-user-select: none;
  border: none;
}

/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

/* On hover, add a black background color with a little bit see-through */
.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

/* Number text (1/3 etc) */
.numbertext {
  color: #f2f2f2;
  font-size: 1rem;
}

/* Container for image text */
.caption-container {
  text-align: center;
  background-color: #222;
  padding: 2px 16px;
  color: white;
}

.row:after {
  content: '';
  display: table;
  clear: both;
}

/* Six columns side by side */
.column {
  float: left;
  width: 16.66%;
}

/* Add a transparency effect for thumnbail images */
.demo {
  opacity: 0.6;
}

.active,
.demo:hover {
  opacity: 1;
}
</style>

