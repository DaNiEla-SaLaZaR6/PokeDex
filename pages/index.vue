<template>
  <div class="principal">
    <div class="vacio"></div>


    <h1><b> PokeDEx</b> </h1>


    <div class="navegacion">
      <input type="text" placeholder="Buscar pokemon">
    </div>

    <div class="padre">
      <cartas v-for="i in response" :key="i.name" :nombre="i.name" :url="i.sprites.front_default"/>
     
      
    </div>



  </div>
</template>

<script>

export default {
  name: 'IndexPage',
  data() {
    return {
      response: [

      ]

    }
  },
  mounted(){
    this.getinfo()
  },
  methods:{
    async getinfo(){
      for(let i=1;i<20;i++){
      const {data}=await this.$axios.get(`pokemon/${i}`)
      this.response.push(data)
      console.log(data)
      }

    }
  }
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.principal {
  height: 100vh;
  width: 100vw;
  background-color: aquamarine;


}

.vacio {
  height: 23px;
}

h1 {
  width: 97%;
  height: 85px;
  margin: auto;
  background-color: white;
  font-size: 75px;
  text-align: center;

  border-radius: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.navegacion {
  margin-top: 20px;
  margin-left: 28px;
}

input {
  height: 38px;
  width: 280px;
  border: solid 2px rgba(128, 128, 128, 0.541);
  border-radius: 5px;

}

.padre {
  height: 80%;
  width: 100%;

  display: flex;
  flex-wrap: wrap;

}
</style>