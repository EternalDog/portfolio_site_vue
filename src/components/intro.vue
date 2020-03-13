<template>
  <div id="intro_div">
    <p>--- intro page ---</p>

    <img alt="There should be a logo here" id="logo" src="../assets/dog_icons/placeholder_logo.jpg">

    <h2>Insert name here</h2>
    <h3>insert subtitle here</h3>



    <div id="card"> 
      <div id="desc">
        <h2>dog dog dog</h2>
        <p>dog dog dog</p>
      </div>

      <div id="selectors">
        <div v-bind:key="projects.name" v-for="projects in projects">
          <div class="projects_list_item" v-bind:id=projects.name v-on:click="project_select(projects.name)" ><p>{{projects.name}}</p></div>
        </div>
      </div>

    </div>


  </div>
</template>
<script>
export default {
    name: "intro",
    data(){
      return {
        projects: [
          {
            name: "Britannia",
            link: "aaaa"
          },
          {
            name: "Dice Doge",
            link: "bbbb"
          },
          {
            name: "something here",
            link: "cccc"
          }
        ]
      }
    },
    methods: { 
      project_select: function (dog) {
            console.log(dog);
            // document.getElementById('title').innerHTML = dog.name;
            // document.getElementById('desc1').innerHTML = dog.desc;
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

</style>

