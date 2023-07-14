<script setup></script>
<template>
  <main>
    <div class="wrapper">
      <Header />
      <div class="buttons">
        <Button path="bygg-sjokoladehus">Bygg sjokoladehus</Button>
        <Button path="bli-inspirert">Bli inspirert</Button>
      </div>
      <Info />
    </div>
    <Build />
    <Inspired />
    <Footer />
  </main>
</template>

<style scoped>
.wrapper {
  position: relative;
}
.buttons {
  position: absolute;
  display: flex;
  justify-content: center;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  gap: 8em;
}
</style>
