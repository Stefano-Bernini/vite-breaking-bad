<script>
export default {
    
}
</script>

<template>
    <div class="loader-wrapper">
        <div class="text">Pokedex</div>
        <div class="loader"></div>
    </div>
</template>

<style lang="scss" scoped>
    .loader-wrapper{
        position: fixed;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
        background-color: white;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;

        .text{
            font-size: 20px;
            font-weight: 700;
            text-transform: uppercase;
            margin-bottom: 2rem;
        }
    }

    .loader {
        border: 16px solid #f3f3f3;
        border-radius: 50%;
        border-top: 16px solid #3498db;
        width: 120px;
        height: 120px;
        -webkit-animation: spin 2s linear infinite; /* Safari */
        animation: spin 2s linear infinite;
    }

    /* Safari */
    @-webkit-keyframes spin {
        0% { -webkit-transform: rotate(0deg); }
        100% { -webkit-transform: rotate(360deg); }
    }

    @keyframes spin {
        0% { transform: rotate(0deg); }
        100% { transform: rotate(360deg); }
    }
</style>