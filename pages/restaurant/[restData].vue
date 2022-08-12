<!-- this is how we add dynamic routes -->
<template>
  <div>THIS IS THE RESTAURANT DATA</div>
  <br />
  <h1>{{ routeName }}</h1>
  <br />
  <div>Name -- {{ restaurant.name }}</div>
  <div>Detail -- {{ restaurant.content }}</div>
  <div>Revenue -- {{ restaurant.revenue }} million</div>
  <div class="image-container"><img :src="restaurant.imageUrl" alt="" /></div>
</template>

<script setup lang="ts">
import restaurants from "@/data.json";

const route = useRoute();
const routeName = route.params.restData;

const restaurant = restaurants.find((el) => el.name === routeName);
</script>

<style scoped>
.image-container {
  width: 30%;
  height: 30%;
}
</style>
