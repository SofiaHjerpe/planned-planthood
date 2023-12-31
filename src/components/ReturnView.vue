<template>
  <div class="return">
    <a href="#start">Till toppen av sidan</a>
  </div>
</template>
<style scoped>
.return {
  display: flex;
  justify-content: center;
  align-items: center;
}
a {
  color: #000;
  font-family: "Open-sans", sans-serif;
  font-weight: 400;
  padding: 20px;
  font-size: 20px;
  margin: 0;
}
a:hover {
  background: none;
  background-color: transparent;
}
@media screen and (max-width: 768px) {
  .return {
    display: block;
    height: 60px;
  }
  a {
    padding: 130px;
    font-size: 12px;
    position: relative;
   top: 15px;

  }
}
</style>
