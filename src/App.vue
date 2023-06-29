<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppPokemonList from './components/AppPokemonList.vue'

export default {
  components:{
    AppHeader,
    AppMain,
    AppPokemonList
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