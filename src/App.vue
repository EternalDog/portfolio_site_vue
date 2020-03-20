<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <intro class="component" />
    <br>
    <projects class="component" />
    <br>
    <skills class="component" />
    <br>
    <exp class="component" />
    <br>
    <self class="component" />
    <br>

  </div>
</template>

<script>
import intro from './components/intro';
import skills from './components/skills';
import exp from './components/exp';
import self from './components/self';
import projects from './components/projects';

export default {
  name: 'app',
  components: {
    intro, projects, skills, exp, self
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

html, body {
  margin: 0;
  //overflow: -moz-scrollbars-none; 

}

.component {
  width: 100%;
  height: 100vh;
  margin: 0;
  padding: 0;

  border-style: solid;
  border-color: red;
  
}

// // // // 

html {
  --scrollbarBG: #CFD8DC;
  --thumbBG: #90A4AE;
}
body::-webkit-scrollbar {
  width: 11px;
}
body {
  scrollbar-width: thin;
  scrollbar-color: var(--thumbBG) var(--scrollbarBG);
}
body::-webkit-scrollbar-track {
  background: var(--scrollbarBG);
}
body::-webkit-scrollbar-thumb {
  background-color: var(--thumbBG) ;
  border-radius: 6px;
  border: 3px solid var(--scrollbarBG);
}


html {
  background: lightgrey;
  overflow: hidden;
}
body {
  height: 100vh;
  background: whitesmoke;
  overflow-y: auto;
  
  margin: 0 auto;
  padding: 2rem;
  font: 100%/1.4 serif;
  border: 1px solid rgba(0, 0, 0, 0.25)
}
p {
  margin: 0 0 1.5em;
}
* {
  box-sizing: border-box;
}



</style>
