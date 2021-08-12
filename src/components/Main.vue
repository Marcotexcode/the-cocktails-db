
<template>

    <div class="container">

        <div class="card-cocktail" v-for="(elementi, index) in listCocktails" :key="index">

            <img class="card--image" :src="elementi.strDrinkThumb" :alt="elementi.name">
           
            <h2>{{elementi.strDrink}}</h2>

        </div>

    </div>

</template>


<script>


export default {

    name: 'Main',  


    props: {

        listCocktails: Array,

    },

}

</script>


<style scoped lang= "scss">

    .container {
        display: flex;
        flex-wrap: wrap;
        padding: 20px;
        justify-content: space-between;

        .card-cocktail {
            padding: 20px;
            text-transform: uppercase;
            text-align: center;
            width: 200px;
            height: 250px;
            margin: 10px;
            box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;

            .card--image {
                width: 100%;
            }
        }
    }

</style>