<script setup lang="ts">
import logoSingle from "../assets/img/single.png";
import polygono from "../assets/img/polygono.png";

const links = {
  urls: {
    logoSingle,
    polygono,
  },
};
</script>

<template>
  <div class="card-work">
    <div class="text-work">
      <h1>WORK EXPERIENCE</h1>
    </div>

    <div class="experience">
      <div class="time-gap">
        <div class="line"></div>
        <div class="polygono">
          <img :src="links.urls.polygono" alt="" />
        </div>
      </div>

      <div class="card-work-place">
        <div class="logo-place">
          <img :src="links.urls.logoSingle" alt="" />
        </div>
        <div class="text">
          <h1>Front-End Developer</h1>
          <h2>Single Software</h2>
          <h3>Jan 2025 - present</h3>
          <p>Desenvolvimento de aplicações front-end</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.time-gap {
  position: relative;
}

.card-work {
  max-width: 327px;
  margin: 50px auto 100px;
}

.text-work h1 {
  font-family: "Poppins", "Inter", sans-serif;
  font-weight: 500;
  font-size: 45px;
  text-align: left;
  color: #111827;
  margin: 0px 0px 20px;
}

.experience {
  display: flex;
}

.card-work-place {
  display: flex;
  margin: 7px 20px;
  font-family: "Poppins", "Inter", sans-serif;
  color: #111827;
}

.card-work-place .text {
  margin-left: 10px;
}

.card-work-place h1 {
  margin: 0 0;
  font-size: 21px;
  font-weight: bold;
}

.card-work h2 {
  margin: 0 0;
  font-weight: 500;
  font-size: 20px;
}

.card-work h3 {
  margin: 7px 0;
  font-weight: 300;
  font-size: 16px;
}

.line {
  height: 186px;
  width: 4px;
  background-color: #007acc;
}

.polygono {
  position: absolute;
  left: 0px;
  top: 20px;
}
</style>
