<script>
import axios from 'axios'
export default {
    data(){
        return{
            pokemonList: []
        }
    },
    mounted(){
        axios.get('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?eq[type1]=Electric&sort[number]=desc').then((response) => {
            this.pokemonList = response.data.docs
        })
    }
}
</script>

<template>
    <div class="container">
        <div class="row">
            <div v-for="(pokemon, index) in pokemonList" :key="index" class="col-6 col-md-4">
                {{ pokemon.name }}
            </div>
        </div>
    </div>
</template>

<style lang="">
    
</style>