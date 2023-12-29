<script setup>
import SeasonView from "../components/SeasonView.vue";
import PlannedPlants from "../components/PlannedPlants.vue";
import FooterComponent from "./FooterComponent.vue";
import ReturnView from "./ReturnView.vue";
</script>

<template>
  <div class="planned-container" id="start">
    <h1>Planned planthood</h1>
    <SeasonView :reverseComponent="false" />
    <PlannedPlants />
    <SeasonView :reverseComponent="true" />
    <FooterComponent />
    <ReturnView />
  </div>
</template>
<style scoped>
h1 {
  font-family: "Maven Pro", sans-serif;
  font-weight: 500;
  font-size: 48px;
  text-transform: uppercase;
  color: #0a846e;
  margin-top: 20px;
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
@media screen and (max-width: 768px) {
  h1 {
    font-size: 24px;
  }
  .planned-container {
    max-width: 768px;
  }
}
</style>
