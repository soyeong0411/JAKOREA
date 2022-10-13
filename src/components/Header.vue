<template>
  <header class="header">
    <div class="container">
        <div class="row">
            <div class="headerWrap">
                <h1><a href="#"><img src="../assets/new_logo.svg" alt=""></a></h1>
                <div class="menuWrap">
                    <nav class="icon_menu">
                        <ul>
                            <li v-for="item in iconData" :key="item">
                                <a href="#"><img :src="`./images/${item}`" alt=""></a>
                            </li>
                        </ul>
                    </nav>
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
            .icon_menu{
                ul{
                    display: flex;
                    height: 100%;
                    img{
                        width: 24px;
                    }
                }
            }
        .main_menu{
            
            ul{
                display: flex;
                height: 100%;
                li{
                    height: 100%; 
                    a{
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        height: 100%;
                        padding: 0 40px;
                        font-size: 19px;
                        font-weight: bold;
                    }
                }
            }
        }
        }
        
    }


</style>