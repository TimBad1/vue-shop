<template>
  <ul class="catalog__list">
      <ProductItem v-for="product in products" :img="product.img" :title="product.title" :price="product.price" :key="product.id"/>
  </ul>
</template>

<script>
import ProductItem from "@/components/ProductItem.vue";

export default {
  components: {ProductItem},
  props: ['products'],
}
</script>