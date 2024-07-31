<script setup lang="ts">
import cards_1 from '../assets/images/cards_1.png';
import { features, faq } from '../constants/index';
</script>

<template>
  <div>
    <div class="my-8 mx-auto max-w-screen-2xl">
      <div class="landing-section flex-col-reverse lg:flex-row">
        <Products />
        <div class="flex flex-col items-center flex-grow gap-8">
          <div>
            <h1 class="text-52 text-dark font-extrabold">
              Chance to win a StockX Mystery Box today!
            </h1>
            <p class="text-22 text-dark">Unleash the Excitement of Mystery Electronics</p>
          </div>
          <div class="w-full flex justify-center">
            <Form class="flex-grow" />
          </div>
        </div>
      </div>

      <div class="landing-section flex-col gap-4">
        <h2 class="text-48 font-bold text-green2 text-center">
          Top Tech Mystery Box <br class="hidden lg:block" />
          at Unbeatable Prices
        </h2>
        <p class="text-20 font-medium text-green text-center">
          Fast shipping | Easy returns | Special discounts for students
        </p>
      </div>

      <div class="landing-section flex-col">
        <div
          class="flex flex-col lg:flex-row gap-8 items-center"
          :class="{ 'lg:flex-row-reverse': index % 2 !== 0 }"
          v-for="(feature, index) in features"
        >
          <img :src="feature.image" :alt="feature.title" />
          <div>
            <h3 class="text-dark text-42 mb-6 font-bold color-dark">{{ feature.title }}</h3>
            <p
              class="text-dark font-normal leading-8 mb-3"
              v-for="paragraph in feature.description"
            >
              {{ paragraph }}
            </p>
          </div>
        </div>
      </div>

      <div class="landing-section py-4 grid lg:grid-cols-3 bg-gray4 text-green2">
        <div class="" v-for="(question, index) in faq">
          <h6 class="text-12 font-semibold mb-2">{{ question.question }}</h6>
          <p class="text-10">{{ question.answer }}</p>
        </div>
      </div>

      <div class="landing-section flex-col gap-2">
        <p class="text-12 text-dark">We accept the following credit cards</p>
        <img :src="cards_1" alt="Credit Cards" />
      </div>
    </div>
  </div>
</template>
