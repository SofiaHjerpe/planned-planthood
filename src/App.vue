<script setup>
import { RouterLink, RouterView } from "vue-router";
import HeaderComponent from "./components/HeaderComponent.vue";
import MyPages from "./views/MyPages.vue";

defineProps({
  myPage: {
    type: Boolean,
    value: false,
    required: true,
  },
});
</script>

<template>
  <div class="page-container">
    <div class="header">
      <HeaderComponent />

      <div>
        <nav>
          <RouterLink to="/">Planner</RouterLink>
          <RouterLink to="/">Historik</RouterLink>
          <RouterLink to="/">Tips</RouterLink>
          <RouterLink to="/mypages">Logga in</RouterLink>
        </nav>
      </div>
    </div>

    <RouterView />
  </div>
</template>


<style scoped>
.page-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.header {
  display: flex;
  flex-direction: column;
  width: 1200px;
  align-items: center;
  justify-content: center;
}
.headerReverse {
  display: flex;
  flex-direction: column;
  width: 1200px;
  align-items: center;
  justify-content: center;
}

nav {
  width: 1001px;
  display: flex;
  justify-content: center;
  gap: 150px;
  z-index: 9999;
  align-items: center;
  background-color: #fff;
  box-shadow: 0px 4px 4px 0px #03382f1c;
  height: 60px;
}
nav a {
  color: #055647;
  font-weight: 500;
  text-transform: uppercase;
  font-family: "Maven Pro", sans-serif;
  font-size: 20px;
}
a:hover {
  background-color: transparent;
}
</style>
