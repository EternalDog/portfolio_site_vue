<template>
    <div id="skills_div">
        <p>--- skills page ---</p>

        <div id="skills_selector_container">
            <div class="skills_selector"> Web Development </div>
            <div class="skills_selector"> Software Development </div>
            <div class="skills_selector"> DBMS </div>
            <div class="skills_selector"> Other </div>
        </div>

        <div class="selectors" id="web_dev_selector">
            <div v-bind:key="item.name" v-for="item in $options.skills.web_dev">
                <div class="selector_item" v-bind:id="item.name" ><p>{{item.name}}</p></div>
            </div>
        </div>

        <div class="selectors" id="soft_dev_selector" > 
            <div v-bind:key="item.name" v-for="item in $options.skills.soft_dev">
                <div class="selector_item" v-bind:id=item.name ><p>{{item.name}}</p></div>
            </div>
        </div>

        <div class="selectors" id="dbms_dev_selector"> 
            <div  v-bind:key="item.name" v-for="item in $options.skills.dbms">
                <div class="selector_item" v-bind:id=item.name ><p>{{item.name}}</p></div>
            </div>
        </div>

        <div class="selectors" id="other_selector">
            <div v-bind:key="item.name" v-for="item in $options.skills.other">
                <div class="selector_item" v-bind:id=item.name ><p>{{item.name}}</p></div>
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
            
        }
    }
}


</script>
<style lang="scss" scoped>
    #skills_div {
        border-style: solid;
    }

    #skills_selector_container{
        border-style: solid;
        display: grid;  
        grid-template-columns: 1fr 1fr 1fr 1fr;
    }

    .selectors {
        display: flex;
        flex-direction: row;
        justify-content: center;
    }

    .selector_item {
        padding: 10px
    }


</style>
