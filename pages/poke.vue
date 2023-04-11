<template>

    <div class="principal">
        <div class="vacio"></div>

        
        <h1><b> PokeDEx</b> </h1>
        

        <div class="navegacion">
            <input type="text" placeholder="Buscar pokemon">
        </div>

        <div class="tarjeta">
            <div class="imag"><img src="https://assets.pokemon.com/assets/cms2/img/pokedex/full/007.png" alt=""></div>
            <button>
                <p> <b>Squirtle</b> </p>
            </button>
         
            
        </div>

    </div>
 

</template>

<style>
*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

.principal{
    height: 100vh;
    width: 100%;
    background-color: aquamarine;
   

}
.vacio{
    height: 23px;
}  

h1{
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
.navegacion{
    margin-top: 20px;
    margin-left: 28px;
}
input{
    height: 38px;
    width: 280px;
    border: solid 2px rgba(128, 128, 128, 0.541);
    border-radius: 5px;

}

.tarjeta{
    height: 330px;
    width: 280px;
    margin-left: 28px;
    margin-top: 20px;
    border: solid 5px white;
    border-radius: 5px;
    background-color: red;
    box-shadow: 4px 5px 4px 5px rgba(0, 0, 0, 0.466);
}
.tarjeta p{
    color: white;
    text-align: center;
    font-size: 25px;
}
button{
    height: 40px;
    width: 100px;
    margin-left: 80px;
}
button p:hover{
    color: rgb(43, 128, 202);
  
}
</style>


