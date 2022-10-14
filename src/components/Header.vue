<template>
  <header class="header">
    <div class="container">
        <div class="row">
            <div class="headerWrap">
                <h1><a href="#"><img src="../assets/new_logo.svg" alt=""></a></h1>
                <div class="menuWrap">
                    <div class="top_menu">
                        <nav class="icon_menu">
                            <ul>
                                <li v-for="item in iconData" :key="item">
                                    <a href="#"><img :src="`./images/${item}`" alt=""></a>
                                </li>
                            </ul>
                        </nav>
                        <div class="toggle">
                            <div class="lineWrap">
                                <div class="line"></div>
                            </div>
                        </div>
                    </div>
                    <nav class="main_menu">
                        <ul>
                            <li v-for="item in menuData" :key="item">
                                <a href="#">{{item}}</a>
                            </li>
                        </ul>
                    </nav>  
                </div>
            </div>
        </div>
    </div>
  </header>
</template>

<script>
export default {
    data(){
        return {
            menuData:["제이에이코리아","투명경영","교육사업","기관소식","후원하기"],
            iconData:["search.png","user.png","facebook.png","instagram.png","youtube.png"]
        }
    }
}

</script>

<style lang="scss">

    .headerWrap{
        display: flex;
        padding: 20px 0;
        img{
        width: 218px;
        }
        .menuWrap{
            margin-left: auto;
            .top_menu{
                display: flex;
                justify-content: end;
                gap:15px;
                .icon_menu{
                    ul{
                        display: flex;
                        height: 100%;
                        gap:15px;
                        img{
                        width: 22px;
                        }
                    }
                }
                .toggle{
                    display: none;
                    cursor: pointer;
                    .lineWrap{
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        position: relative;
                        width: 25px;height: 25px;
                            .line{
                            width: 20px;height: 1px;
                            background: #000;  
                            border-radius: 10px;
                            &::before,&::after{
                                content: "";display: block;
                                width: 20px;height: 1px;
                                background: #000;  
                                border-radius: 10px;
                                position: absolute;
                                transform: translateY(-5px);
                                }
                                &::after{
                                    transform: translateY(5px);
                                }
                            }
                        }   
                    } 
                }
            .main_menu{
                ul{
                    display: flex;
                    height: 100%;
                    gap:70px;
                    li{
                        height: 100%; 
                        a{
                            display: flex;
                            justify-content: center;
                            align-items: center;
                            height: 100%;
                            font-size: 20px;
                            font-weight: bold;
                        }
                    }
                }
            }
        }
    }

    @media (max-width: 1199px){
        .headerWrap{
            padding: 15px 0;
            img{
                width: 170px;
            }
            .menuWrap{
                display: flex;
                align-items: center;
                .top_menu{
                    .icon_menu{
                        li{
                            display: flex;
                            align-items: center;
                            &:nth-child(1){
                                display: none;
                            }
                            &:nth-child(2){
                                display: none;
                            }
                        }
                    }
                    .toggle{
                        display: flex;
                        align-items: center;
                    }
                }
                .main_menu{
                    display: none;
                }   
            }    
        }
    }


</style>