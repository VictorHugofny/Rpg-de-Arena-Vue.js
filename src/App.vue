<template>
  <div id="app">
   <a href="https://github.com/VictorHugofny">
   <button  class="button is-small is-black" id ="logo">
    <span class="icon ">
     <img src="https://raphaelbrodrigues.github.io/images/git.png" alt="" srcset="">
    </span>
    <span>Victorhugofny</span>
  </button></a>
  <h1 class = "title is-4"> RPG DE ARENA COM VUE.JS </h1>
  <Personagem/>
  </div>
</template>

<script>
import Personagem from './components/Personagem.vue'

export default {
  name: 'App',
  components: {
    Personagem,
    
  },
  data(){
    return{
      nomePersonagem: "",
      nomeRaca: "",
      nomeArma: ""
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
  margin-top: 0px;
}
#logo{
  margin: 2%;
  width: 150px;
  height: 30px;
}

</style>
