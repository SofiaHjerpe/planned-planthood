<script setup>
import { RouterLink, RouterView } from "vue-router";
import HeaderComponent from "./components/HeaderComponent.vue";

</script>

<template>
  <div class="header">
    <div>
      <HeaderComponent />
    </div>
    <div>
      <nav>
        <RouterLink to="/">Planner</RouterLink>
        <RouterLink to="/">Historik</RouterLink>
        <RouterLink to="/">Tips</RouterLink>
        <RouterLink to="/">Logga in</RouterLink>
      </nav>
    </div>
  </div>

  <RouterView />
</template>

<style scoped>
.header {
  display: flex;
  flex-direction: column;
  width: 1200px;
  align-items: center;
  justify-content: center;
}

nav {
  width: 1001px;
  top: 0;
  display: flex;
  justify-content: center;
  gap: 150px;
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
