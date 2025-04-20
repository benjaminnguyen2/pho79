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
      <div class="item">
        <div class="polaroid">
          <img src="@/assets/about/family.jpg" alt="" />
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
</style>
