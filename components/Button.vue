<script setup>
const { path } = defineProps(["path"]);
</script>
<template>
  <div>
    <NuxtLink :to="path">
      <slot />
    </NuxtLink>
  </div>
</template>
<style scoped>
div {
  display: flex;
  background-color: var(--btn);
  min-width: 220px;
  height: 60px;
  border-radius: 40px;
  box-shadow: 0px 2px 10px var(--primary);
}
a {
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: var(--font);
  color: var(--textLight);
  font-weight: 600;
  width: 100%;
  height: 100%;
  text-transform: uppercase;
  text-decoration: none;
  text-align: center;
}
</style>
