<template>
  <div id="intro_div">
    <img alt="There should be a logo here" id="logo" src="../assets/static/normannis_regional.jpg">

    <div id="intro_text">
      
      <h1>Dominik</h1>
      <h2>Software Developer | Amateur Historian | Volunteer </h2>

      <br>
      <!-- <h3>THIS SITE IS CURRENTLY WORK IN PROGESS</h3> -->
      <p>I am a Polish Programmer and Web Developer who recently came from Ireland to England. <br>
       Last year I have finished a degree (BSc Web Development) in the Cork Institute of Technology.  <br>
       The year before that I have also worked as an intern software engineer at McAfee, which I found to be a pretty positive experience. <br>
       I am pretty passionate about programming and IT in general, and my current goal in life is to continue expanding my existing skills. <br>
       My skills in programming primarily revolve around various JavaScript technologies as well as Java, Python, PHP and others. </p>
      <br><br>

      <a :href="`${publicPath}CV.pdf`" download="Dominik's CV" class="tooltip">
        <span class="tooltiptext">My CV</span>
        <img id="pdf_icon" alt="There should be a pdf icon here" src="../assets/static/icons/PDF_file_icon.svg">
      </a>

      <a href="https://github.com/EternalDog"  class="tooltip">
        <span class="tooltiptext">Github profile</span>
        <img id="pdf_icon" alt="There should be a pdf icon here" src="../assets/static/icons/GitHub.png">
      </a>

      <a href="https://github.com/EternalDog"  class="tooltip">
        <span class="tooltiptext">Linkedin profile</span>
        <img id="pdf_icon" alt="There should be a pdf icon here" src="../assets/static/icons/linkedin.png">
      </a>

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
        publicPath: process.env.BASE_URL,
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

  #logo {
    width: 40%;
    height: auto;
    border-radius: 4px;
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

  #pdf_icon {
    height: 80px;
    widows: auto;
  }

  .tooltip {
  margin: 0px 30px;
  position: relative;
  display: inline-block;
  border-bottom: 1px dotted black; /* If you want dots under the hoverable text */
}

/* Tooltip text */
.tooltip .tooltiptext {
  visibility: hidden;
  width: 120px;
  background-color: black;
  color: #fff;
  text-align: center;
  padding: 5px 0;
  border-radius: 6px;
 
  /* Position the tooltip text - see examples below! */
  position: absolute;
  z-index: 1;
  bottom: 100%;
  left: 50%;
  margin-left: -60px;
}

/* Show the tooltip text when you mouse over the tooltip container */
.tooltip:hover .tooltiptext {
  visibility: visible;
}


</style>

