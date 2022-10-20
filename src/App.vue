<template>
  <Header></Header>
  <main-visual></main-visual>
  <IconBanner></IconBanner>
  <SlideBanner></SlideBanner>
  <NumberCount></NumberCount>
  <TabSwiper :notice="notice" :story="story" :news="news"></TabSwiper>
  <Notice :notice="noticeCon" :result="result"></Notice>
  <JaVideo></JaVideo>
  <Support :support="support"></Support>
</template>

<script>
import Header from "./components/Header.vue"
import MainVisual from './components/MainVisual.vue'
import IconBanner from './components/IconBanner.vue'
import SlideBanner from "./components/slideBanner.vue";
import TabSwiper from "./components/TabSwiper.vue";
import NumberCount from "./components/NumberCount.vue"
import Notice from './components/Notice.vue'
import JaVideo from "./components/JaVideo.vue";
import Support from './components/Support.vue';

import notice from "@/data/04notice.js"
import story from "@/data/05story.js"
import news from "@/data/06news.js"
import noticeCon from '@/data/07notice.js';
import result from '@/data/08result.js';
import support from '@/data/09support.js'






export default {
  components:{
    Header,
    MainVisual,
    IconBanner,
    SlideBanner,
    TabSwiper,
    NumberCount,
    Notice,
    JaVideo,
    Support
},
  data(){
    return {
      notice:notice,
      story:story,
      news:news, 
      noticeCon:noticeCon,
      result:result,
      support:support,
    }
  }
}
</script>

<style>

@import url(./assets/style.css);

</style>
