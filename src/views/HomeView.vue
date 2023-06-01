<script setup>
import cars from '../data/cars.json';
import { RouterLink } from 'vue-router';
</script>

<template>
  <div>
    <h1>Home View</h1>
    <div class="cars">
      <RouterLink
        v-for="car in cars"
        :key="car.id"
        href=""
        :to="`/cars/${car.id}`"
      >
        {{ car.name }}</RouterLink
      >
      >
    </div>
  </div>
</template>

<style scoped>
.cars {
  display: flex;
  align-items: center;
}

.cars a {
  text-decoration: none;
  color: black;
  width: 100%;
  box-shadow: 1px 1px 1px rgba(0, 0, 0, 0.1);
  margin: 10px;
}
</style>
