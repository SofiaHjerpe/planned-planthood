
<template>
  <div
    v-if="reverseComponent == false"
    :class="reverseComponent == true ? 'reverseItems' : 'originalItems'"
  >
    <div class="season-container">
      <div class="circle">
        <img :src="seedInfo[0].icon" class="seed" alt="seed" />
      </div>
      <div class="info-text">
        <div>
          <h2>{{ seedInfo[0].title }}</h2>
        </div>
        <div>
          <p>Våren är äntligen här i kollektivet!</p>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
          <p>Nesciunt laborum maiores dolorum possimus aliquid</p>
        </div>
        <div>
          <button class="sa-btn">{{ seedInfo[0].btnText }}</button>
        </div>
      </div>
    </div>
    <div class="line-container">
      <hr class="green-line" />
    </div>
  </div>

  <div v-if="reverseComponent == true">
    <div
      class="season-c"
      :class="reverseComponent == true ? 'reverseItems' : 'originalItems'"
    >
      <div class="circle">
        <img :src="seedInfo[1].icon" class="seed" alt="seed" />
      </div>
      <div class="info-text" style="margin-inline: 30px 0">
        <div>
          <h2>{{ seedInfo[1].title }}</h2>
        </div>
        <div>
          <p>Våren är äntligen här i kollektivet!</p>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
          <p>Nesciunt laborum maiores dolorum possimus aliquid</p>
        </div>
        <div>
          <button class="longBtn">{{ seedInfo[1].btnText }}</button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import seed from "../seed.js";
export default {
  props: {
    reverseComponent: Boolean,
  },
  data() {
    return {
      seedInfo: seed.seedInfo,
    };
  },
};
</script>
 <style scoped>
.line-container {
  display: flex;
  justify-content: center;
  bottom: 0;
}
.season-c {
  display: flex;
  justify-content: space-between;
  bottom: 0;
}
.season-container {
  display: flex;
  justify-content: space-between;
  bottom: 0;
}
.reverseItems {
  display: flex;
  justify-content: space-between;
  flex-direction: row-reverse;
}
.originalItems {
  display: flex;
  flex-direction: column;
  gap: 35px;
}
h2 {
  font-weight: 700;
  font-family: "Open-sans", sans-serif;
  font-size: 32px;
  margin-top: 120px;
  line-height: 44px;
  color: #1e1e1e;
  padding-inline: 0;
}
p {
  color: #000;
  font-family: "Open-sans", sans-serif;
  font-size: 16px;
  font-weight: 400;
  line-height: 22px;
  margin-inline: 0;
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
  margin-inline: 0;
  width: 179px;
  border: none;
  outline: none;
  font-family: "Open-sans", sans-serif;
  font-size: 24px;
  font-weight: 700;
  text-transform: uppercase;
  line-height: 32.68px;
  margin-top: 10px;
  margin-inline: 230px 30px;
}
.longBtn {
  box-shadow: 0px 4px 4px 0px #00000040;
  background-color: #0a846e;
  color: #fff;
  border-radius: 9px;
  height: 63px;
  width: 281px;
  border: none;
  outline: none;
  font-family: "Inter", sans-serif;
  font-size: 24px;
  font-weight: 600;
  line-height: 32.68px;
  margin-top: 10px;
  align-self: center;
}
.green-line {
  background-color: #055647;
  width: 303.24px;
  height: 3px;
  margin-bottom: 30px;
  margin-top: 100px;
}
@media screen and (max-width: 768px) {
  .line-container {
    max-width: 400px;
    margin-top: 0;
    position: relative;
    bottom: 100px;
  }

  .season-container {
    display: flex;
    flex-direction: column-reverse;
    justify-content: center;
    align-items: center;
    overflow-x: hidden;
    width: 408px;
    height: 590px;
    position: relative;
    margin-top: 0;
    bottom: 150px;
  }
  .season-c {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 408px;
    height: 590px;
  }

  h2 {
    font-size: 16px;
    align-self: center;
    padding-inline: 112px;
  }
  .season-c .info-text h2 {
    font-size: 16px;
    align-self: center;
    padding-inline: 80px;
  }

  p {
    font-size: 14px;
    align-self: center;
    line-height: 19px;
    margin-inline: 0 30px;
  }
  .sa-btn {
    width: 99px;
    height: 35px;
    font-size: 16px;
    align-self: center;
    margin-inline: 115px 0;
  }
  .longBtn {
    width: 179px;
    height: 35px;
    font-size: 16px;
    align-self: center;
    margin-inline: 70px 0;
  }
  .circle {
    width: 241px;
    height: 241px;
    margin-top: 30px;
    margin-inline: 0 30px;
    margin-bottom: 0;
  }
  .green-line {
    width: 202px;
    margin-top: 0;
  }
  .seed {
    width: 126px;
    height: 124px;
  }
  .info-text {
    align-items: flex-start;
    justify-content: flex-start;
  }
  .season-c .info-text {
    margin-top: -100px;
  }
}
</style>