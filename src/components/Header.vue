<template>
<div class="header-wrapper">
  <div class="header-left">
    <div class="header-icon">
      <img src="../assets/logo.png">
    </div>
    
  </div>
  <div class="header-right">
    <div class="navigation-wrapper" v-for="link in links" :key="link.id">
      {{link.title}}
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: "Header.vue",
  data() {
    return {
      links: [
        {id: 1, title: "SHOW ALL TYRES"},
        {id: 2, title: "FIND A DEALER"},
        {id:3, title: "GUIDES & VIDEOS"},
        {id: 4, title: "GO WITH"},
        {id: 5, title: "SERVICE & HELP"}
      ]
    }
  }
}
</script>

<style scoped>

.header-wrapper {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
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
  width: 50%;
  justify-content: space-between;
}
.header-icon {
  margin-right: 1rem;
}
</style>