<template>
  <Header></Header>
  <main-visual></main-visual>
  <IconBanner></IconBanner>
  <SlideBanner></SlideBanner>
  <NumberCount></NumberCount>
  <TabSwiper :notice="notice" :story="story" :news="news"></TabSwiper>
</template>

<script>
import Header from "./components/Header.vue"
import MainVisual from './components/MainVisual.vue'
import IconBanner from './components/IconBanner.vue'
import SlideBanner from "./components/slideBanner.vue";
import TabSwiper from "./components/TabSwiper.vue";
import NumberCount from "./components/NumberCount.vue"

import notice from "@/data/04notice.js"
import story from "@/data/05story.js"
import news from "@/data/06news.js"




export default {
  components:{
    Header,
    MainVisual,
    IconBanner,
    SlideBanner,
    TabSwiper,
    NumberCount,
},
  data(){
    return {
      notice:notice,
      story:story,
      news:news, 

    }
  }
}
</script>

<style>

@import url(./assets/style.css);

</style>
