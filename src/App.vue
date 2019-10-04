<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <intro />
    <br>
    <skills />
    <br>
    <exp />
  </div>
</template>

<script>
import intro from './components/intro';
import skills from './components/skills';
import exp from './components/exp';
import self from './components/self';

export default {
  name: 'app',
  components: {
    intro, skills, exp, self
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
