<script setup></script>
<template>
  <div>
    <NuxtLink to="#"
      ><img src="/img/freia-logo.svg" alt="Freia logo"
    /></NuxtLink>
    <ul>
      <NuxtLink to="bygg-sjokoladehus">Bygg sjokoladehus</NuxtLink>
      <NuxtLink to="bli-inspirert">Bli inspirert</NuxtLink>
      <NuxtLink to="qa">Q&A</NuxtLink>
    </ul>
  </div>
</template>
<style scoped>
div {
  display: flex;
  justify-content: space-between;
  padding: 0 3em;
}
img {
  max-width: 150px;
  filter: drop-shadow(2px 2px 5px var(--bg));
}
ul {
  display: flex;
  gap: 1em;
  margin-top: 1.5em;
}
a {
  color: rgb(235, 235, 235);
  font-weight: 600;
  text-decoration: none;
  text-transform: uppercase;
  text-shadow: 2px 2px 5px var(--bg);
  letter-spacing: 0.1rem;
}
</style>
