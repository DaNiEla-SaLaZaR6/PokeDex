<template>
    <div>
        <p> {{ nombre }} </p>
        <img v-if="mostrar" src="https://i.pinimg.com/736x/b0/e9/11/b0e91175f0772af0f80ab3a544587443.jpg" alt="" width="500px">
        <button @click="cambiar" >Cambiar nombre</button>

    </div>

</template>

<script>
export default{
    name: 'PruebaPage',
    data() {
        return {
            nombre:'Lizeth Daniela',
            mostrar: true
        }
    },

    methods: {
        cambiar (){
            if(this.nombre == 'Lizeth Daniela'){
                this.nombre = 'Salazar Anaya'
                this.mostrar= false
            }else{
                this.nombre= 'Lizeth Daniela'
                this.mostrar=true
            }
            
        }
    }

}
</script>

<style>
button{
  
    background-color: rgba(238, 130, 238, 0.384) ;
    border: solid 1px red;
}
button:hover{
    background-color: rgba(137, 43, 226, 0.281);
}
</style>
