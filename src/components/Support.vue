<template>
  <div class="container supportWrap">
    <div class="supportTxt">
        <div class="sTxt">
            <p>국내외 여러기업이 동참하고 있습니다.</p>
            <h1>JA Korea 후원</h1>
        </div>
        <div class="slideBtn">
            <a href="#">자세히 보기 →</a>
        </div>
    </div>

    <div class="supportSwiper">
        <swiper :modules="modules2" v-bind="swiperOptions2" class="mySwiper2">
            <swiper-slide v-for="(item,i) in 9" :key="i">
                <ul>
                    <li><img :src="`./images/09support/${support[i].src}`" alt=""></li>
                </ul>
            </swiper-slide>
            <swiper-slide v-for="(item,i) in 9" :key="i">
                <ul>
                    <li><img :src="`./images/09support/${support[i].src}`" alt=""></li>
                </ul>
            </swiper-slide>
            <!-- <swiper-slide v-for="item in support" :key="item">
                <h4>{{item.title}}</h4>
                <p v-html="item.subtitle"></p>
            </swiper-slide>
            <swiper-slide v-for="item in support" :key="item">
                <h4>{{item.title}}</h4>
                <p v-html="item.content"></p>
            </swiper-slide> -->

            <div class="swiper-btn">
                <div class="next"><img src="../assets/next.png" alt=""></div>
                <div class="prev"><img src="../assets/prev.png" alt=""></div>
            </div>
        </swiper>
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
  
  // import required modules
  import { Navigation,Pagination } from "swiper";
export default {
    props:[
        "support"
    ],
    
}
</script>

<style>
    img{
        width: 30px;
    }
</style>