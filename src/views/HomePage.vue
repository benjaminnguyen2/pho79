<template>
  <div class="main-section">
    <div class="pho-bowl">
      <img src="@/assets/home/flower.png" alt="" class="flower" />
      <img src="@/assets/home/flower.png" alt="" class="flipped-flower" />
    </div>
    <div class="content-wrapper">
      <div class="business-hours">
        <p style="font-weight: 700; padding-right: 4rem">Business<br />Hours</p>
        <p style="text-align: center">
          <span> Monday Closed<br />Tuesday - Sunday<br />11Am - 7PM </span>
        </p>
      </div>
      <div class="pho-bowl">
        <img src="@/assets/home/bowl.png" alt="" style="width: 400px" />
      </div>
      <div style="text-align: center; margin-bottom: 2rem">
        <RouterLink to="/menu" class="active-nav"
          ><button class="button-pho">Check out our Menu</button></RouterLink
        >
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
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2851.2615002296416!2d-79.70652763358241!3d44.386753458178696!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x882aa33761cc8da7%3A0xacf6c4ee782fcfb9!2zUGjhu58gNzk!5e0!3m2!1sen!2sca!4v1755295086956!5m2!1sen!2sca" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.business-hours {
  align-items: center;
  justify-content: center;
  display: flex;
  flex-direction: row;
  font-size: 2rem;
  z-index: 1;
  @media only screen and (max-width: 1024px) {
    font-size: 1.5rem;
  }
  @media only screen and (max-width: 550px) {
    font-size: 1rem;
  }
}
.navigation {
  display: flex;
  flex-direction: row;
  @media only screen and (max-width: 1024px) {
    flex-direction: column;
  }
}
.navigation-header {
  margin-right: 2rem;
}
.navigation-title {
  font-size: 2rem;
  font-weight: 700;
  padding-bottom: 1rem;

  @media only screen and (max-width: 1024px) {
    width: 100%;
    font-size: 1.5rem;
    text-align: center;
  }
}
.navigation-description {
  font-size: 1.5rem;
  @media only screen and (max-width: 1024px) {
    font-size: 1rem;
  }
}

.navigation-maps {
  text-align: right;
  width: 60%;
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
</style>
