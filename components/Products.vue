<script setup lang="ts">
import product_1 from '../assets/images/products/product_1.png';
import product_2 from '../assets/images/products/product_2.png';
import product_3 from '../assets/images/products/product_3.png';
import product_4 from '../assets/images/products/product_4.png';

const products = [
  {
    id: 2,
    name: 'Product 2',
    image: product_2
  },
  {
    id: 3,
    name: 'Product 3',
    image: product_3
  },
  {
    id: 4,
    name: 'Product 4',
    image: product_4
  }
];

const currentProduct = ref({
  id: 1,
  name: 'Product 1',
  image: product_1
});
</script>

<template>
  <div class="flex flex-col gap-4">
    <div>
      <img class="max-h-md max-w-md" :src="currentProduct.image" :alt="currentProduct.name" />
    </div>
    <div class="flex justify-between">
      <div
        class="max-w-32"
        v-for="product in products"
        :key="product.id"
        @click="currentProduct = product"
      >
        <img :src="product.image" :alt="product.name" />
      </div>
    </div>
  </div>
</template>
