<script>
import AppPokemonCard from './AppPokemonCard.vue'

import { store } from '../store.js'

export default {
    components:{
        AppPokemonCard
    },
    data(){
        return{
            store
        }
    }  
}
</script>

<template>
    <div class="container">
        <div class="row">
            <div v-for="(pokemon, index) in store.pokemonList" :key="index" class="col-6 col-lg-3">
                <AppPokemonCard :myPokemon="pokemon"/>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    
</style>