<script setup lang="ts">
import { features } from '../constants/index';
</script>

<template>
  <div class="p-8">
    <div class="flex items-center gap-16">
      <Products />
      <div>
        <h1 class="text-52 text-dark font-extrabold">Chance to win a StockX Mystery Box today!</h1>
        <p class="text-22 text-dark">Unleash the Excitement of Mystery Electronics</p>
        <Form />
      </div>
    </div>
    <div class="w-full flex flex-col items-center my-16">
      <h2 class="text-48 font-bold text-green2 text-center">
        Top Tech Mystery Box <br />
        at Unbeatable Prices
      </h2>
      <p class="text-20 font-medium text-green">
        Fast shipping | Easy returns | Special discounts for students
      </p>
    </div>
    <div class="w-full flex flex-col items-center my-16">
      <div
        class="flex gap-32 items-center"
        :class="{ 'flex-row-reverse': index % 2 !== 0 }"
        v-for="(feature, index) in features"
      >
        <img :src="feature.image" :alt="feature.title" />
        <div>
          <h3 class="text-42 mb-6 font-bold color-dark">{{ feature.title }}</h3>
          <p class="font-normal leading-8 mb-3" v-for="paragraph in feature.description">
            {{ paragraph }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
