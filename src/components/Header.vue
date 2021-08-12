
<template>

    <div class="container">

        <img class="container--logo" src="@/assets/img/logo.png" alt="">

    </div>

</template>


<script>

    export default {

        name: 'Header',

    }

</script>


<style scoped lang="scss">

    @import '@/style/variabili.scss';

    .container {
        text-align: center;
        width: 100%;
        padding: 30px;
        background-color: $Carminio;

        .container--logo {
            width: 25%;
                
        }

    }

</style>