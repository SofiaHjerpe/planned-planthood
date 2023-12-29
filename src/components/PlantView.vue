
<template>
  <div class="header" style="display: flex; height: 540px">
    <img
      :class="flower[0].width >= 500 ? 'headerImg' : 'plannedPlant'"
      :src="flower[0].imageUrl"
      alt="flowerImg"
    />
    <img :src="flower[0].logoUrl" class="plantLogo" alt="flowerIcon" />

    <div class="rectangle-container">
      <div class="rectangle r1">
        <img src="../assets/img/seedling.svg" class="seed" alt="flowerIcon1" />
      </div>

      <div class="rectangle r2">
        <img src="../assets/img/dig.svg" class="seed" alt="flowerIcon2" />
      </div>
    </div>
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
.rectangle-container {
  display: flex;
  flex-direction: column;
}
.headerImg {
  width: 501px;
  height: 540px;
}
.plannedPlant {
  max-width: 294px;
  max-height: 296px;
}
.plantLogo {
  position: absolute;
  max-width: 190px;
  margin-top: 170px;
  margin-inline: 150px;
}
.rectangle {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 500px;
  height: 270px;
}
.r1 {
  background: #0a846e;
}
.r2 {
  background: #9e6d52;
}
.seed {
  max-width: 176px;
}
.seed:nth-of-type(2) {
  max-width: 155px;
}
@media screen and (max-width: 768px) {
  .rectangle-container {
    flex-direction: row;
  }
  .header {
    flex-direction: column;
    height: 1000px;
  }
  .rectangle {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 195px;
    height: 295px;
  }
  .headerImg {
    width: 390px;
    z-index: 9999;
    height: 390px;
  }
  #app {
    padding: 0;
  }

  .plantLogo {
    position: absolute;
    width: 190px;
    z-index: 9999;
    margin-top: 80px;
    margin-inline: 90px;
  }
  .seed {
    max-width: 112px;
  }
  .seed:nth-of-type(2) {
    max-width: 98px;
  }
}
</style>
