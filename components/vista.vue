<template>
    <div class="principall">

        <div class="vacio"></div>

        <h2 class="h1v"><b>{{ nombre }} </b></h2>

        <div class="parte2">

            <div class="img">
                <img :src="url" alt="">
            </div>

            <div class="habilidades">
                <div class="stats">
                    <h2 class="hh"><b> Stats:</b></h2>
                    <p v-for="i in response.stats" :key="i.stat.name"><b> {{ i.stat.name }}: {{ i.base_stat }}</b> </p>

                </div>

                <div class="abilities">
                    <h2 class="hh"><b>Abilities:</b>
                    </h2>
                    <p v-for="i in response.abilities" :key="i.ability.name"><b> {{ i.ability.name }}: </b> </p>
                    <!-- <li>torrent</li>
                        <li>rain-dish</li> -->

                </div>
            </div>
        </div>

        <div class="parte3">
            <h2 class="h1v"><b> Pictures</b></h2>
        </div>

        <div class="parte4">
            <img :src="imagenes.back_default" alt="" class="image">
            <img :src="imagenes.front_default" alt="" class="image">
            <img :src="imagenes.back_shiny" alt="" class="image">
            <img :src="imagenes.front_shiny" alt="" class="image">

        </div>



    </div>
</template>

<script>
export default {

    name: 'VistaComponent',

    data() {
        return {
            response: [],
            nombre: this.$route.params.habi,
            url: '',
            imagenes: {},

        }
    },

    mounted() {
        console.log(this.$route)
        this.getinfo()
    },
    methods: {
        async getinfo() {
            const { data } = await this.$axios.get(`pokemon/${this.$route.params.habi}`)
            this.response = (data)
            this.url = this.response.sprites.other.dream_world.front_default
            this.imagenes = this.response.sprites
            console.log(this.response)
        }
    },
}
</script>



<style>
.principall {
    height: 100vh;
    width: 100vw;
    background-image: url(https://images.wikidexcdn.net/mwuploads/esssbwiki/thumb/2/2c/latest/20180819065319/Estadio_Pok%C3%A9mon_2_SSBU.jpg/1200px-Estadio_Pok%C3%A9mon_2_SSBU.jpg);
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;

}

.vacio {
    height: 33px;
}

.h1v {
    width: 50%;
    height: 48px;
    -webkit-text-stroke-width: 1px 2px;
    margin: auto;
    color: white;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 50px;

}

.parte2 {
    width: 100%;
    height: 40%;
    display: flex;

}

.parte3 {
    width: auto;
    height: auto;
    display: flex;
}

.parte4 {
    height: auto;
    width: auto;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: auto;

}

.img {
    width: 20%;
    height: 70%;
    margin: auto;
    box-shadow: 3px 3px 3px 4px rgba(13, 13, 13, 0.792);
}

.image {
    height: 20%;
    width: 20%;
    display: flex;

}

.habilidades {
    height: 83%;
    width: 70%;
    border-radius: 22px;
    border: solid 1px black;
    display: flex;
    margin: auto;
    box-shadow: 3px 3px 3px 4px rgba(228, 222, 222, 0.792);
    background-color: rgba(128, 128, 128, 0.346);
    animation: fond 3s linear infinite;
}

@keyframes fond {
    10% {
        background-color: rgba(128, 128, 128, 0.333);
    }

    50% {
        background-color: rgba(255, 255, 255, 0.279);
    }

}

.hh {
    font-size: 40px;
    color: rgb(240, 25, 25);
}

.stats {
    height: 90%;
    width: 40%;
    margin: auto;
    font-size: 1.3rem;
    color: white;

}

.abilities {
    height: 90%;
    width: 40%;
    margin: auto;
    font-size: 1.3rem;
    color: white;


}</style>