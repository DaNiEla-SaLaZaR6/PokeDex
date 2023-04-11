<template>
    <div class="tarjeta" >
        <div class="imag"><img :src=url alt=""></div>
          <p class="nom"> <b> {{ nombre }}</b> </p>
        


    </div>
    
        
    
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
    height: 330px;
    width: 295px;
    margin-left: 30px;
    margin-top: 20px;
    border: solid 5px white;
    border-radius: 5px;
    background-color: red;
    box-shadow: 4px 5px 4px 5px rgba(0, 0, 0, 0.466);
    display: flex;
    justify-content: center;
 
    flex-direction: column;
  }
  
.tarjeta p {
    color: white;
    text-align: center;
    font-size: 25px;
}
img{
    height: 100%;
    width: 100%;
    display: flex;
    justify-content:center ;
    align-items: center;

}


  


</style>