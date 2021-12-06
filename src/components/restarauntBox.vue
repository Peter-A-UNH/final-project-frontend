<template>
    <div>
       {{pizzas}}
    </div>
    <div class="restarauntBox">
        <div v-for="pizza in pizzas" :key="pizza.id" >
            <Pizza :pizza="pizza"/>
        </div>
    </div>

</template>

<script>

import Pizza from "./Pizza.vue"

export default {
    name: 'restarauntBox',
    components:{
        Pizza
    },
    props:{
        pizzas: Array
    }

}

</script>

<style scoped>

div{
    text-align: center;
}
.restarauntBox{

    background-color: cadetblue;
    padding: 1em;
    color: darkblue;

}


</style>