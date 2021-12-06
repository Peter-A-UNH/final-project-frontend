<template>
  <div class="container">

    <Header restaurantName="Pizza Places in CT" restaurantCity="City"/>

    <RestarauntBox :pizzas="pizzas" />
    

  </div>
</template>

<script>
import Header from './components/Header.vue'
import RestarauntBox from './components/RestarauntBox.vue'

export default {
  name: 'App',
  components: {
    Header,
    RestarauntBox
  },
  data(){
    return {
        pizzas: {} //[]    
    }
  },

  methods:{
    //promices (also how to fetch from API)

    async fetchPizzas(){
      //const res= await fetch('https://young-dawn-31355.herokuapp.com/https://pa-final-project.herokuapp.com/api')
      const res= await fetch('https://pa-final-project.herokuapp.com/api')
      //const res= await fetch('http://localhost:5555/pizza')
      const data= await res.json()
      console.log(data)
      console.log(typeof(data))

      return data
    }
  },
  async created(){
    this.pizzas = await this.fetchPizzas()
  }
}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Open+Sans&display=swap');

*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Open Sans', sans-serif;
}

.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.4em solid blueviolet;
  padding: 20px;
  border-radius: 10px;
}

div{
  margin-bottom: 0.3em;
}

/*
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
