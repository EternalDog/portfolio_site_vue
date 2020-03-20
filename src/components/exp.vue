<template>
    <div id="exp_div">
        exp div
 
    </div>
</template>
<script>
import exp from '../data/exp.json'
export default {
    name: "exp",
    exp_data: exp,
    
}
</script>
<style lang="scss" scoped>
    #exp_div {
        border-style: solid;
    }
</style>