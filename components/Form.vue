<script setup lang="ts">
import encryption_1 from '../assets/images/encryption/encryption_1.png';
import encryption_2 from '../assets/images/encryption/encryption_2.png';
import encryption_3 from '../assets/images/encryption/encryption_3.png';

const encryptionImages = [encryption_1, encryption_2, encryption_3];

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
  <div class="border rounded-20 border-gray3 flex flex-col gap-2 p-4">
    <h2 class="text-32 text-green2 text-center">Enter Details</h2>
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
    <button class="btn-primary" @click="handleSubmitForm">Submit</button>
    <div class="flex gap-4">
      <image v-for="image in encryptionImages" :src="image" />
    </div>
  </div>
</template>
