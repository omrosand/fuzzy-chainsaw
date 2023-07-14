<script setup>
const currentSlide = ref(1);
const numberOfSlides = ref(null);

const nextSlide = () => {
  if (currentSlide.value === numberOfSlides.value) {
    currentSlide.value = 1;
    return;
  }
  currentSlide.value += 1;
};
const prevSlide = () => {
  if (currentSlide.value === 1) {
    currentSlide.value = numberOfSlides.value;
    return;
  }
  currentSlide.value -= 1;
};

onMounted(() => {
  numberOfSlides.value = document.querySelectorAll(".slide").length;
});
</script>
<template>
  <div>
    <slot :currentSlide="currentSlide" />
    <div class="navigate">
      <div class="toggle left">
        <Icon
          @click="prevSlide"
          name="material-symbols:arrow-back-ios-new-rounded"
        />
      </div>
      <div class="toggle right">
        <Icon
          @click="nextSlide"
          name="material-symbols:arrow-forward-ios-rounded"
        />
      </div>
    </div>
  </div>
</template>
<style scoped>
.navigate {
  height: 100%;
  width: 100%;
  position: absolute;
  display: flex;
  justify-content: center;
  gap: 420px;
  align-items: center;
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
  filter: drop-shadow(0px 0px 7px black);
}
</style>
