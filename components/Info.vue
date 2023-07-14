<template>
  <div>
    <div class="card">
      <h1>God Jul!</h1>
      <div class="infoContainer">
        <div class="imgContainer">
          <img class="infoImg" src="/img/choco1.jpg" alt="info image" />
        </div>
        <div class="textContainer">
          <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Consequuntur architecto labore deserunt laudantium quibusdam neque
            magni, natus explicabo vel ex nostrum.
          </p>
          <img class="logo" src="/img/freia-logo.svg" alt="logo" />
        </div>
      </div>
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
  height: 35em;
}
.textContainer,
.imgContainer {
  display: flex;
  flex-direction: column;
  max-width: 400px;
}
.infoImg {
  background-size: cover;
  height: auto;
  max-width: 100%;
  rotate: 3deg;
  box-shadow: -8px 8px 5px var(--primary);
}
.infoContainer {
  display: flex;
  align-items: center;
  gap: 5em;
}
.logo {
  max-width: 120px;
  align-self: flex-end;
}
h1 {
  font-size: 3.5rem;
  text-transform: uppercase;
  font-weight: 900;
}
p {
  font-size: 1.2rem;
}
</style>
