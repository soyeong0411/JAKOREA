<template>
  <div class="slideBan" data-aos="fade-up" data-aos-duration="1500">
        <div class="container">
            <h1>JA 교육 프로그램</h1>
            <div class="swiperWrap">
                <swiper :modules="modules" v-bind="swiperOptions" class="mySwiper px-0">
                    <swiper-slide v-for="(item,i) in swiperData" :key="i" class="slide">
                        <div class="slideCon">
                            <div class="slideLeft">
                                <div class="slideText">
                                    <div class="mainTitle" v-html="item.title"></div>
                                    <div class="subTitle" v-html="item.subtitle"></div>
                                </div>
                                <div class="slideBtn">
                                    <a href="#">자세히 보기 →</a>
                                </div>
                            </div>
                            <div class="slideImg" :class="`img${i}`">
                                <img :src="`./images/03eduProgram/${item.src}`" alt="">
                            </div>
                        </div>
                    </swiper-slide>
                    <div class="swiper-btn">
                        <div class="next"><img src="../assets/right.png" alt=""></div>
                        <div class="prev"><img src="../assets/left.png" alt=""></div>
                    </div>
                </swiper>
                
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

  AOS.init();
  </script>

<style lang="scss" scoped>
.slideBan{
    position: relative;
    width: 100%;
    padding: 20px 0 80px 0;
    h1{
    font-size: 46px;
    }
    .slideCon{
        display: flex;
        height: 500px;
        position: relative;
        padding-left: 100px;
        .slideLeft{
            position: absolute;
            top: 50%;
            transform: translateY(-100%);
            
            .mainTitle{
                font-size: 35px;
                margin-bottom: 15px;
            }
            .subTitle{
                font-size: 18px;
            }
        .slideBtn{
            width: 200px;height: 50px;
            background: #fff;
            font-size: 17px;
            font-weight: 600;
            border-radius: 50px;
            position: absolute;
            top: 230px;
            left: 0;
            box-shadow: 1px 1px 20px rgba(0,0,0,0.2);
            a{
                display: flex;
                justify-content: center;
                align-items: center;
                height: 100%;
            }
        }
    }
    .slideImg{
        position: absolute;
        right: 200px;top: 0;
        &.img0{
            width:400px;
            right: 170px;
        }
        &.img1{
            width:500px;
            position: absolute;
            right: 120px;
        }
        &.img2{
            width:350px;
            position: absolute;
            right: 150px;
        }
        &.img3{
            width:420px;
            position: absolute;
            right: 100px;
        }
    img{
    width: 100%;
    }
}

}
.swiper-btn{
        cursor: pointer;
        .prev{
            position: absolute;
            left: 20px;top: 50%;
            z-index: 1;
            img{
                width: 34px;
            }
        }
        .next{
            position: absolute;
            right: 20px;top: 50%;
            z-index: 1;
            img{
                width: 34px;
            }
        }
    }

}

@media (max-width: 991px){
   .slideImg{
    display: none;
   }
}
@media (max-width: 767px){
   .slideCon{
    padding-left: 50px !important;
    height: 300px !important;
        .slideLeft{
            .slideText{
                height: 400px;
                width: 400px;
                position: absolute;
                top: -120px;
                .mainTitle{
                    font-size: 26px;
                }
                .subTitle{
                    font-size: 16px;
                }
            }
        }
        .slideBtn{
            top: 80px !important;
        }
   }
    .swiper-btn .next{
        left: calc(50% + 205px) !important;
        bottom: -116px;
        img{
            width: 26px !important;
        }
    }
    .swiper-btn .prev{
        left: calc(50% - 205px) !important;
        img{
        width: 26px !important;
        }
    } 
    
}


       
</style>