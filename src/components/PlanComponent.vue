<template>
  <div class="planned">
    <h2 class="planned-plants">Dina planerade planteringar:</h2>
    <div class="card">
      <img class="plannedPlant" :src="plant[0].imageUrl" alt="flowerImg" />
      <img :src="plant[0].logoUrl" class="plantLogo" alt="flowerIcon" />
      <div class="plant-name">
        <h4>{{ plant[0].title }}</h4>
        <p class="date">{{ plant[0].date }}</p>
      </div>
      <div class="plant-name">
        <p class="plant">{{ plant[0].plant }}</p>
        <button class="remove">Ta bort</button>
      </div>
    </div>
  </div>
  
    <PlantComponent />
  
</template>
<script>
import plants from "../plants.js";
import PlantComponent from "@/components/PlantComponent.vue";
export default {
  components: {
    PlantComponent,
  },
  data() {
    return {
      plant: plants.plant,
    };
  },
};
</script>
<style scoped>
.planned {
  display: flex;
  flex-direction: column;
  gap: 30px;
  justify-content: center;
  margin-bottom: 60px;
}
.planned-plants {
  font-family: "Lato", sans-serif;
  font-weight: 600;
  font-size: 32px;
  align-self: center;
  margin-top: 30px;
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
  margin: 20px;
  margin-top: 60px;
  margin-inline: 16px;
}
.plant-name:nth-of-type(2) {
  margin-top: 0;
}
.date {
  font-weight: 700;
  font-family: "Open-sans", sans-serif;
  font-size: 16px;
  margin-inline: 16px;
}
.plantLogo {
  display: flex;
  margin-top: -250px;
  width: 50%;
  align-self: center;
}
.card {
  display: flex;
  flex-direction: column;
  background-color: #fff;
  box-shadow: 3px 4px 4px 0px #00000040;
  width: 294px;
  height: 407px;
  margin-inline: 30px;
}
</style>