<template>
    <div class="visual" id="visual">
        <div class="container">
            <div class="row">
                <swiper :modules="modules" v-bind="swiperOptions" class="mySwiper px-0">
                    <swiper-slide v-for="(item,i) in swiperData" :key="item" class="slide">
                        <div class="slideCon">
                            <div class="slideText">
                                <div class="main_title" v-html="item.mainTitle"></div>
                                <div class="sub_title" v-html="item.subtitle"></div>
                            </div>
                            <div class="slideBtn">
                                <a href="#">자세히 보기 →</a>
                            </div>
                            <div class="slideVideo" :class="`video${i}`">
                                <video class="main_video" :src="`./images/01mainSlide_video/${item.mVideo}`" autoplay muted loop></video>
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
  
  // import required modules
  import { Navigation,Pagination } from "swiper";
  
  // import swiper data
  import swiperData from "@/data/01mainSlide.js";

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Navigation,Pagination],
        swiperData: swiperData,
        swiperOptions:{
            loop:true,
            navigation:{
                nextEl:'.visual .next',
                prevEl:'.visual .prev',
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
    #visual{
        background: #e1eff2;
        height: 745px;
        position: relative;
        .slide{
            width: 100%;height: 745px;
            overflow: hidden;
            .slideCon{
                .slideText{
                    position: absolute;
                    bottom: 50%;left: 50px;
                    z-index: 1;
                    .main_title{
                        font-size: 56px;
                        color:#285f74;
                        font-weight: 300;
                        span{
                            font-weight: 800;
                        }
                    }
                    .sub_title{
                        font-size: 18px;
                        color:#285f74;
                        font-weight: 600;
                        margin-top: 20px;
                    }
                }
                .slideBtn{
                    width: 200px;height: 60px;
                    background: #fff;
                    font-size: 17px;
                    font-weight: 600;
                    border-radius: 50px;
                    position: absolute;
                    bottom: 200px;left: 50px;
                    box-shadow: 1px 1px 20px rgba(0,0,0,0.2);
                    a{
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        height: 100%;
                    }
                }
                .slideVideo{
                    position: absolute;
                    right:-20px;top: 0;
                    width: 800px;height: 100%;
                    &.video1{
                        width: 900px;
                    }
                    .main_video{
                        width: 100%;height: 100%;
                    }
                }
            } 
        }
        .swiper-btn{
            position: absolute;bottom: 130px;
            z-index: 1;
            cursor: pointer;
            .prev{
                position: absolute;
                left: 60px;
                img{
                    width: 14px;
                }
            }
            .next{
                position: absolute;
                left: 160px;
                img{
                    width: 14px;
                }
            }
        }
        .swiper-pagination{
            position: absolute;
            left: 110px;bottom: 112px;
            .swiper-pagination-bullet{
                background: #285f74;
                width: 10px;height: 10px;
            }
        }
    }

    @media (max-width: 1199px){
            .slideText{
                    top: 50px;
                    .main_title{
                        font-size: 40px !important;
                    }
                }
            .slideVideo{
                width: 600px !important;
                top: 80px !important;
                &.video1{
                    width: 700px !important;
                    bottom: 20px !important;
                }
            }
            .slideBtn{
                width: 130px;height: 50px;
                top: 300px;
                z-index: 1;
            }   
        }
        
    @media (max-width: 767px){
        .slideText{
                    top: 50px;
                    .main_title{
                        font-size: 30px !important;
                    }
                    .sub_title{
                        font-size: 16px !important;
                    }
                }
        .slideBtn{
            width: 120px !important;height: 30px !important;
            font-size: 12px !important;
            top: 230px;
        }
        .slideVideo{
            right: -40px !important;
            top: 100px !important;
            &.video1{
                width: 600px !important;
            }
        }
        .swiper-btn{
            .prev{
                left: calc(50% - 40px) !important;
                bottom: -116px;
                img{
                    width: 12px !important;
                }
            }
            .next{
                left: calc(50% + 40px) !important;
                bottom: -116px;
                img{
                    width: 12px !important;
                }
            }
        }
        .swiper-pagination{
            left: 50% !important;
            bottom: 20px !important;
        }
    }


</style>