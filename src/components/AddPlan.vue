<template>
  <h2 class="add">Lägg till ny planering:</h2>
  <div class="inputs">
    <div class="input-holder">
      <label for="name">Planta:</label>
      <input class="input" type="text" name="planta" id="name" />
    </div>
    <div class="input-holder">
      <label for="date">Datum:</label>
      <input class="input" type="text" name="date" id="date" />
    </div>
  </div>
  <div class="btn-container">
    <button class="addBtn">Lägg till</button>
  </div>
</template>
<style scoped>
.add {
  margin: 0;
  color: #060606;
  font-weight: 400;
  font-size: 32px;
  margin-inline: 30px;
  font-family: "Open-sans", sans-serif;
  line-height: 43.58px;
}
.addBtn {
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
  margin-top: 30px;
  align-self: center;
}
.btn-container {
  display: flex;
  justify-content: center;
  margin-inline: 0;
}
.inputs {
  display: flex;
  flex-direction: row;
  margin-top: 20px;
  gap: 10px;
  align-items: center;
  justify-content: center;
}
.input-holder {
  display: flex;
  flex-direction: column;
  gap: 5px;
}
label {
  font-family: "Open-sans", sans-serif;
  font-size: 20px;
  font-weight: 400;
  line-height: 27.24px;
  margin-inline: 0;
}
.input {
  width: 442px;
  height: 45px;
  border: 1px solid #ffffff;
  box-shadow: 0px 4px 4px 0px #00000040;
  border-radius: 4px;
  align-self: center;
  outline: none;
  line-height: 43.58px;
  margin-inline: 0;
}
@media screen and (max-width: 768px) {
  .add {
    font-size: 24px;
    margin-bottom: 20px;
    margin-top: -70px;
    margin-inline: 80px;
  }
  label {
    font-size: 12px;
    margin-inline: 10px;
  }
  .inputs {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
  }
  .input {
    width: 357px;
    height: 36px;
    margin-inline: 10px;
  }
  .btn-container {
    justify-content: flex-start;
    line-height: 22px;
    margin-inline: 120px 0;
  }
  .addBtn {
    height: 34px;
    width: 116px;
    border: none;
    outline: none;
    font-size: 16px;
    font-weight: 700;
    align-self: flex-start;
  }
}
</style>