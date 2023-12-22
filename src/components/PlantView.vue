<script setup>
import HeaderComponent from "./HeaderComponent.vue";

   
defineProps({
  flowerImg: {
    type: String,
    required: true,
  },
  width: {
    type: Number,
    required: true,
  },
  ficon: {
    type: String,
    required: true,
  },
});
</script>
<template>
  <div :class="width >= 500 ? 'headerImg' : 'plannedPlant'">
    <img :src="flowerImg" alt="flowerImg">
    <img :src="ficon" alt="flowerIcon"  />
  </div>
</template>
<style scoped>
.headerImg img {
  width: 501px;
  height: 540px;
}
.plannedPlant {
  width: 294px;
  height: 296px;
}
</style>