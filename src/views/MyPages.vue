<script setup>
import PagesHeader from "@/components/PagesHeader.vue";
import AddPlan from "@/components/AddPlan.vue";
import PlanComponent from "@/components/PlanComponent.vue";
</script>
<template>
  <div class="myPages">
    <PagesHeader />
    <AddPlan />
    <PlanComponent />
  </div>
</template>

<style scoped>
.myPages {
  width: 1000px;
  height: 100%;
  background-color: #fff;
}
</style>