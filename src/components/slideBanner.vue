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
        .slideLeft{
            position: absolute;
            top: 50%;left:100px;
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
            top: 230px;left:0;
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
// @media (max-width: 1199px){
//     h1{
//     font-size: 40px !important;
//     }
//     .slideLeft{
//         left: 70px !important;
//         .mainTitle{
//                 font-size:30px !important;
//                 margin-bottom: 15px;
//             }
//             .subTitle{
//                 font-size: 15px !important;
//             }
//     }
//     .slideImg{
//         &.img0{
//             width:300px !important;
//             top: 70px !important;
//         }
//         &.img1{
//             width:350px !important;
//             top: 70px !important;
//         }
//         &.img2{
//             width:280px !important;
//             right: 50px !important;
//         }
//         &.img3{
//             width:320px !important;
//             right: 50px !important;
//             top: 40px !important;
//         }
//     }
// }
// @media (max-width: 991px){
//     h1{
//     font-size:36px !important;
//     }
//     .slideLeft{
//         left: 30px !important;
//         .mainTitle{
//                 font-size:30px !important;
//                 margin-bottom: 15px;
//             }
//             .subTitle{
//                 font-size: 14px !important;
//             }
//     }
//     .slideImg{
//         &.img0{
//             right: 50px !important;
//         }
//         &.img1{
//             right: 50px !important;
//             width:320px !important;
//         }
//         &.img2{
//             width:250px !important;
//             right: 50px !important;
//         }
//         &.img3{
//             width:250px !important;
//             right: 50px !important;
//             top: 40px !important;
//         }
// }
// }
// @media (max-width: 767px){
//     .slideLeft{
//         left: 30px !important;
//         top: 150px !important;
//         .mainTitle{
//                 font-size:26px !important;
//                 margin-bottom: 15px;
//             }
//     }
//     .slideBtn{
//         top: 150px !important;
//         }
//         .slideImg{
//             display: none;
//         }
//         }


       
</style>