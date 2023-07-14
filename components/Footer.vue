<script setup></script>
<template>
  <div>
    <div class="wrapper">
      <section class="links">
        <NuxtLink to="/">Hjem</NuxtLink>
        <NuxtLink to="bygg-sjokoladehus">Bygg sjokoladehus</NuxtLink>
        <NuxtLink to="bli-inspirert">Bli inspirert</NuxtLink>
        <NuxtLink to="qa">Q&A</NuxtLink>
      </section>
      <section class="socials">
        <Icon name="mdi:facebook" />
        <Icon name="mdi:twitter" />
        <Icon name="mdi:instagram" />
        <Icon name="ic:baseline-tiktok" />
      </section>
      <section class="trademark">
        <img src="/img/freia-logo-dark.png" />
        <p>&copy; 2023 - Freia skaper glede</p>
      </section>
    </div>
  </div>
</template>
<style scoped>
.wrapper {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-wrap: wrap;
  color: var(--textDark);
  padding: 2em 0;
  background-color: var(--btn);
  text-transform: uppercase;
}
img {
  max-width: 90px;
}
.socials {
  display: flex;
  gap: 0.7em;
}
svg {
  width: 45px;
  height: 45px;
}
.links {
  display: grid;
  gap: 10px;
  grid-template-columns: 1fr 1fr;
}
a {
  text-decoration: none;
  color: var(--textDark);
  font-size: 0.9rem;
  font-weight: 600;
}
.trademark {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
p {
  font-size: 0.9rem;
  font-weight: 500;
}
</style>
