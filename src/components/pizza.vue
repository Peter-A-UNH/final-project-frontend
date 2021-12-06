<template>
    <div>
        <h2>{{pizza.name}}</h2>
        <h4>{{pizza.address}} {{pizza.city}}, {{pizza.state}} {{pizza.zip}}</h4>
        <h4>Phone: {{pizza.phone}}</h4>
    </div>
</template>

<script>
export default{
    name: 'Pizza',
    props:{
        pizza: Array
    }
}
</script>

<style scoped>

div{
    background-color: #0baf27;
    color: black;
    padding: 1em;

}

</style>
