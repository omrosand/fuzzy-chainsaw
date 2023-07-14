<script setup></script>
<template>
  <div class="slide">
    <transition name="slide">
      <slot />
    </transition>
  </div>
</template>
<style scoped>
.slide-enter-active,
.slide-leave-active {
  transition: opacity 1.2s ease-in-out;
}
.slide-enter-from,
.slide-leave-to {
  opacity: 0;
}
.slide-leave-from,
.slide-enter-to {
  opacity: 1;
}
</style>
