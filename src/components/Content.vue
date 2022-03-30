<template>
  <div class="dealer-slider-wrapper">
    <div class="upside-dealer">
      <div class="slider-title">
        Featured Products
      </div>
    </div>
    <div class="lowside-dealer">
      <div class="dealer-options" v-for="dealer in dealers" :key="dealer.index">
        <div class="dealer-upper">
          <div class="dealer-title">
           <h3>{{dealer.title}}</h3>
          </div>
          <div class="dealer-text">
            {{dealer.text}}
          </div>
        </div>
        <div class="dealer-lower">
          <button class="left-button">
            LEARN MORE
          </button>
          <button class="right-button">
            FIND A DEALER
          </button>
        </div>

      </div>
    </div>

  </div>
</template>

<script>

export default {
  name: "Content.vue",
  data() {
    return {
      dealers: [
        {title: "ICEWAYS", text: "City life is changing. So are the habits of urban citizens. 4X4 cars that were previously used only on challenging lands are now preferred for urban use."},
        {title: "DRIVEWAYS SPORT", text: "Driveways is a ‘’Comfort tyre’’ developed for a considerably wide vehicle pool ranging from middle class sedans to upper class comfort automobiles."},
        {title: "DRIVEWAYS COMPETUS H/P", text: "City life is changing. So are the habits of urban citizens. 4X4 cars that were previously used only on challenging lands are now preferred for urban use."}
      ]
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Sora:wght@400;600;700&display=swap');
.dealer-slider-wrapper {
  background: #F9F6F6;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 1rem;
  align-items: center;
}

.lowside-dealer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 1rem;
  padding: 1rem;
}
.dealer-options {
  border: 1px solid #E0D8D7;
  background: white;
  margin: 1rem;
  border-bottom: 4px solid red;
  border-radius: 2px;
}
.dealer-lower {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  width: 100%;
  margin: 24px 0 8px 0;
}

.dealer-title {
  margin: 24px;
  font-family: 'SORA';
}

.dealer-text {
  margin: 24px;
  font-family: 'SORA';
 font-weight: 400;
}

.slider-title {
  font-size: 32px;
  color: #400E03;
  font-weight: bold;
  font-family: 'Sora', sans-serif;
}

.left-button {
  background-color: #FDE4E5;
  color: #ED1C24;
  border: none;
  padding: 16px;
  width: 40%;
  font-size: 12px;
  font-weight: bold;
  border-radius: 4px;
  font-family: 'SORA';
}

.right-button {
  background-color: #ED1C24;
  font-size: 12px;
  font-weight: bold;
  color: white;
  width: 40%;
  padding: 16px;
  border: none;
  border-radius: 4px;
  font-family: 'SORA';
}
</style>