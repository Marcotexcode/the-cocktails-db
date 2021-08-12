
<template>

    <div class="container">


        <img class="container--logo" src="@/assets/img/logo.png" alt="">

    </div>

</template>


<script>

    export default {

        name: 'Header',

        components: {


        },

    }

</script>


<style scoped lang= "scss">

    .container {
        text-align: center;
        width: 100%;
        padding: 10px;
        background-color: red;

        .container--logo {
            width: 15%;
            
        }

    }

</style>