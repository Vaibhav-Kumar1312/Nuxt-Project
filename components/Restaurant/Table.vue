<template>
  <div class="table">
    <h1>TOP 50 Ranking</h1>
    <p>Click on the restaurants to know about the restaurant</p>
    <br />
    <div class="table-container">
      <div class="">
        <RestaurantRow
          v-for="item in restList.first"
          :key="item.id"
          :name="item.name"
          :rank="item.rank"
        />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import restaurants from "@/data.json";

const restList = { first: [...restaurants].splice(0, 50) };
</script>

<style></style>
