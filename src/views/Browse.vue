// This will let them search for movies by actors, genres, or titles
<template>
  <!-- <div class="browse">
    <h1>This is a browse page</h1>
  </div> -->
    <div>
        <div class="wrapper">
            <div class="search">
                <form class="pure-form">
                <i class="fas fa-search"></i><input v-model="searchText" />
                </form>
            </div>
        </div>
        <MovieList :products="products" />
    </div>
</template>

<script>
import MovieList from "../components/MovieList.vue"

export default {
    name: 'Home',
    components: {
        MovieList
    },
    data() {
        return {
            searchText: '',
        }
    },
    computed: {
        products() {
            // return this.$root.$data.products;
            return this.$root.$data.products.filter(product => product.title.toLowerCase().search(this.searchText.toLowerCase()) >= 0);
        // Object.values(users).filter
        }
    },
}
</script>