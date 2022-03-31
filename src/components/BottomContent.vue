<template>
<div class="bottom-content-wrapper">
  <div class="bottom-content-up">
    <div class="bottom-content-text"> Feel the excellent wet braking with Driveways!</div>
    <div class="bottom-content-link">
    <button class="bottom-content-button">
      WATCH ALL VIDEOS
    </button> </div>
  </div>
  <div class="bottom-content-down">
    <img src="../assets/video-demo.png" class="demo-image">
  <video>

  </video>


  </div>
</div>
</template>

<script>
export default {
  name: "BottomContent.vue"
}
</script>

<style scoped>
.bottom-content-wrapper {
  width: 100%;
  height: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: #434448;
}

.bottom-content-up {
  width: auto;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  margin: 32px;
  padding: 32px;
  flex-wrap: wrap;
}

.demo-image {
  max-width: 100%;
}

.bottom-content-text {
  color: white;
  font-family: 'Sora', sans-serif;
  font-weight: 700;
  font-size: 40px;
  margin-right: 12px;
}

.bottom-content-button {
  color: #ED1C24;
  background: white;
  font-family: 'Sora', sans-serif;
  font-weight: 700;
  font-size: 16px;
  padding: 16px 72px;
  white-space: nowrap;
}

.bottom-content-down {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  max-width: 100%;
}
</style>