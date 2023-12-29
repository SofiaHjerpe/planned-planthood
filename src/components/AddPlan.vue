<template>
  <h2 class="add">Lägg till ny planering:</h2>
  <div class="inputs">
    <div style="display: flex; flex-direction: column">
      <label for="name">Planta:</label>
      <input type="text" name="planta" id="name" />
    </div>
    <div style="display: flex; flex-direction: column">
      <label for="date">Datum:</label>
      <input type="date" name="date" id="date" />
    </div>
  </div>
</template>
<style scoped>
.add {
  margin-top: 0;
  color: #060606;
  font-weight: 400;
  font-size: 32px;
  font-family: "Open-sans", sans-serif;
}
.inputs {
  display: flex;
  flex-direction: row;
  gap: 40px;
}
</style>