<template>
  <div id="intro_div">
    <img alt="There should be a logo here" id="logo" src="../assets/dog_icons/placeholder_logo.jpg">

    <div id="intro_text">
      
      <h1>Dominik</h1>
      <h2>Software Developer | Amateur Historian | Volunteer </h2>

      <br><br><br>
      <h3>THIS SITE IS CURRENTLY WORK IN PROGESS</h3>
      <p>As such, there will be a few placeholder strings/images and the styling isnt finalised.</p>
      <br><br>
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
      project_select: function (dog) {    
        this.current_selection = dog;
        document.getElementById('project_name').innerHTML = dog.name;
        document.getElementById('project_desc').innerHTML = dog.desc;
        document.getElementById('project_link').href = dog.link;
        this.img = dog.img;
      }
    }
}


</script>
<style lang="scss" scoped>
  #intro_div {
    border-style: solid;
  }

  #intro_text {
    color: white;
    background-color: rgba($color: #220000, $alpha: 0.2);  
  }




  #intro_text {
    margin: 0px 15vw 0px 15vw;
  }
  
  #card {
    display: flex;
    flex-direction: row;
    background-color: white;
    opacity: 0.85;
    border-radius: 10px;
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
    padding: 5px;
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

