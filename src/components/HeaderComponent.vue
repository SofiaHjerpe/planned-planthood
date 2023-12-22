<script setup>
import PlantView from "./PlantView.vue";
const  flowerim ="./assets/img/plant.svg";
const  floweri ="./assets/img/Logo.svg";




</script>
<template>
  <div class="header">
    <PlantView :ficon="floweri" :flowerImg="flowerim" :width="502" />
  </div>
</template>
<style scoped>
.header {
  display: flex;
  top: 0;
  width: 1001px;
  height: 540px;
}
</style>