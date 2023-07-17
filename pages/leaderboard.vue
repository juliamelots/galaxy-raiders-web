<template>
  <div id="canvas">
    <div id="deep-space" />
    <div id="board">
      <h1 id="game-title">GALAXY RAIDERS</h1>
      <h1 id="board-title">Leaderboard</h1>
      <table id="board-data">
        <thead>
          <tr>
            <th>Date & time</th>
            <th>Destroyed asteroids</th>
            <th>Score</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="data in board" :key="data.dateTime">
            <td>{{ data.dateTime }}</td>
            <td>{{ data.destroyedAsteroids }}</td>
            <td>{{ data.finalScore }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
import JSON from '~/assets/Leaderboard.json'
export default{
    data(){
        return{
            board: JSON
        }
    }
}
</script>

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

#board {
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
</style>
