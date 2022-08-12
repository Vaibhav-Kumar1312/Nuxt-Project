<template>
  <div>
    {{ rank }}
    ----
    <NuxtLink :to="`/restaurant/${name}`">{{ name }}</NuxtLink>
  </div>
</template>

<script setup lang="ts">
interface RowProps {
  rank: number;
  name: string;
}
const props = defineProps<RowProps>();
</script>

<style></style>
