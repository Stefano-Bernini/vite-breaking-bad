<script>
import AppPokemonCard from './AppPokemonCard.vue'
import AppLoader from './AppLoader.vue'

import { store } from '../store.js'

export default {
    components:{
        AppPokemonCard,
        AppLoader
    },
    data(){
        return{
            store
        }
    }  
}
</script>

<template>
    <div class="container color-background">
        <div class="row" v-if="store.loading === false">
            <div v-for="(pokemon, index) in store.pokemonList" :key="index" class="col-6 col-lg-3 ">
                <AppPokemonCard :item="pokemon"/>
            </div>
        </div>
        <AppLoader v-else/>
    </div>
</template>

<style lang="scss">
    .color-background{
        background-color: rgb(75,81,86);
    }
</style>