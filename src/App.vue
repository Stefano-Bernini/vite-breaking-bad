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
  mounted() {
    this.getPokemon()
  },
  methods: {
    getPokemon(){
      let url = store.apiUrl
      if (store.selectType !== '') {
        url += `&eq[type1]=${store.selectType}`
      }

      axios.get(url).then((response) => {
          store.pokemonList = response.data.docs
          store.loading = false
      })
    }
  }
}
</script>

<template lang="">
  <div>
    <AppHeader @typeChange="getPokemon" />
    <AppMain />
    <AppPokemonList />
  </div>
</template>

<style lang="scss">
  @use "./style/generals.scss" as *;
</style>