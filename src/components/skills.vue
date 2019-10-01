<template>
    <div id="skills_div">
        <p>--- skills page ---</p>

        <div id="skills_selector_top_container">
            <div class="skill_group_selector" id="web_dev_selector"> <button v-on:click="web_dev_display"> Web Development </button>  </div>
            <div class="skill_group_selector" id="soft_dev_selector"> <button v-on:click="soft_dev_display"> Software Development </button> </div>
            <div class="skill_group_selector" id="dbms_selector"> <button v-on:click="dbms_display"> DBMS </button>  </div>
            <div class="skill_group_selector" id="other_selector"> <button v-on:click="other_display"> Other </button>  </div>
        </div>

        <div id="skills_selector_bottom_container">
            <div class="selectors" id="web_dev_selector" v-show="show_web_dev" >
                <div v-bind:key="item.name" v-for="item in $options.skills.web_dev">
                    <div class="selector_item" ><button v-bind:id=item.name v-on:click="technology_select(item)">{{item.name}}</button></div>
                </div>
            </div>

            <div class="selectors" id="soft_dev_selector" v-show="show_soft_dev" > 
                <div v-bind:key="item.name" v-for="item in $options.skills.soft_dev">
                    <div class="selector_item" ><button v-bind:id=item.name v-on:click="technology_select(item)">{{item.name}}</button></div>
                </div>
            </div>

            <div class="selectors" id="dbms_dev_selector" v-show="show_dbms"> 
                <div  v-bind:key="item.name" v-for="item in $options.skills.dbms">
                    <div class="selector_item" ><button v-bind:id=item.name v-on:click="technology_select(item)">{{item.name}}</button></div>
                </div>
            </div>

            <div class="selectors" id="other_selector" v-show="show_other">
                <div v-bind:key="item.name" v-for="item in $options.skills.other">
                    <div class="selector_item" ><button v-bind:id=item.name v-on:click="technology_select(item)">{{item.name}}</button></div>
                </div>
            </div>
        </div>


    </div>
</template>
<script>
import skill_list from '../data/skill_list.json'
export default {
    name: "skills",
    skills: skill_list,
    data(){
        return {
            current_selection: "web_dev",
            show_web_dev: true,
            show_soft_dev: false,
            show_dbms: false,
            show_other: false
        }
    },
    methods: {
        web_dev_display: function (event) {
            this.current_selection = "web_dev";
            this.show_web_dev = true;
            this.show_soft_dev = false;
            this.show_dbms = false;
            this.show_other = false;
        },
        soft_dev_display: function (event) {
            this.current_selection = "soft_dev";
            this.show_web_dev = false;
            this.show_soft_dev = true;
            this.show_dbms = false;
            this.show_other = false;
        },
        dbms_display: function (event) {
            this.current_selection = "dbms";
            this.show_web_dev = false;
            this.show_soft_dev = false;
            this.show_dbms = true;
            this.show_other = false;
        },
        other_display: function (event) {
            this.current_selection = "other";
            this.show_web_dev = false;
            this.show_soft_dev = false;
            this.show_dbms = false;
            this.show_other = true;
        },
        technology_select: function (dog) {
            console.log(dog);
        }
    }
}


</script>
<style lang="scss" scoped>
    #skills_div {
        border-style: solid;
    }

    #skills_selector_top_container{
        border-style: solid;
        display: grid;  
        grid-template-columns: 1fr 1fr 1fr 1fr;
    }

    .selectors {
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .selector_item {
        padding: 10px
    }


</style>
