<template>

  <div class="principal">
    <div class="vacio"></div>

    <div class="titulo">
     
      <h1><b> PokeDEx</b> </h1>
    </div>
 


    <div class="navegacion">
      <form action="" @submit.prevent="encontrar()">
        <input type="text" placeholder="Buscar pokemon" v-model="buscar">
      </form>
  
    </div>

    <div class="padre">
      <cartas v-for="i in response" :key="i.name" :nombre="i.name" :url="i.sprites.other.dream_world.front_default"/>
     
      
    </div>



  </div>
</template>

<script>



export default {
    name: "IndexPage",
    data() {
        return {
            response: [],
            buscar: ""
        };
    },
    mounted() {
        this.getinfo(),
        this.encontrar()
    },
    methods: {
        async getinfo() {
            for (let i = 1; i < 15; i++) {
                const { data } = await this.$axios.get(`pokemon/${i}`);
                this.response.push(data);
                console.log(data);
            }
        },
        encontrar(){
        for (let i=0; i<this.response.length;i++){
          if(this.response[i].name==this.buscar){
            this.$router.push(`/${this.buscar}`)
          }
        }
      }

    },
   
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.principal {
  height: auto;
  width: 100vw;
  background-image: url('https://img.freepik.com/vector-premium/nubes-pixeles-ilustracion-fondo-retro-8-bits-cielo-azul-nube-aerea-pixel-art_102902-1365.jpg');
  background-position: center;
  background-size: cover;



}


.vacio {
  height: 23px;
}
.titulo{
  width: 90%;
  height:95px ;

  border-radius: 20px;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 3px 3px 3px 4px rgba(13, 13, 13, 0.501);


}


h1 {
  width: 99%;
  height: 83px;
  margin: auto;
  background-color: white;
  font-size: 75px;
  text-align: center;
  border-radius: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  color:  rgba(20, 185, 235, 0.559);
  
}
.navegacion {
  margin-top: 20px;
  margin-left: 28px;
}

input {
  height: 38px;
  width: 280px;
  border: solid 3px rgba(20, 185, 235, 0.559);
  border-radius: 5px;
  box-shadow: 3px 3px 3px 4px rgba(13, 13, 13, 0.501);

}

.padre {
  height: 80%;
  width: 100%;

  display: flex;
  flex-wrap: wrap;

}
</style>