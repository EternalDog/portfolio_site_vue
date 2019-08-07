<template>
  <div id="intro_div">
    <p>--- intro page ---</p>

    <img alt="There should be a logo here" id="logo" src="../assets/logo.jpg">

    <h2>Dominik Bahrynowski</h2>
    <h3>Software Developer | Web Developer | Volunteer</h3>


    <div class="flex_container_inner" v-bind:key="projects.name" v-for="projects in projects">
      <div class="projects_list_item" v-bind:id=projects.link ><p>{{projects.name}}</p></div>
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
    }
}
</script>
<style lang="scss" scoped>
  #intro_div {
    border-style: solid;
  }

  .flex_container_outer {
    display: flex;
    flex-direction: row;
    border-style: solid;
  }

  .flex_container_inner {
    display: flex;
    flex-direction: column;
    border-style: solid;
  }

  .projects_list_item {
    color:red;
  }

</style>

