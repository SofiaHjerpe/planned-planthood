<script setup>
import CardComponent from "./CardComponent.vue";
</script>

<template>
  <div class="plants">
    <h3 class="heading">Våra planerade planteringar:</h3>

    <CardComponent />

    <button class="more">Visa fler</button>
  </div>
</template>

<style scoped>
.plants {
  display: flex;
  flex-direction: column;
  gap: 40px;
  max-width: 100%;
}
.heading {
  font-family: "Lato", sans-serif;
  font-weight: 600;
  font-size: 32px;
  margin-bottom: 0;
  align-self: center;
  line-height: 38.4px;
}
.more {
  box-shadow: 0px 4px 4px 0px #00000040;
  background-color: #0a846e;
  color: #fff;
  border-radius: 9px;
  height: 63px;
  width: 179px;
  border: none;
  outline: none;
  font-family: "Inter", sans-serif;
  font-size: 24px;
  font-weight: 600;
  line-height: 32.68px;
  margin-top: 10px;
  text-transform: none;
  align-self: center;
  margin-inline: 0;
}
@media screen and (max-width: 768px) {
  .plants {
    display: block;
  }
  .heading {
    font-size: 16px;
    margin-inline: 90px;
    margin-bottom: 10px;
  }

  .more {
    height: 35px;
    width: 116px;
    text-transform: uppercase;
    font-size: 16px;
    font-weight: 700;
    line-height: 22px;
    margin-top: 10px;
    align-self: center;
    margin-top: 30px;
    margin-inline: 140px;
  }
}
</style>