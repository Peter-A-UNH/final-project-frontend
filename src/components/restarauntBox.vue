<template>
    <div>
        <h1>
            {{restaurantName}}
        </h1>
        <h3>
            {{restaurantCity}}
        </h3>
    </div>
</template>

<script>

export default {
    name: 'restarauntBox',
    props:{
        restaurantName: String,
        restaurantCity: String
    }

}

</script>

<style scoped>

div{
    text-align: center;
}


</style>