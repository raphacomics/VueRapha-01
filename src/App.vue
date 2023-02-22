<script setup>
import { ref } from 'vue';

const count = ref(0);

const addCount = () => {
  count.value = count.value + 1;
};
const removeCount = () => {
  if (count.value <= 0) {
    return;
  } else {
    count.value = count.value - 1;
  }
};
</script>

<template>
  <div class="container text-center my-5">
    <h1>Rapha Counter in Vue3</h1>
    <hr />
    <p class="display-1 bg-dark text-light py-5 rounded-4">{{ count }}</p>
    <div class="d-grid gap-2">
      <button @click="addCount" class="btn btn-primary">ADD</button>
      <button @click="removeCount" class="btn btn-primary">REMOVE</button>
    </div>
  </div>
</template>

<style scoped></style>
