<script setup lang="ts">
import security_providers from '../assets/images/security_providers.png';

const inputData = ref({
  first_name: '',
  last_name: '',
  street: '',
  postal_code: '',
  city: '',
  phone_number: '',
  email: ''
});

const handleSubmitForm = () => {
  console.log('Form submitted, values:' + JSON.stringify(inputData.value));
};
</script>

<template>
  <div class="border rounded-20 border-gray3 flex flex-col gap-4 p-4 max-w-4xl">
    <h2 class="text-32 text-green2 text-center font-medium">Enter Details</h2>
    <div class="flex gap-4">
      <input
        class="input-primary text-16"
        placeholder="First Name"
        v-model="inputData.first_name"
      />
      <input class="input-primary" placeholder="Last Name" v-model="inputData.last_name" />
    </div>
    <input class="input-primary" placeholder="Street" v-model="inputData.street" />
    <div class="flex gap-4">
      <input class="input-primary" placeholder="Postal Code" v-model="inputData.street" />
      <input class="input-primary" placeholder="City" v-model="inputData.street" />
    </div>
    <input class="input-primary" placeholder="Phone number" v-model="inputData.street" />
    <input class="input-primary" placeholder="E-mail" v-model="inputData.street" />
    <button class="btn-primary uppercase mt-2 font-medium" @click="handleSubmitForm">
      Proceed to payment
    </button>
    <div class="flex items-center justify-center gap-4 my-2">
      <img :src="security_providers" alt="security providers" />
    </div>
  </div>
</template>
