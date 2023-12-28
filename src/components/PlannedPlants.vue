<template>
  <div class="plants">
    <h3 class="heading">Våra planerade planteringar:</h3>
    <div class="cards">
      <div v-for="i in firstRow" :key="i">
        <div class="card">
          <img class="plannedPlant" :src="i.imageUrl" alt="flowerImg" />
          <img :src="i.logoUrl" class="plantLogo" alt="flowerIcon" />
          <div class="plant-name">
            <h4>{{ i.title }}</h4>
            <p class="date">{{ i.date }}</p>
          </div>
          <div class="plant-name">
            <p class="plant">{{ i.plant }}</p>
            <button class="remove">Ta bort</button>
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
    firstRow() {
      return this.plant.slice(0, 3);
    },
    secondRow() {
      return this.plant.slice(4, 6);
    },
  },
};
</script>
<style scoped>
.plants {
  display: flex;
  flex-direction: column;
  gap: 40px;
}
.heading {
  font-family: "Lato", sans-serif;
  font-weight: 600;
  font-size: 32px;
  align-self: center;
  line-height: 38.4px;
}
.plannedPlant {
  width: 294px;
  height: 296px;
}
h4 {
  font-family: "Lato", sans-serif;
  font-weight: 600;
  font-size: 24px;
  line-height: 28.8px;
}
.remove {
  background-color: #b93857;
  color: #fff;
  font-size: 15px;
  font-family: "Open-sans", sans-serif;
  border-radius: 9px;
  text-transform: uppercase;
  font-weight: 700;
  width: 97px;
  height: 30px;
  border: none;
}
.plant {
  font-family: "Lato", sans-serif;
  font-weight: 300;
  font-size: 16px;
}
.plant-name {
  display: flex;
  justify-content: space-between;
  margin-top: 20px;
  margin-inline: 16px;
}
.date {
  font-weight: 700;
  font-family: "Open-sans", sans-serif;
  font-size: 16px;
  margin-inline: 16px;
}
.plantLogo {
  margin-top: -250px;
  width: 50%;
  align-self: center;
}
.cards {
  display: flex;
  flex-direction: row;
  justify-content: center;
  width: 100%;
  gap: 20px;
}
.plantLogo {
  display: flex;
}

.card {
  display: flex;
  flex-direction: column;
  background-color: #fff;
  box-shadow: 3px 4px 4px 0px #00000040;
  width: 294px;
  gap: 20px;
  height: 407px;
}
</style>