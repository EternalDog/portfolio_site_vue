<template>
    <div id="projects_div">

    <div id="card"> 
      <div id="project_box">
        <h2 id="project_name"> dog dog dog </h2>
        <p id="project_desc" > dog dog dog dog </p>
        <a id="project_link" href="https://github.com/EternalDog/fyp">Repository link</a> <br>
        <img alt="There should be an image here" id="project_picture" :src="'img/' + img" > 
        <!-- <img alt="There should be an image here" id="project_picture" :src="getImage(obj.img)" > -->
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
            
            console.log(this.current_selection);
            document.getElementById('project_name').innerHTML = dog.name;
            document.getElementById('project_desc').innerHTML = dog.desc;
            document.getElementById('project_link').href = dog.link;

            this.img = dog.img;

            //document.getElementById('project_picture').src = "../assets/static/" + dog.img;

            // document.getElementById('desc2').innerHTML = dog.desc2;
      },
      test: function() {
        console.log(projects);
      },
      getImage(path) {
        return require(path)
      }

    }

    
}
</script>
<style lang="scss" scoped>
  #projects_div {
    border-style: solid;
  }
  
  #card {
    display: flex;
    flex-direction: row;
  }

  .flex_container_outer {
    display: flex;
    flex-direction: row;
    border-style: solid;
  }

  #project_box {
    border-style: solid;
    border-color: red;
    width: 60%;
  }

  #project_selectors {
    //display: flex;
    //flex-direction: column;
    //border-style: solid;
    width:40%;
    border-style: solid;
    border-color: blue;
  }

  .projects_list_item {
    color:red;
    border-style: solid;
    border-color: green;
    border-radius: 10px;
  }

</style>