
<template>
  <div style="display: flex; gap: 35px">
    <div class="circle">
      <img src="../assets/img/Vectorseedpackage.svg" class="seed" alt="seed" />
    </div>
    <div class="info-text">
      <div>
        <h2>Säsong att så</h2>
      </div>
      <div>
        <p>Våren är äntligen här i kollektivet!</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
        <p>Cupiditate, ab quod dolores eu fugiat nulla pariatur.</p>
      </div>
      <div>
        <button class="sa-btn">Så-tips</button>
      </div>
    </div>
  </div>
  <div style="display:flex; justify-content: center">
    <hr class="green-line" />
  </div>
</template>
<script>
export default {};
</script>
 <style scoped>
h2 {
  font-weight: 700;
  font-family: "Open-sans", sans-serif;
  font-size: 32px;
  margin-top: 120px;
  line-height: 44px;
  color: #1e1e1e;
}
p {
  color: #000;
  font-family: "Open-sans", sans-serif;
  font-size: 16px;
  font-weight: 400;
  line-height: 22px;
}
.circle {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 400px;
  height: 400px;
  margin: 30px;
  border-radius: 200px;
  background-color: #0a846e;
}
.seed {
  width: 197px;
  height: 197px;
}
.info-text {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.sa-btn {
  box-shadow: 0px 4px 4px 0px #00000040;
  background-color: #0a846e;
  color: #fff;
  border-radius: 9px;
  height: 63px;
  width: 179px;
  border: none;
  outline: none;
  font-family: "Open-sans", sans-serif;
  font-size: 24px;
  font-weight: 700;
  text-transform: uppercase;
  line-height: 32.68px;
  margin-top: 10px;
  margin-inline: 230px 0;
}
.green-line {
  background-color: #055647;
  width: 303.24px;
  height: 3px;
  margin-bottom: 30px;
  margin-top: 100px;
}
</style>