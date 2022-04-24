<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Search @search="search" msg=""/>
</template>

<script>
import Search from './components/Search.vue'
import axios from 'axios'
export default {
  name: 'App',
  components: {
    Search
  },
methods:{
  search(text){
    axios.get("http://localhost:5000").then(data =>{
      console.log(data);
    })
   console.log(text)
   
  }
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
