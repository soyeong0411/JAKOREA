<template>
  <swiper :modules="modules1" v-bind="swiperOptions1" class="mySwiper1">

    <swiper-slide v-if="tab==1" v-for="item in notice" :key="item">
        <h4>{{item.title}}</h4>
        <p v-html="item.content"></p>

    </swiper-slide>

    <swiper-slide v-if="tab==2" v-for="item in story" :key="item">
        <h4>{{item.title}}</h4>
        <p v-html="item.subtitle"></p>
    </swiper-slide>

    <swiper-slide v-if="tab==3" v-for="item in news" :key="item">
        <h4>{{item.title}}</h4>
        <p v-html="item.content"></p>
    </swiper-slide>

  </swiper>  
    <div class="swiper-btn">
        <div class="next"><img src="../assets/next.png" alt=""></div>
        <div class="prev"><img src="../assets/prev.png" alt=""></div>
    </div>
</template>

<script>

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/navigation";
import "swiper/css/pagination";

// import required modules
import { Navigation,Pagination } from "swiper";

export default {
    props:[
        "notice",
        "story",
        "news",
        "tab",
    ],
    components: {
      Swiper,
      SwiperSlide,
    },

    setup() {
      return {
        modules1: [Navigation,Pagination],
        swiperOptions1:{
            slidesPerView:3,
            spaceBetween:30,
            loop:true,
            observer: true,
            observeParents: true,
            navigation:{
                nextEl:'.next',
                prevEl:'.prev',
            },
            pagination:{
                dynamicBullets: true,
                clickable:true,
            }
        }
    };
    },
}
</script>

<style lang="scss">
.mySwiper1{
    height: 300px;
}

</style>