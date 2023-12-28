<script setup>
import SeasonView from "../components/SeasonView.vue";
</script>

<template>
  <div class="planned-container">
    <h1>Planned planthood</h1>
    <SeasonView />
  </div>
</template>
<style scoped>
h1 {
  font-family: "Maven Pro", sans-serif;
  font-weight: 500;
  font-size: 48px;
  text-transform: uppercase;
  color: #0a846e;
  align-self: center;
}
.planned-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-top: 2px;
  z-index: -1;
  width: 1000px;
  background-color: #fff;
}
</style>
