<template>
  <div class="iconBanner">
    <div class="container">
        <div class="row">
            <ul>
                <li v-for="item in iconData" :key="item" data-aos="fade-up" data-aos-duration="2000" >
                    <a href="#"><img :src="`./images/02iconBanner/${item.src}`" alt=""></a>
                    <a href="#"><h5 v-html="item.title"></h5></a>
                    <a href="#"><p v-html="item.subtitle"></p></a>
                </li>
            </ul>
        </div>
    </div>
  </div>
</template>

<script>
import iconData from "@/data/02iconBanner.js"

export default {
    data(){
        return {
            iconData:iconData,
        }
    },
}

AOS.init();
</script>

<style lang="scss" scoped>
    ul{
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 50px 0;
        li{
            img{
                width: 160px;
                height: 200px;
            }
            h5{
                font-weight: bold;
                text-align: center;
                margin-bottom: 15px;
            }
            p{
                text-align: center;
            }
        }
    }
    @media (max-width: 991px){
        ul{
            flex-wrap: wrap;
            li{
                display: flex;
                flex-direction: column;
                align-items: center;
                img{
                width: 130px !important;
                height: 150px !important;
            }
                
            }
            
        }
    }

    @media (max-width: 767px){
        h5{
            font-size: 18px;
        }
        p{
            font-size: 15px;
        }
            
    }


</style>