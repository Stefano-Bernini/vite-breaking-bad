<script>
export default {
    computed: {
        pokemon() {
            return {
                type: this.item.type1,
                catalogNumber: this.item.number,
                details: this.item.info,
                portrait: this.item.imageUrl,
                name: this.item.name,
            }
        }
    },
    props:{
        item: Object
    }
}
</script>

<template>
    <div class="pokemon text-center color-background-border">
        <img :src="pokemon.portrait" class="img-fluid mb-3" :alt="pokemon.details">
        <h4>{{ pokemon.catalogNumber }}</h4>
        <div>{{ pokemon.name }}</div>
        <div>{{ pokemon.type }}</div>
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