<script setup>
const slides = ["c1", "c2", "c3"];
const activeSlide = ref(0);
const slideCount = slides.length;

const prev = () => {
  if (activeSlide.value === 0) {
    activeSlide.value = slideCount - 1;
    return;
  }
  activeSlide.value -= 1;
  return;
};
const next = () => {
  if (activeSlide.value === slideCount - 1) {
    activeSlide.value = 0;
    return;
  }
  activeSlide.value += 1;
  return;
};
</script>
<template>
  <div class="wrapper">
    <div class="toggle left">
      <Icon @click="prev" name="material-symbols:arrow-back-ios-new-rounded" />
    </div>

    <section class="images">
      <div class="imageContainer">
        <div v-for="(slide, index) in slides" :key="index">
          <img v-show="index === activeSlide" :src="`/img/${slide}.jpg`" />
        </div>
      </div>
      <div>
        <h4>Lorem ipsum</h4>
        <p>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consequatur
          repellendus error mollitia, iste totam quidem corporis fugit omnis
          beatae dolore reiciendis temporibus sint rem optio ullam provident
          hic? Culpa, tempore.
        </p>
      </div>
    </section>

    <div class="toggle right">
      <Icon @click="next" name="material-symbols:arrow-forward-ios-rounded" />
    </div>
  </div>
</template>
<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 2em;
  margin: 2em 0;
}
.images {
  display: flex;
  align-items: center;
  justify-content: center;
  max-width: 600px;
  gap: 3em;
}
img {
  max-width: 270px;
  rotate: 3deg;
  box-shadow: 2px 2px 5px black;
}
svg {
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 60px;
  height: 60px;
  padding: 0 10px;
  color: var(--secondary);
  background-color: rgb(0, 77, 0);
  border-radius: 50%;
  filter: drop-shadow(0px 0px 1px black);
}
h4 {
  font-size: 1.5rem;
}
p {
  font-size: 1.1rem;
}
</style>
