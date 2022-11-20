<template>
  <main class="wrapper">
    <h1>Products</h1>
    <div class="card-container">
      <ProductCard v-for="(product, index) in inventory.slice(0,6)" :key="index" :index="index" :product="product"
        :addToCart="addToCart" class="card">

      </ProductCard>
    </div>
  </main>
</template>

<script>
import ProductCard from '@/components/ProductCard.vue'

export default {
  name: 'ProductView',
  props: ['inventory', 'addToCart', 'product'],
  components: {
    ProductCard
  }
}
</script>
