<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->

    <div id="navbar">
      <div class="navbar_item" v-scroll-to="{ element: '#intro', duration: 1000 }" >Intro </div>
      <div class="navbar_item" v-scroll-to="{ element: '#projects', duration: 1000 }" >Projects </div>
      <div class="navbar_item" v-scroll-to="{ element: '#skills', duration: 1000 }">Skills </div>
      <div class="navbar_item" v-scroll-to="{ element: '#exp', duration: 1000 }">Experience </div>
      <div class="navbar_item" v-scroll-to="{ element: '#self', duration: 1000 }">About Me </div>
    </div>


    <br><br>
    <intro id="intro" class="component" />

    <projects id="projects" class="component" />

    <skills id="skills" class="component" />

    <exp id="exp" class="component" />

    <self id="self" class="component" />


  </div>
</template>

<script>
import intro from './components/intro';
import skills from './components/skills';
import exp from './components/exp';
import self from './components/self';
import projects from './components/projects';

var VueScrollTo = require('vue-scrollto');
var options = {
    container: '#container',
    easing: 'ease-in',
    offset: -60,
    force: true,
    cancelable: true,
    onStart: function(element) {
      // scrolling started
    },
    onDone: function(element) {
      // scrolling is done
    },
    onCancel: function() {
      // scrolling has been interrupted
    },
    x: false,
    y: true
}


export default {
  name: 'app',
  components: {
    intro, projects, skills, exp, self
  },
  methods: {
    goto: function(dog) {
      //alert(dog);
      //var element_to_scroll_to = document.getElementById(dog);
      //element_to_scroll_to.scrollIntoView();
      VueScrollTo.scrollTo(dog, 1000, options)
    }
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
  background: lightgrey;
  overflow: hidden;
}
body::-webkit-scrollbar {
  width: 11px;
}
body {
  height: 100vh;
  background: whitesmoke;
  overflow-y: auto;
  
  margin: 0 auto;
  
  font: 100%/1.4 serif;
  border: 1px solid rgba(0, 0, 0, 0.25);


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

p {
  margin: 0 0 1.5em;
}
* {
  box-sizing: border-box;
}

// 

#navbar {
  height: 5vh;
  width: 100%;
  position: fixed;
  border: 1px solid rgba(200, 0, 0, 1);
  display: flex;
  flex-direction: row;
  justify-content: center;
  opacity: 0.6;
  background-color: rgb(0, 0, 0);
}

#navbar:hover {
  opacity: 1;
}


.navbar_item {
  width: 20%;
  color: white;
  border: 3px solid rgba(0, 0, 0, 0.1);
  font-size: 1.4em;
}

.navbar_item:hover {
  background-color: rgb(102, 2, 2);
}

//// 

#intro {
  background-image: url("./assets/static/dog.jpg");
  background-size: cover;
}

#skills {
  background-image: url("./assets/static/dog.jpg");
  background-size: cover;
}

#exp {
    background-image: url("./assets/static/prog1.jpg");
  background-size: cover;
}

#self {
  background-image: url("./assets/static/lewes.jpg");
  background-size: cover;
}




</style>
