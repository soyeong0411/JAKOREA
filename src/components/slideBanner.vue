<template>
  <div class="slideBan">
        <div class="container">
            <div class="row">
                <h1>JA 교육 프로그램</h1>
                <swiper :modules="modules" v-bind="swiperOptions" class="mySwiper px-0">
                    <swiper-slide v-for="(item,i) in swiperData" :key="item" class="slide">
                        <div class="slideCon">
                            <div class="slideLeft">
                                <div class="slideText">
                                    <div class="main_title" v-html="item.title"></div>
                                    <div class="sub_title" v-html="item.subtitle"></div>
                                </div>
                                <div class="slideBtn">
                                    <a href="#">자세히 보기 →</a>
                                </div>
                            </div>
                            <div class="slideImg">
                                <img :src="`./images/03eduProgram/${item.src}`" alt="">
                            </div>
                        </div>
                    </swiper-slide>
                </swiper>
                <div class="swiper-btn">
                    <div class="next"><img src="../assets/next.png" alt=""></div>
                    <div class="prev"><img src="../assets/prev.png" alt=""></div>
                </div>
            </div>
        </div>
    </div>
  </template>

  <script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from "swiper/vue";
  
  // Import Swiper styles
  import "swiper/css";
  
  import "swiper/css/navigation";
  import "swiper/css/pagination";
  import "swiper/css/effect-fade";
  
  // import required modules
  import { Navigation,Pagination,EffectFade } from "swiper";
  
  // import swiper data
  import swiperData from "@/data/03eduProgram.js";

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Navigation,Pagination,EffectFade],
        swiperData: swiperData,
        swiperOptions:{
            loop:true,
            effect: 'fade',
            fadeEffect: {
            crossFade: true
            },
            navigation:{
                nextEl:'.slideBan .next',
                prevEl:'.slideBan .prev',
            },
            pagination:{
                dynamicBullets: true,
                clickable:true,
            }
        }
    };
    },
  };
  </script>

<style lang="scss">
h1{
    font-weight: 800;
}
.slideCon{
    display: flex;
   height: 600px;
    position: relative;
    .slideImg{
        position: absolute;
        right: 0;top: 0;
    img{
    width: 400px;
    }
}

}

       
</style>