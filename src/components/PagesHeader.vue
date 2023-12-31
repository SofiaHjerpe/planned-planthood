<template>
  <img class="headerImg" :src="flower[1].imageUrl" alt="flowerImg" />
  <div class="bg-overlay"></div>
  <div class="logo">
    <img :src="flower[1].logoUrl" class="plantLogo" alt="flowerIcon" />
    <h1>Mina sidor</h1>
  </div>
</template>
<script>
import data from "../data.js";
export default {
  data() {
    return {
      flower: data.flower,
    };
  },
};
</script>
<style scoped>
.headerImg {
  width: 100%;
  height: 379px;
  z-index: -1;
}
.bg-overlay {
  height: 379px;
  margin-top: -385px;
  position: relative;
  z-index: 9999;
  width: 1001px;
  background-color: #00000033;
}
.plantLogo {
  align-self: center;
  position: relative;
  width: 189px;
  height: 186px;
  z-index: 9999;
  bottom: 0;
  margin-inline: 0;
}
.logo {
  display: flex;
  flex-direction: column;
  gap: 20px;
  position: relative;
  margin-top: -340px;
  z-index: 9999;
  margin-bottom: 200px;
}
h1 {
  font-family: "Maven-pro", sans-serif;
  font-size: 40px;
  position: relative;
  z-index: 9999;
  color: #fff;
  align-self: center;
  font-weight: 500;
  bottom: 0;
  margin-inline: 0;
}
@media screen and (max-width: 768px) {
  .bg-overlay {
    height: 379px;
    margin-top: -395px;
    z-index: -1;
  }
  .headerImg {
    width: 390px;
    height: 390px;
    margin-top: -40px;
    margin-bottom: 80px;
    z-index: -1;
  }
  .logo {
    position: relative;
    margin-top: 0;
    z-index: 9999;
    margin-bottom: 0;
  }

  .logo {
    width: 100%;
    height: 10px;
  }
  .plantLogo {
    align-self: flex-start;
    margin-inline: 100px;
    position: relative;
    bottom: 360px;
    width: 189px;
    height: 186px;
    z-index: 9999;
  }
  h1 {
    font-size: 32px;
    align-self: flex-start;
    bottom: 350px;
    margin-inline: 120px;
    position: relative;
    z-index: 9999;
  }
}
</style>