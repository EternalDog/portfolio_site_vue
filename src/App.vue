<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <intro />
  </div>
</template>

<script>
import intro from './components/intro';

export default {
  name: 'app',
  components: {
    intro
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', 'Helvetica', 'Arial', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
