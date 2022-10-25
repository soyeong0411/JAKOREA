<template>
  <div class="container supportWrap">
    <div class="supportTxt">
        <div class="sTxt"  data-aos="fade-up" data-aos-duration="1500">
            <p>국내외 여러기업이 동참하고 있습니다.</p>
            <h1>JA Korea 후원</h1>
        </div>
        <div class="slideBtn"  data-aos="fade-up" data-aos-duration="2000">
            <a href="#">자세히 보기 →</a>
        </div>
    </div>
    <div class="supportSwiper" data-aos="fade-up" data-aos-duration="1500">
        <swiper :modules="modules2" v-bind="swiperOptions2" class="mySwiper2">
            <swiper-slide v-for="(item,i) in support" :key="i">
                <img :src="`./images/09support/${support[i].src}`" alt="">
            </swiper-slide>
        </swiper>
        <div class="swiper-btn">
            <div class="next"><img src="../assets/right.png" alt=""></div>
            <div class="prev"><img src="../assets/left.png" alt=""></div>
        </div>
    </div>
    
  </div>
  
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";
  
  // Import Swiper styles
  import "swiper/css";
  
  import "swiper/css/grid";
  import "swiper/css/navigation";
  import "swiper/css/pagination";
  
  // import required modules
  import { Navigation,Pagination,Grid } from "swiper";

  import swiperData from "@/data/09support.js";

export default {
    props:[
        "support"
    ],
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules2: [Navigation,Pagination,Grid],
        swiperData: swiperData,
        swiperOptions2:{
            loop:true,
            slidesPerView: 3,
            grid: {
            rows: 3,
            },
            spaceBetween: 15,
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
    .supportWrap{
        display: flex;
        justify-content: center;
        padding: 80px 0;
        position: relative;
        .sTxt{
            width: 300px;
        }
        .supportSwiper{
        width: 900px;
        height: 400px;
        margin-left: 130px;
        .swiper {
            width: 100%;
            height: 100%;
            margin-left: auto;
            margin-right: auto;
            .swiper-slide {
                text-align: center;
                font-size: 18px;
                background: #fff;
                height: calc((100% - 50px) / 3) !important;
                display: flex;
                justify-content: center;
                align-items: center;
                background: rgb(213, 213, 213);
                border-radius: 20px;
                    img{
                        width: 50%;
                    }
                }
            }
            .swiper-pagination-bullet{
                display: none;
            }
        }
        .swiper-btn{
            cursor: pointer;
            .next{
            position:absolute;
            z-index: 1;
            width: 26px;
            right: -50px;
            bottom: 200px;
        }
        .prev{
            position:absolute;
            z-index: 1;
            width: 26px;
            left: -50px;
            bottom: 200px;
        }
        }
        

    }
    




    
    




</style>