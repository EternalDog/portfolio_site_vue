<template>
  <div id="intro_div">
    <p>--- intro page ---</p>

    <img alt="There should be a logo here" id="logo" src="../assets/dog_icons/placeholder_logo.jpg">

    <h2>Insert name here</h2>
    <h3>insert subtitle here</h3>


  </div>
</template>
<script>
import project_list from '../data/projects.json';

export default {
    name: "intro",
    projects: project_list,
    data(){
      return {
        current_selection: ""
      }
    },
    methods: { 
      test: function() {
        console.log(projects);
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

</style>

