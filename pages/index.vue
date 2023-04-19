<template>
  <div>
    <loading v-if="login"/>

  <div class="principal" v-else>
   
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

    <div class="botones">

      
        <button class="boton1" @click="restar()"></button>
     
       <button class="boton2" @click="sumar()"></button>
     

    </div>



  </div>
  </div>


</template>

<script>






export default {
    name: "IndexPage",
    data() {
        return {
            response: [],
            buscar: "",
            contador: 1,
            login: true
        };
    },
    mounted() {
        this.getinfo(),
        this.encontrar()
    },
    methods: {
        async getinfo() {
            try {
                if (this.contador == 1) {
                    this.response = [];
                    for (let i = 1; i < 20; i++) {
                        const { data } = await this.$axios.get(`pokemon/${i}`);
                        this.response.push(data);
                        this.login=false;
                    
                    }
                }
                else if (this.contador == 2) {
                    this.response = [];
                    for (let i = 20; i < 40; i++) {
                        const { data } = await this.$axios.get(`pokemon/${i}`);
                        this.response.push(data);
                        this.login=false;
                  
                    }
                }
                else if (this.contador == 3) {
                    this.response = [];
                    for (let i = 40; i < 60; i++) {
                        const { data } = await this.$axios.get(`pokemon/${i}`);
                        this.response.push(data);
                        this.login=false;
          
                    }
                }
                else if (this.contador == 4) {
                    this.response = [];
                    for (let i = 60; i < 80; i++) {
                        const { data } = await this.$axios.get(`pokemon/${i}`);
                        this.response.push(data);
                        this.login=false;
                
                    }
                }
                else if (this.contador == 5) {
                    this.response = [];
                    for (let i = 80; i < 100; i++) {
                        const { data } = await this.$axios.get(`pokemon/${i}`);
                        this.response.push(data);
                        this.login=false;
                  
                    }
                }
                else if (this.contador == 6) {
                    this.response = [];
                    for (let i = 100; i < 120; i++) {
                        const { data } = await this.$axios.get(`pokemon/${i}`);
                        this.response.push(data);
                        this.login=false;
                  
                    }
                }
                else if (this.contador == 7) {
                    this.response = [];
                    for (let i = 120; i < 140; i++) {
                        const { data } = await this.$axios.get(`pokemon/${i}`);
                        this.response.push(data);
                        this.login=false;
                    
                    }
                }
                else if (this.contador == 8) {
                    this.response = [];
                    for (let i = 140; i < 160; i++) {
                        const { data } = await this.$axios.get(`pokemon/${i}`);
                        this.response.push(data);
                        this.login=false;
              
                    }
                }
                else if (this.contador == 9) {
                    this.response = [];
                    for (let i = 160; i < 180; i++) {
                        const { data } = await this.$axios.get(`pokemon/${i}`);
                        this.response.push(data);
                        this.login=false;
                
                    }
                }
                else if (this.contador == 10) {
                    this.response = [];
                    for (let i = 200; i < 220; i++) {
                        const { data } = await this.$axios.get(`pokemon/${i}`);
                        this.response.push(data);
                        this.login=false;

                    }
                }
                else if (this.contador == 11) {
                    this.response = [];
                    for (let i = 220; i < 240; i++) {
                        const { data } = await this.$axios.get(`pokemon/${i}`);
                        this.response.push(data);
                        this.login=false;
       
                    }
                }
            }
            catch (error) {
            }
        },
        encontrar() {
            for (let i = 0; i < this.response.length; i++) {
                if (this.response[i].name == this.buscar) {
                    this.$router.push(`/${this.buscar}`);
                }
            }
        },
        sumar() {
            this.contador++;
            this.getinfo();
            this.response=[]
        },
        restar() {
            this.contador--;
            this.getinfo();
            this.response=[]
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
.botones{
  height: 120px;
  width: 320px;

  display: flex;
  justify-content: center;
  align-items: center;
  margin: auto;
  gap: 20px;
}
.boton1{
  height: 60px;
  width: 150px;
  border: solid 2px white;
  background-color: rgb(33, 158, 183);
  border-radius: 15px;
  background-image: url(https://cdn-icons-png.flaticon.com/512/60/60577.png);
  background-position: center;
  background-repeat: no-repeat;
  background-size: contain;
}
.boton2{
  height: 60px;
  width: 150px;
  border: solid 2px white;
  background-color: rgb(33, 158, 183);
  border-radius: 15px;
  background-image: url(https://cdn-icons-png.flaticon.com/512/60/60546.png);
  background-position: center;
  background-repeat: no-repeat;
  background-size: contain;
}
.boton1:hover{
  background-color: rgba(255, 255, 255, 0.801);
  border: solid 2px rgb(20, 185, 235);
}
.boton2:hover{
  background-color: rgba(255, 255, 255, 0.801);
  border: solid 2px rgb(20, 185, 235);
}
</style>