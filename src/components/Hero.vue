<template>
<div class="hero-wrapper">
  <img class="img-wrapper" src="../assets/2022-infiniti-q50-sedan-side-mirror.jpg" :style="{ 'heigth' : '10px'}">
  <h2 class="hero-title">
    Nothing can stop you

  </h2>
  <button class="hero-button">
    FIND OUT MORE
  </button>

</div>
</template>

<script>
export default {
  name: "Hero.vue"
}
</script>

<style scoped>

.hero-wrapper {

  background-repeat: no-repeat;
  background-size: contain;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.hero-title {
  font-size: 4rem;
  color: white;
  width: 29rem;
  text-align: center;
  flex: 1;
  position: absolute;
}

.img-wrapper {
  flex: 1;
  position: relative;
  width: 100%;
}
.hero-button {
  position: absolute;
  height: 2rem;
}
</style>