<template>
    <div id="projects_div">
      <H1>Projects</H1>
      <div id="card"> 
        <div id="project_box">
          <h2 id="project_name"> Select a project on the right. </h2>
          <h4 id="project_stack" > </h4>
          <p id="project_desc" > </p>
          <a id="project_link" href="https://github.com/EternalDog/fyp"></a> <br>
          <img alt="There should be an image here" id="project_picture" :src="'img/' + img" > 
        </div>

        <div id="project_selectors">
          <div v-bind:key="projects.name" v-for="projects in  $options.projects">
            <div class="projects_list_item" v-bind:id=projects.name v-on:click="project_select(projects)" >
              <p>{{projects.name}}</p>
              <p>{{projects.desc_short}}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>
<script>

import project_list from '../data/projects.json';

export default {
    name: "projects",
    projects: project_list,
    data(){
      return {
        current_selection: {"img": "dog1.png"},
        img: "dog1.png",
      }
    },
    methods: { 
      project_select: function (dog) {    
        this.current_selection = dog;
        document.getElementById('project_name').innerHTML = dog.name;
        document.getElementById('project_stack').innerHTML = "Technology stack: " + dog.stack;
        document.getElementById('project_desc').innerHTML = dog.desc;
        document.getElementById('project_link').href = dog.link;
        document.getElementById('project_link').innerHTML = "Repository link";
        this.img = dog.img;
      }
    }
  
}
</script>
<style lang="scss" scoped>
  #projects_div {
    border-style: solid;
  }

  h1 {
    color: white;
  }
  
 #card {
    display: flex;
    flex-direction: row;
    opacity: 0.85;
    border-radius: 1px;
    margin-right: 5vw;
    margin-left: 7vw;
  }

  .flex_container_outer {
    display: flex;
    flex-direction: row;
    border-style: solid;
  }

  #project_box {
    border-radius: 1px;
    box-shadow: 0px 0px 5px 3px rgba(56, 0, 0, 0.5);
    width: 60%;
    height: 100%;
    padding: 40px;
    background-color: white;
    border-style: solid;
    border-color: black;
    border-width: 0.5px;
  }

  #project_box:hover {
    border-width: 1px;
    box-shadow: 0px 0px 5px 9px rgba(56, 0, 0, 0.5);
  }

  #project_selectors {
    width:40%;
  }

  .projects_list_item {
    border-style: solid;
    border-color: black;
    border-width: 0.5px;
    font-size: 1.2em;
    color:white;
    padding-top: 15px;
    margin-left: 5px;
    margin-bottom: 5px;
    border-radius: 1px;
    background-color:black;
    width: 85%;
    box-shadow: 0px 0px 5px 5px rgba(0, 0, 0, 0.5);
  }

  .projects_list_item:hover {
    border-style: solid;
    border-color: black;
    border-width: 0.5px;
    box-shadow: 0px 0px 5px 9px rgba(56, 0, 0, 0.5);
  }

  .projects_list_item:hover { 
    color: rgb(102, 2, 2);
    background-color: white;
  }

  #project_picture {
    width: 70%;
    height: 70%;
  }
</style>