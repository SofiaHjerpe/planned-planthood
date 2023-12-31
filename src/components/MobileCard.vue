<template>
  <div class="mobile-cards">
    <div class="cards">
      <div v-for="i in firstMobileRow" :key="i">
        <div class="card">
          <img class="plannedPlant" :src="i.imageUrl" alt="flowerImg" />
          <img :src="i.logoUrl" class="plantLogo" alt="flowerIcon" />
          <div class="plant-name">
            <h4>{{ i.title }}</h4>
            <p class="date">{{ i.date }}</p>
          </div>
          <div class="plant-name">
            <p class="plant">{{ i.plant }}</p>
            <span class="material-symbols-outlined"> delete </span>
          </div>
        </div>
      </div>
    </div>
    <div class="cards">
      <div v-for="i in secondMobileRow" :key="i">
        <div class="card">
          <img class="plannedPlant" :src="i.imageUrl" alt="flowerImg" />
          <img :src="i.logoUrl" class="plantLogo" alt="flowerIcon" />
          <div class="plant-name">
            <h4>{{ i.title }}</h4>
            <p class="date">{{ i.date }}</p>
          </div>
          <div class="plant-name">
            <p class="plant">{{ i.plant }}</p>
            <span class="material-symbols-outlined"> delete </span>
          </div>
        </div>
      </div>
    </div>
    <div class="cards">
      <div v-for="i in thirdMobileRow" :key="i">
        <div class="card">
          <img class="plannedPlant" :src="i.imageUrl" alt="flowerImg" />
          <img :src="i.logoUrl" class="plantLogo" alt="flowerIcon" />
          <div class="plant-name">
            <h4>{{ i.title }}</h4>
            <p class="date">{{ i.date }}</p>
          </div>
          <div class="plant-name">
            <p class="plant">{{ i.plant }}</p>
            <span class="material-symbols-outlined"> delete </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import plants from "../plants.js";
export default {
  data() {
    return {
      plant: plants.plant,
    };
  },
  computed: {
    firstMobileRow() {
      return this.plant.slice(0, 2);
    },
    secondMobileRow() {
      return this.plant.slice(2, 4);
    },
    thirdMobileRow() {
      return this.plant.slice(4, 6);
    },
  },
};
</script>
<style scoped>
.mobile-cards {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.plannedPlant {
  width: 175px;
  height: 160px;
}
h4 {
  font-family: "Lato", sans-serif;
  font-weight: 600;
  font-size: 14px;
  line-height: 28.8px;
}
.material-symbols-outlined {
  color: #b93857;
  width: 13px;
  height: 16px;
}
.plant {
  font-family: "Lato", sans-serif;
  font-weight: 300;
  font-size: 10px;
}
.plant-name {
  display: flex;
  justify-content: space-between;
  margin-top: 40px;
  margin-inline: 10px;
}
.plant-name:nth-of-type(2) {
  margin-top: 0;
}

.date {
  font-weight: 700;
  font-family: "Open-sans", sans-serif;
  font-size: 10px;
  margin-inline: 0;
  align-self: center;
}
.plantLogo {
  display: flex;
  margin-top: 0;
  color: #fff;
  width: 65px;
  margin-top: -130px;
  height: 89px;
  align-self: center;
}
.cards {
  display: flex;
  flex-direction: row;
  max-width: 300px;
  margin-inline: 8px 10px;
  gap: 10px;
}
.card {
  display: flex;
  flex-direction: column;
  background-color: #fff;
  box-shadow: 3px 4px 4px 0px #00000040;
  width: 175px;
  height: 220px;
}
</style>