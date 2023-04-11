<template>
    <div class="principal">

        <div class="vacio"></div>

        <h1 class="h1v"><b>Squirtle</b></h1>

        <div class="parte2">

            <div class="img">
                <img src="https://assets.pokemon.com/assets/cms2/img/pokedex/full/007.png" alt="">
            </div>

            <div class="habilidades">
                <div class="stats">
                    <h1 class="hh"><b> Stats</b></h1>
                    <p><b> hp:</b> 44</p>
                    <p><b>attack:</b>  48</p>
                    <p><b>defense:</b>  65</p>
                    <p><b>special-attack:</b>  50</p>
                    <p><b>special-defense:</b>  64</p>
                    <p><b>special-defense:</b>43</p>
                </div>

                <div class="abilities">
                    <h1 class="hh"><b>Abilities</b>
                        </h1>
                    
                        <li>torrent</li>
                        <li>rain-dish</li>
                        
                        
                    

                   
                </div>
            </div>
        </div>

        <div class="parte3">
            <h1 class="hhh"> Pictures</h1>


        </div>
    </div>
</template>


<style>
.principal{
    height: 100vh;
    width: 100%;
    background-color: rgb(153, 246, 228);
}
.vacio{
    height: 33px;
} 
.h1v{
    width: 50%;
    height: 50px;
    margin: auto;

    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 50px;
}
.parte2{
    width: 100%;
    height: 40%;

    margin-top: 20px;
    display: flex;
 
}
.img{
    width: 15%;
    height: 65%;
    margin: auto;

}
.habilidades{
    height: 80%;
    width: 70%;
    border-radius: 20px;
    border: solid 3px;
    display: flex;
    margin: auto;
    border-style: dashed;

}
.hh{
    font-size: 40px;
}
.stats{
    height: 90%;
    width: 40%;

    margin: auto;
    font-size: 1.3rem;
}
.abilities{
    height: 90%;
    width: 40%;

    margin: auto;
    font-size: 1.3rem;

}
</style>