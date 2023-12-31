<script setup>
import PagesHeader from "@/components/PagesHeader.vue";
import AddPlan from "@/components/AddPlan.vue";
import PlanComponent from "@/components/PlanComponent.vue";
import ReturnView from "@/components/ReturnView.vue";
import PagesFooter from "@/components/PagesFooter.vue";
</script>
<template>
  <div class="myPages" id="start">
    <PagesHeader />
    <AddPlan />
    <PlanComponent />
    <PagesFooter />
    <ReturnView />
  </div>
</template>

<style scoped>
.myPages {
  width: 1000px;
  height: 100%;
  background-color: #fff;
  margin-bottom: 100px;
}
</style>