<template>
    <div id="exp_div">

        <h1>Experience and Education</h1>
        <br>

        <ul>
            <li v-bind:key="item.name" v-for="item in $options.exp">
                <h3 id="exp_name">Title: {{item.name}}</h3>
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
    }
}



</script>
<style lang="scss" scoped>
    #exp_div {
        border-style: solid;
    }

    h1 {      
        color: white;
    }

    ul {
        margin: 0px 20vw 0px 20vw;
        color: white;
        list-style-type:none;

    }
    li {
        background-color: rgba(0, 0, 0, 0.3);
        padding: 5px 15px 5px 15px;
    }

</style>