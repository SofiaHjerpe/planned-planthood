<script setup>
import PlantView from "./PlantView.vue";
</script>
<template>
  <div class="header">
    <PlantView />
  </div>
</template>
<style scoped>
.header {
  display: flex;
  top: 0;
  padding: 0;
  align-items: flex-start;
  justify-content: flex-start;
}
@media screen and  (max-width: 768px){
  .header{
    display: flex;
    flex-direction: column;
  }
}
</style>