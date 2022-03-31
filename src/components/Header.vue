<template>

<div class="header-wrapper">
  <div class="header-left">
    <div class="header-icon">
      <img src="../assets/logo.png">
    </div>
  </div>
  <div class="header-right"  v-if="!isMobile">
    <div class="navigation-wrapper" v-for="link in links" :key="link.id" >
      {{link.title}}
    </div>
  </div>
  <div class="header-hamburger" v-if="isMobile">
      <Slide right class="hamburger-wrapper">
        <div  v-for="link in links" :key="link.id">
          <a id="home" href="#">
            <span class="hamburger-titles">{{link.title}}</span>
          </a>
        </div>

      </Slide>
  </div>
</div>
</template>

<script>
import { Slide } from "vue-burger-menu";
export default {
  name: "Header.vue",
components: {
  Slide
},
  data() {
    return {
      isMobile: true,
      links: [
        {id: 1, title: "SHOW ALL TYRES"},
        {id: 2, title: "FIND A DEALER"},
        {id:3, title: "GUIDES & VIDEOS"},
        {id: 4, title: "GO WITH"},
        {id: 5, title: "SERVICE & HELP"}
      ]
    }
  },
  methods: {
    screenCheck() {
      let width = (window.innerWidth > 0) ? window.innerWidth : screen.width;
      if(width > 1260){
        return this.isMobile = false;
      } else {
        return this.isMobile = true;
      }
    }
  },
  beforeMount() {
    this.screenCheck();
  }
}
</script>

<style scoped>

.header-wrapper {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  margin: 1rem 1rem;
}
.hamburger-titles {
  color: white;
  background-color: #400E03;
  border-bottom: 1px solid lightgrey;
}
#bm-menu {
  background-color: #400E03;
}

.header-left {
  display: flex;
  flex-direction: row;
  width: 50%;
  justify-content: flex-start;
}

.header-right {
  display: flex;
  flex-direction: row;
  width: 100%;
  justify-content: space-evenly;
}
.header-icon {
  margin-right: 1rem;
}

.navigation-wrapper {
  font-family: 'Sora', sans-serif;
  font-weight: 600;
  color: #400E03;
  font-size: 14px;

}
</style>