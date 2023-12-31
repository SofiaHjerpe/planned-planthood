<template>
  <div class="brown-container">
    <div class="image-row">
      <div class="img-container">
        <img src="../assets/img/plantf1.jpg" alt="pf1" />
        <img src="../assets/img/plantf2.jpg" alt="pf2" />
      </div>
      <div class="img-container">
        <img src="../assets/img/plantf3.jpg" alt="pf3" />
        <img src="../assets/img/plantf4.jpg" alt="pf4" />
      </div>
    </div>
  </div>
</template>
<style scoped>
.brown-container {
  background-color: #9e6d52;
  display: block;
  height: 336px;
  padding-inline: 0;
}
.image-row {
  display: flex;
  gap: 30px;
  justify-content: center;
  align-items: center;
}
.img-container {
  display: flex;
  gap: 30px;
}
.img-container img {
  width: 220px;
  height: 277px;
  margin-top: 30px;
}
@media screen and (max-width: 768px) {
  .brown-container {
    height: 220px;
    padding-inline: 10px;
  }
  .image-row {
    gap: 10px;
    padding-top: 10px;
    justify-content: flex-start;
    align-items: flex-start;
  }
  .img-container {
    display: flex;
    flex-direction: column;
    gap: 0;
  }
  .img-container img {
    width: 173px;
    height: 86px;
    margin-top: 10px;
  }
}
</style>