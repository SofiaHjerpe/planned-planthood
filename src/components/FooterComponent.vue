<template>
  <div class="bg">
    <div class="bg-overlay">
      <div class="bg-overflow">
        <div class="text-and-icon">
          <h1 class="seeu">Vi hörs!</h1>
          <img src="../assets/img/Logo.svg" alt="logo" />
        </div>
        <div class="footer-all-info">
          <div class="footer-info">
            <span class="material-icons">call</span>
            <p class="f-info">0701-234567</p>
          </div>
          <div class="footer-info">
            <p class="f-info">mail@mail.se</p>
            <span class="material-icons">mail</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
.bg {
  margin-top: 100px;
  background-image: url("../assets/img/footer.jpg");
  background-size: cover;
  background-position: 50%;
  height: 644px;
  background-repeat: no-repeat;
}
.bg-overlay {
  width: 100%;
  background-color: #05564733;
  height: 100%;
}
.bg-overflow {
  background-color: #000000c9;
  width: 500px;
  height: 100%;
}
.text-and-icon {
  display: flex;
  width: 1000px;
  z-index: 9999;
  align-items: center;
  gap: 0;
  padding: 150px;
  justify-content: space-between;
}
.seeu {
  font-family: "Maven Pro", sans-serif;
  font-weight: 500;
  font-size: 64px;
  color: #fff;
  margin-inline: 0;
}
.footer-all-info {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 500px;
  margin-top: 50px;
  padding: 16px;
  margin-top: 0;
}
.footer-info {
  display: flex;
  flex-direction: row;
  gap: 5px;
  align-items: center;
  justify-content: center;
}
.material-icons {
  color: #fff;
  max-width: 35px;
  height: 35px;
  align-self: center;
  margin-top: 10px;
  bottom: 0;
}
.f-info {
  color: #fff;
  font-family: "Maven-pro", sans-serif;
  font-weight: 400;
  font-size: 20px;
}
@media screen and (max-width: 768px) {
  .bg-overflow {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 50%;
  }

  .seeu {
    font-size: 32px;
    font-weight: 500;
    margin-top: 10px;
    margin-inline: 0 190px;
  }
  .bg-overlay {
    display: flex;
    flex-direction: column-reverse;
    width: 100%;
    background-color: #05564733;
    height: 100%;
  }
  .text-and-icon {
    flex-direction: column-reverse;
    width: 600px;
    z-index: 9999;
    align-items: center;
    gap: 200px;
    padding: 0;
    justify-content: center;
  }
  .text-and-icon img {
    margin-top: -250px;
    margin-inline: 0 200px;
    width: 190px;
  }
  .bg {
    flex-direction: column-reverse;
    height: 774px;
    background-image: url("../assets/img/footer.jpg");
    background-size: cover;
    background-position: 50%;
  }
  .footer-all-info {
    margin-top: 130px;
    width: 400px;
  }
  .f-info {
    font-size: 12px;
  }
  .footer-info:nth-of-type(2) {
    margin-inline: 0 30px;
  }
}
</style>
