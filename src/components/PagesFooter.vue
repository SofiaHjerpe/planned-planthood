<template>
  <div class="brown-container">
    <div class="image-row">
      <img src="../assets/img/plantf1.jpg" alt="pf1" />
      <img src="../assets/img/plantf2.jpg" alt="pf2" />
      <img src="../assets/img/plantf3.jpg" alt="pf3" />
      <img src="../assets/img/plantf4.jpg" alt="pf4" />
    </div>
  </div>
</template>
<style scoped>
.brown-container {
  background-color: #9e6d52;
  display: block;
  height: 336px;
}
.image-row {
  display: flex;
  gap: 30px;
  justify-content: center;
  align-items: center;
}
.image-row img {
  width: 220px;
  height: 277px;
  margin-top: 30px;
}
</style>