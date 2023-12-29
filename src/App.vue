<script>
import { RouterLink, RouterView } from "vue-router";
import HeaderComponent from "./components/HeaderComponent.vue";
export default {
  components: {
    HeaderComponent,
  },
  name: "app",
  data() {
    return {
      mobile: false,
      mobileNav: null,
      windowWidth: null,
      myPage: false,
    };
  },

  created() {
    window.addEventListener("load", this.checkScreen);

    window.addEventListener("resize", this.checkScreen);
  },

  methods: {
    toggleMobileView() {
      this.mobileNav = !this.mobileNav;
    },
    toggleNavView() {
      this.myPage = !this.myPage;
    },
    removeMobileView() {
      if (this.mobileNav == true) {
        return (this.mobileNav = false);
      } else {
        return (this.mobileNav = false);
      }
    },
    checkScreen() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 750) {
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
    },
  },
};
</script>


<template>
  <div class="page-container">
    <div @click="toggleNavView(myPage)" class="header">
      <HeaderComponent />

      <div>
        <nav>
          <div>
            <div class="menu" @click="toggleMobileView" v-show="mobile">
              <div :class="{ line1: mobileNav }"></div>
              <div :class="{ line2: mobileNav }"></div>
              <div :class="{ line3: mobileNav }"></div>
            </div>
          </div>
          <transition name="mobile-nav">
            <ul v-show="mobileNav" class="mobileN">
              <li><RouterLink to="/">Planner</RouterLink></li>
              <li><RouterLink to="/">Historik</RouterLink></li>
              <li><RouterLink to="/">Tips</RouterLink></li>
              <li>
                <RouterLink class="link" v-show="!myPage" to="/mypages"
                  >Logga in</RouterLink
                >
              </li>
              <li>
                <RouterLink class="link2" v-show="myPage" to="/mypages"
                  >Logga ut</RouterLink
                >
              </li>
            </ul>
          </transition>

          <ul v-show="!mobile" class="nav-links">
            <li><RouterLink class="link" to="/">Planner</RouterLink></li>
            <li><RouterLink to="/">Historik</RouterLink></li>
            <li><RouterLink to="/">Tips</RouterLink></li>
            <li>
              <RouterLink v-show="!myPage" to="/mypages">Logga in</RouterLink>
            </li>
            <li>
              <RouterLink class="link2" v-show="myPage" to="/mypages"
                >Logga ut</RouterLink
              >
            </li>
          </ul>
        </nav>
      </div>
    </div>

    <RouterView />
  </div>
</template>


<style scoped>
.mobile-nav-enter-active,
.mobile-nav-leave-active {
  transition: 1s ease all;
}

.mobile-nav-enter-from,
.mobile-nav-leave-to {
  transform: translateX(750px);
}
.mobile-nav-enter-to {
  transform: translateX(0);
}
.menu {
  height: 30px;
  width: 40px;
  margin-top: -400px;
}
.menu div {
  display: block;
  z-index: 9999;
  width: 40px;
  box-shadow: 0px 4px 4px 0px #00000040;

  height: 6px;
  background-color: #fff;
  margin: 5px;
  border-radius: 9px;
  transition: all 0.3s ease;
  cursor: pointer;
  transition: 0.8s ease all;
}
.mobileN {
  display: flex;
  flex-direction: column;
  height: 100%;
  z-index: 9999;
  width: 200px;
}
.line1 {
  transform: rotate(-45deg) translate(-6px, 6px);
}
.line2 {
  opacity: 0;
}
.line3 {
  transform: rotate(45deg) translate(-5px, -6px);
}
.page-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.header {
  display: flex;
  flex-direction: column;
  width: 1200px;
  align-items: center;
  justify-content: center;
}
.headerReverse {
  display: flex;
  flex-direction: column;
  width: 1200px;
  align-items: center;
  justify-content: center;
}

.nav-links {
  width: 1001px;
  z-index: 9999;
  align-items: center;
  background-color: #fff;
  box-shadow: 0px 4px 4px 0px #03382f1c;
  height: 60px;
}
ul {
  display: flex;
  list-style: none;
  text-decoration: none;
  width: 1001px;
  justify-content: center;

  gap: 150px;
  align-items: center;
}

.link {
  margin-inline: 150px 0;
}
.link2 {
  margin-inline: -150px 150px;
}
nav a {
  white-space: nowrap;
  color: #055647;
  font-weight: 500;
  text-transform: uppercase;
  font-family: "Maven Pro", sans-serif;
  font-size: 20px;
}
a:hover {
  background-color: transparent;
}
</style>
