<template>
  <div class="cards">
    <div v-show="!mobile" v-for="i in firstRow" :key="i">
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
  <div class="cards">
    <div v-show="!mobile" v-for="i in secondRow" :key="i">
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
  <div v-show="mobile">
    <MobileCard />
  </div>
</template>
<script>
import plants from "../plants.js";
import MobileCard from "../components/MobileCard.vue";
export default {
  components: {
    MobileCard,
  },
  data() {
    return {
      plant: plants.plant,
      mobile: false,
      mobileWidth: false,
    };
  },
  created() {
    window.addEventListener("load", this.checkScreen);

    window.addEventListener("resize", this.checkScreen);
  },

  computed: {
    firstRow() {
      return this.plant.slice(0, 3);
    },
    secondRow() {
      return this.plant.slice(3, 6);
    },
  },
  methods: {
    toggleMobileView() {
      this.mobileWidth = !this.mobileWidth;
    },
    checkScreen() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 750) {
        this.mobile = true;
        this.mobileWidth = true;
        return;
      }
      this.mobile = false;
    },
  },
};
</script>
<style scoped>
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
.cards {
  display: flex;
  flex-direction: row;
  justify-content: center;
  width: 100%;
  gap: 20px;
}

.card {
  display: flex;
  flex-direction: column;
  background-color: #fff;
  box-shadow: 3px 4px 4px 0px #00000040;
  width: 294px;
  height: 407px;
}
@media screen and (max-width: 768px) {
  .cards {
    max-width: 300px;
    gap: 13px;
  }
  
}
</style>