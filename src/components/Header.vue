<template>
    <div>
        <img src="https://images.unsplash.com/photo-1542834369-f10ebf06d3e0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2670&q=80" alt="Pizza">
        <h1>
            {{title}}
        </h1>
    </div>
</template>

<script>

export default {
    name: 'Header',
    props:{
        title: String,
    }
}

</script>

<style scoped>

div{
    text-align: center;
    border-radius: 10px;
    padding: 1em;
    background-color: rgb(50, 231, 44);
    border: 1em solid rgb(240, 10, 144);
}
img {
    max-width:65%;
    height:auto;
}

</style>
