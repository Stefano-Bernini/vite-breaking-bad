<script>
export default {
    props:{
        myPokemon: Object
    }
}
</script>

<template>
    <div class="pokemon text-center color-background-border">
        <img :src="myPokemon.imageUrl" class="img-fluid mb-3" :alt="myPokemon.info">
        <h4>{{ myPokemon.number }}</h4>
        <div>{{ myPokemon.name }}</div>
        <div>{{ myPokemon.type1 }}</div>
    </div>
</template>

<style lang="scss" scoped>
    h4{
        text-transform: capitalize;

        &::after{
            content: '';
            display: block;
            width: 40px;
            height: 1px;
            margin: 1rem auto;
        }
    }

    .pokemon{
        margin-bottom: 4rem;
    }

    img{
        height: 250px;
        width: 250px;
        border-radius: 50%;
    }

    .color-background-border{
        background-color: yellow;
        border-radius: 20px;
    }
</style>