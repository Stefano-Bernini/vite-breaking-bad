<script>
import axios from 'axios'
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppPokemonList from './components/AppPokemonList.vue'

import { store } from './store.js'

export default {
  components:{
    AppHeader,
    AppMain,
    AppPokemonList
  },
  data(){
      return{
          store,
      }
  },
  mounted(){
      axios.get(store.apiUrl).then((response) => {
          store.pokemonList = response.data.docs
          store.loading = false
      })
  }
}
</script>

<template lang="">
  <div>
    <AppHeader />
    <AppMain />
    <AppPokemonList />
  </div>
</template>

<style lang="scss">
  @use "./style/generals.scss" as *;
</style>