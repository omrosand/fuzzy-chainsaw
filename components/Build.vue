<script setup>
const slides = ["carousel1", "carousel2", "carousel3", "carousel4"];
</script>
<template>
  <div>
    <div class="imageContainer">
      <h2>Bygg ditt eget sjokoladehus</h2>
      <p>Lorem ipsum dolor sit amrt hyst</p>
      <Carousel class="carousel" v-slot="{ currentSlide }">
        <Slide v-for="(slide, index) in slides" :key="index">
          <div v-show="currentSlide === index + 1" class="slideContainer">
            <img :src="`/img/${slide}.png`" alt="bildekarusell bilde" />
            <h3>{{ `Navn hus ${currentSlide}` }}</h3>
          </div>
        </Slide>
      </Carousel>
      <Button path="bygg-sjokoladehus">Bygg sjokoladehus</Button>
    </div>
  </div>
</template>
<style scoped>
.imageContainer {
  background-image: url("/img/build.jpg");
  background-size: cover;
  background-position: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  color: var(--textLight);
  text-shadow: 2px 2px 5px black;
  padding: 3em 0;
}
h2 {
  font-size: 2rem;
  text-transform: uppercase;
  font-weight: 900;
}
p {
  font-weight: 600;
}
h3 {
  width: 240px;
  display: flex;
  justify-content: center;
  font-size: 2rem;
  background-color: rgb(0, 77, 0);
}
.carousel {
  position: relative;
  max-height: 420px;
  height: 420px;
  margin: 2em 0;
}
.slideContainer {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  max-height: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
img {
  min-width: 100%;
  height: 100%;
  filter: drop-shadow(0px 0px 7px black);
}
</style>
