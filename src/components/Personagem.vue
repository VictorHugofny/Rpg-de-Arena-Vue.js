<template>
<div >
  <div v-show = "criar == false" > 
  <div class="field">
  <label class="label">Nome do personagem</label>
  
  <div class="control">
    <input class="input" v-model = "nome" type="text" placeholder="Text input">
  </div>
</div>

<div class="field">
  <label class="label">Raça</label>
  <div class="control">
    <div class="select">
      <select v-model = "raca">
        <option>Humano</option>
        <option>Elfo</option>
        <option>Ogro</option>
      </select>
    </div>
  </div>
</div>

<div class="field">
  <label class="label">Arma</label>
  <div class="control">
    <div class="select">
      <select  v-model = "arma">
        <option>Katana</option>
        <option>Machado</option>
      </select>
    </div>
  </div>
</div>
<div class="field">
  <div class="control">
    <button class="button is-link" @click="criarPersonagem">Criar Personagem</button>
  </div>
</div>



</div>

<div v-show = "criar == true" >
<div class="columns" >
  <div class="column is-half">
    <div class="card">
  <div class="card-image">
    <figure class="image is-128x128">
      <img v-if = 'raca == "Humano"' src="../assets/humano.png" alt="Placeholder image" height="50px">
      <img v-if = 'raca == "Elfo"' src="../assets/elfo.png" alt="Placeholder image" height="50px">
      <img v-if = 'raca == "Ogro"' src="../assets/ogro.png" alt="Placeholder image" height="50px">
    </figure>
    
  </div>
    <figure class="image is-64x64 ">
      <img v-if = 'arma == "Katana"' src="../assets/katana.png" alt="Placeholder image" height="50px">
      <img v-if = 'arma == "Machado"' src="../assets/machado.png" alt="Placeholder image" height="50px">
    </figure>
  <div class="card-content">
    <div class="media">
      
      <div class="media-content">
        <p class="title is-4">Nome: {{nome}} </p>
        <p class="subtitle is-5">Raça: {{raca}}</p>
      </div>
    </div>

    <div class="content">
      <h3> Arma Equipada: {{arma}}</h3>
      <h3> Vida: {{racas[0].vidaMax}} </h3>
    </div>
  </div>
</div>
  </div>

  <div class="column is-half">
    <div class="card ">
  <div class="card-image ">
    <figure class="image is-128x128 ">
      <img src="https://i.pinimg.com/originals/57/12/fc/5712fc208336b5fc4977bb007f143413.jpg" alt="Placeholder image" height="50px">
    </figure>
  </div>

  <div class="card-content">
    <div class="media">
      
      <div class="media-content">
        <p class="title is-4">Nome: Inimigo</p>
        <p class="subtitle is-6">Raça: Desconhecida</p>
      </div>
    </div>

    <div class="content">
      <h3> Vida: {{racas[0].vidaMax}}</h3>
    </div>
  </div>
</div>
  </div>
  </div>
    <button class="button is-dark" @click = 'lutar'>Bater</button>
    <button class="button is-link" @click ='curar'> Usar Cura</button>

  </div>
</div>
</template>

<script>



export default {
    data(){
      return{
        criar : false,
        racas : [
         {
        nome: 'Humano',
        vidaMax : 1000,
        foto: 'img/humano.png',
        forca:20,
        destreza:40,
        inteligencia:30
    },
     {
        nome: 'Elfo',
        vidaMax : 1000,
        foto: 'img/elfo.png',
        forca:10,
        destreza:60,
        inteligencia:50
    },
    {
        nome: 'Ogro',
        foto: 'img/ogro.png',
        vidaMax : 1000,
        forca:80,
        destreza:40,
        inteligencia:30
    }   
        ],
    armas : [
    {
        nome: 'Katana',
        dano:100,
        escala: 'destreza'
    },
    {
        nome: 'Machado',
        dano:50,
        escala: 'forca'
    }
],
      }
    },

    props:{
        nome: String,
        raca: String,
        arma: String,
},
methods:{
  criarPersonagem: function(){
    this.criar = true
  },
  lutar: function(){
    console.log("lutando")
    alert("EM DESENVOLVIMENTO")
  },
  curar: function(){
    console.log("lutando")
    alert("EM DESENVOLVIMENTO")
  }
}

}

</script>

<style>

.control{
    margin-left: 20%;
    margin-right: 20%;
}
.info{
    color: aqua;
    background: rgba(0, 0, 0, 0.158);
}

</style>