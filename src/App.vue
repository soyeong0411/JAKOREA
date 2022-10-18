<template>
  <Header></Header>
  <main-visual></main-visual>
  <IconBanner></IconBanner>
  <SlideBanner></SlideBanner>
</template>

<script>
import Header from "./components/Header.vue"
import MainVisual from './components/MainVisual.vue'
import IconBanner from './components/IconBanner.vue'
import SlideBanner from "./components/slideBanner.vue";


export default {
  components:{
    Header,
    MainVisual,
    IconBanner,
    SlideBanner
}
}
</script>

<style>

@import url(./assets/style.css);

</style>
