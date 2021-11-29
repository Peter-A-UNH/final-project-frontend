<template>
    <div>
        {{pizzas}}
    </div>
    <div class="restarauntBox">
        <div v-for="pizza in pizzas" :key="pizza.id" >
            <pizza :pizza="pizza"/>
        </div>

       
    </div>

</template>

<script>

import pizza from './pizza.vue'

export default {
    name: 'restarauntBox',
    components:{
        pizza
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