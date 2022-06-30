<template>
    <main class="wrapper">
        <h1>Products</h1>
        <div class="card-container">
            <ProductCardVue
            v-for="(product, index) in inventory.slice(0,6)"
            :key="product.id"
            class="card"
            :index="index"
            :product="product"
            :addToCart="addToCart"
        />
        </div>
    </main>
</template>

<script>
import ProductCardVue from '@/components/ProductCard.vue'

export default {
  props: ['inventory', 'addToCart'],
  components: {
    ProductCardVue
  }
}
</Script>
