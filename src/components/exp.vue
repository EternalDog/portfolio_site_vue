<template>
    <div id="exp_div">
        exp div

        <p v-on:click="dog()">dog dog dog</p>

        <ul>
            <li v-bind:key="item.name" v-for="item in $options.exp">
                <p id="exp_name">Title: {{item.name}}</p>
                <span id="exp_date">Duration: {{item.start_date}} to {{item.end_date}} </span>
                <p id="exp_location">Location: {{item.location}}</p>
                <p id="exp_desc">{{item.desc}}</p>
                
                <!-- <span id="exp_duration">{{item.duration}}</span> -->
                <p></p>
            </li>
        </ul>

    </div>
</template>
<script>
import exp_data from '../data/exp.json'
export default {
    name: "exp",
    exp: exp_data,
    methods: {
        dog: function () {
            console.log(this.exp);
        }

    }
}



</script>
<style lang="scss" scoped>
    #exp_div {
        border-style: solid;
    }
</style>