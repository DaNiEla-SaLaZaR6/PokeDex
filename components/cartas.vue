<template>


  <nuxt-link :to=nombre>

    <div class="tarjeta" >
      
      <div class="imag"><img :src=url alt="" class="imaagee"></div>
        <p class="nom"> <b> {{ nombre }}</b> </p>
      


  </div>


  </nuxt-link>
  

    
        
    
</template>

<script>
export default {
  name: 'poke2',
  props: {
    nombre:{
        type: String,
        required : true
    },
    url:{
        type: String,
        required : true
    }
  }


}
</script>
<style>
.tarjeta {
    height: 450px;
    width: 330px;
    margin: 25px;
    border: solid 5px rgb(251, 244, 249);
    border-radius: 5px;
    box-shadow: 3px 3px 3px 4px rgba(32, 30, 30, 0.652);
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background-color: rgba(255, 0, 0, 0.653);
    animation: fondo 3s linear infinite;
  }
  @keyframes fondo {
    0%{
      background-color: rgba(179, 61, 38, 0.905);
    }
    10%{
      background-color: rgba(206, 112, 23, 0.819);
    }
    20%{
      background-color: rgb(234, 162, 18);
    }
    30%{
      background-color: rgb(93, 190, 20);
    }
    40%{
      background-color: rgb(24, 174, 124);
    }
    50%{
      background-color: rgb(21, 83, 198);
    }
    70%{
      background-color: rgb(76, 0, 255);
    }
    80%{
      background-color: rgb(186, 28, 192);
    }
    90%{
      background-color: rgb(205, 22, 114);
    }
    100%{
      background-color: rgb(200, 17, 60);
    }
    
  }

  
.tarjeta p {
    color: white;
    text-align: center;
    font-size: 25px;
}
img{

    height: 100%;
    width: 100%;
}

.nom{
  font-family: Georgia, 'Times New Roman', Times, serif ;

}

  


</style>