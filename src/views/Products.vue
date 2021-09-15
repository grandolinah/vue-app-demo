<template>
  <main class="wrapper">
  <h1>Products</h1>
  <ProductCard
    v-for="(product) in inventory"
    :key="product.id"
    :product="product"
    :index="index"
    :addToCart="addToCart"
  />
  </main>
</template>

<script>
import ProductCard from '../components/ProductCard.vue';

export default {
  name: 'Products',
  components: {
    ProductCard,
  },
  props: ['inventory', 'addToCart'],
};

</script>
