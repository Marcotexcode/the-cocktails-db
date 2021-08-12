
<template>

  <div id="app">

    <Header/>

    <Search @searchCockt="searchCocktail"/>

    <Main :listCocktails="filterCocktailList"/>

  </div>

</template>


<script>

  import axios from 'axios';
  import Header from '@/components/Header.vue';
  import Main from '@/components/Main.vue';
  import Search from '@/components/Search.vue';


  export default {

    name: 'App',

    components: {

      Header,
      Main,
      Search

    },

    data() {
            
      return {

        apiURL: 'https://www.thecocktaildb.com/api/json/v1/1/search.php?f=a',

        listCockt: [],
        searchCocktails: [],
          
      }

    },

    created() {

      this.getListCocktail();

    },

    computed: {

      filterCocktailList() {

        return this.listCockt.filter( element => {
          
          return element.strDrink.includes(this.searchCocktails)

        });

      }

    },

    methods: {

      // CHIAMATA AXIOS
      getListCocktail() {

        axios.get(this.apiURL).then(response => {      

          this.listCockt = response.data.drinks;

          console.log(this.listCockt);

        })

      },

      // RICERCA INPUT
      searchCocktail(searchInput) {

        this.searchCocktails = searchInput;

        console.log('ciao', this.searchCocktails);

      }

    }

  }

</script>


<style lang="scss">

  @import '@/style/commons.scss';
    

</style>
