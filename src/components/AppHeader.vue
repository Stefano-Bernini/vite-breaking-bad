<script>
export default {
    
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
                <select class="form-select" aria-label="Default select example">
                    <option selected>Open this select menu</option>
                    <option value="1">One</option>
                    <option value="2">Two</option>
                    <option value="3">Three</option>
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