<template>
  <div id="intro_div">
    <p>--- intro page ---</p>

    <img alt="There should be a logo here" id="logo" src="../assets/dog_icons/placeholder_logo.jpg">

    <h2>Insert name here</h2>
    <h3>insert subtitle here</h3>

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
    name: "intro",
    projects: project_list,
    data(){
      return {
        current_selection: {"img": "dog1.png"},
        img: "dog1.png",

      }
    },
    methods: { 
      test: function() {
        console.log(projects);
      },
            project_select: function (dog) {
            
            this.current_selection = dog;
            
            console.log(this.current_selection);
            document.getElementById('project_name').innerHTML = dog.name;
            document.getElementById('project_desc').innerHTML = dog.desc;
            document.getElementById('project_link').href = dog.link;

            this.img = dog.img;

            //document.getElementById('project_picture').src = "../assets/static/" + dog.img;

            // document.getElementById('desc2').innerHTML = dog.desc2;
      }


    }
}


</script>
<style lang="scss" scoped>
  #intro_div {
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

  #selectors {
    //display: flex;
    //flex-direction: column;
    //border-style: solid;
    border-style: solid;
    border-color: blue;
  }

  .desc {
    border-style: solid;
    border-color: red;
  }

  .projects_list_item {
    color:red;
  }

  #projects_div {
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

