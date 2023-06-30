<script>
import { store } from '../store'

export default {
    data(){
        return{
            store,
            pokemonType:[
                'Grass',
                'Fire',
                'Water',
                'Bug',
                'Normal',
                'Dark',
                'Poison',
                'Electric'
            ]
        }
    }
    
}
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col-8 py-4 d-flex">
                <div class="buttons_big"></div>
                <div class="buttons_little red"></div>
                <div class="buttons_little yellow"></div>
                <div class="buttons_little green"></div>
            </div>
            <div class="col-4 d-flex align-items-center">
                <select class="form-select" v-model="store.selectType" @change="$emit('typeChange')">
                    <option value="" selected>Tutte le tipologie di Pokemon</option>
                    <option v-for="(type, index) in pokemonType" :key="index" :value="type"> {{ type }}</option>
                    <!-- <option value="Grass">Erba</option>
                    <option value="Fire">Fuoco</option>
                    <option value="Water">Acqua</option>
                    <option value="Bug">Coleottero</option>
                    <option value="Normal">Normale</option>
                    <option value="Dark">Buio</option>
                    <option value="Poison">Veleno</option>
                    <option value="Electric">Elettro</option> -->
                </select>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .buttons_big{
        height: 100px;
        width: 100px;
        background-color: blue;
        border-radius: 50%;
        border: 5px solid white;
    }

    .buttons_little{
        height: 50px;
        width: 50px;
        border-radius: 50%;
        border: 5px solid white;
        margin: 0 10px;
    }

    .red{
        background-color: red;
    }

    .yellow{
        background-color: yellow;
    }

    .green{
        background-color: green;
    }
</style>