<template>
    <div class="princial">
        <div class="fondo">
            <div class="imagenpo"></div>
            <p class="pereee"><b>LOADING....... </b> </p>
        </div>
        
    </div >
</template>

<script>
export default{
    name: 'LoadingComponent'
}
</script>

<style>
.princial{
    height: 100vh;
    width: 100%;
    background-image: url(https://i.pinimg.com/originals/06/5e/5e/065e5e9239f7d492dc3d64e57e84d6ed.jpg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;



}
.fondo{
    height: 100%;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.572);
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;

}
.imagenpo{
    height: 30%;
    width: 20%;
    background-color: rgba(0, 0, 0, 0.438);
    background-image: url( ../img/png-clipart-pokeball-pokeball-removebg-preview.png);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
    
}
.pereee{
    font-size: 50px;
    -webkit-text-stroke-width: 3px 2px;
    color: white;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    
}

</style>