<template>
  <div id="canvas">
    <div id="deep-space" />
    <div id="menu">
      <h1 id="game-title">GALAXY RAIDERS</h1>
      <button><router-link class="menu-button" to="/game">Iniciar partida</router-link></button>
      <button><router-link class="menu-button" to="/leaderboard">Visualizar placar</router-link></button>
      <!-- Implementamos o encerramento do jogo como o redirecionamento para uma página em branco,
      pois métodos de fechar abas da WEB foram descontinuados por razões de segurança -->
      <button><router-link class="menu-button" to="/exit">Fechar jogo</router-link></button>
    </div>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Russo+One&display=swap');

#canvas {
  height: calc(100vh - 4rem);
  width: calc(100vw - 4rem);

  padding: 2rem;

  background-color: #36bbf5;
  overflow: hidden;

  position: relative;

  display: flex;
  justify-content: center;
  align-items: center;
}

#deep-space {
  height: calc(100% - 4rem);
  width: calc(100% - 4rem);

  background-image: url("~/assets/space.png");
  background-origin: content-box;
  animation: slide 3s linear infinite;

  position: absolute;
  z-index: 0;
}

#menu {
  height: calc(100% - 4rem);
  width: calc(100% - 4rem);
  
  color: orange;
  font-family: 'Russo One', sans-serif;
  font-size: large;

  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

#game-title {
  color: #36bbf5;
}

.menu-button {
  background-color: black;
  color: orange;
  font-family: 'Russo One', sans-serif;
  font-size: large;
  text-decoration: none;
}
</style>