<template>
  <div class="app-wrapper">
    <Header></Header>
     <Hero></Hero>
    <div class="content-wrapper">
      <Content></Content>
    </div>
    <div class="bottom-content">
      <BottomContent></BottomContent>
    </div>
  </div>
</template>

<script>

import Content from "@/components/Content";
import Header from "@/components/Header";
import Hero from "@/components/Hero";
import BottomContent from "@/components/BottomContent";
export default {
  name: 'App',
  components: {
    Content,
    Hero,
    Header,
    BottomContent,
  }
}
</script>

<style>
.app-wrapper {
  max-width: 1400px;
  margin: 36px;
}


</style>
