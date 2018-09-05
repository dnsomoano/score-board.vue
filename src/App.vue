<template>
  <div id="app">
    <h1>This is a Scoreboard</h1>
    <section class="team-container">
    <ScoreCounter />
    <ScoreCounter />
  </section>
  </div>
</template>

<script>
import ScoreCounter from './components/ScoreCounter.vue'

export default {
  name: 'app',
  components: {
    ScoreCounter
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.team-container {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: flex-start;
}
</style>
