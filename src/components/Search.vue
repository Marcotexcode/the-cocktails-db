
<template>

    <div class="container">

        <form class="container--search" action="">

            <input class="ricerca" type="text" placeholder="ricerca" v-model.trim="inputText">

            <button class="btn " type="submit" @click.prevent="$emit('searchCockt', inputText)" @click="reset">Invio</button>

        </form>

    </div>

</template>


<script>

export default {

    name: 'Search',

    data() {

        return {

            inputText: ''

        }

    },

    methods: {
        
        reset() {

            this.inputText = ''
            
        }

    }

}

</script>


<style scoped lang= "scss">

    .container {
        background-color: red;
        text-align: center;
        padding: 20px;

        .container--search {

            .ricerca {
                height: 30px;
                width: 600px;
                margin: 20px;
                text-transform: uppercase;
                padding: 20px;
                border: none;
                border-radius: 20px;
            }

            .btn {
                padding: 10px 40px;
                background: rgb(212, 212, 212);
                border: none;
                border-radius: 20px;
                text-transform: uppercase;
                box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
                cursor: pointer;
            }
            
        }
    }

</style>