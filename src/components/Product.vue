<template>
    <div class="container product-container">
            <h4 class="product-heading">Fetured Items</h4>
            <p class="product-text">Shop for items based on what we featured in this week</p>
        <div class="product">    
  
            <Card v-bind:key="good.id" v-bind:good="good" v-for="good of catalog" />

        </div>
        <a href="catalog.html" class="browse-button">Browse All Product</a>
    </div>
</template>

<script>
import Card from './Card.vue'

export default {
    name: 'Catalog',
    components: {
        Card
    },
    computed: {
        catalog() {
            return this.$store.getters.getCatalog
        }
    }
}
</script>