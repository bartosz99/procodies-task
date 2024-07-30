<script setup lang="ts">
import cards_1 from '../assets/images/cards_1.png';
import { features, faq } from '../constants/index';
</script>

<template>
  <div class="">
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
    <div class="w-full bg-gray4 flex gap-16 items-center my-16 text-green2">
      <div class="" v-for="(question, index) in faq">
        <h6 class="text-12">{{ question.question }}</h6>
        <p class="text-10">{{ question.answer }}</p>
      </div>
    </div>
    <div class="w-full flex flex-col items-center pb-8">
      <p class="text-12">We accept the following credit cards</p>
      <img :src="cards_1" alt="Credit Cards" />
    </div>
  </div>
</template>
