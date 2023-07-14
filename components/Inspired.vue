<template>
  <div>
    <div class="card">
      <h2>Bli inspirert</h2>
      <Carousel2 />
      <Button path="bli-inspirert">Bli inspirert</Button>
    </div>
  </div>
</template>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 2em;
  background-color: #e1e7ea;
  color: var(--textDark);
  padding: 2em 0;
}
h2 {
  font-size: 2rem;
  text-transform: uppercase;
  font-weight: 900;
}
</style>
