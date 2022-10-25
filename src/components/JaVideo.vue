<template>
<div class="jaVideo">
    <video src="../assets/main-home.mp4" autoplay muted loop></video>
    <p class="title"  data-aos="fade-up" data-aos-duration="1500">우리 청소년들이 미래의 인재로 성장하도록</p>
    <h1  data-aos="fade-up" data-aos-duration="2000">JA KOREA가 함께합니다.</h1>
    <div class="slideBtn"  data-aos="fade-up" data-aos-duration="2500">
        <a href="#">자세히 보기 →</a>
    </div>
</div>                
</template>

<script>
export default {

}
</script>

<style lang="scss">
    .jaVideo{
        height: 100vh;
        width: 100%;
        overflow: hidden;
        position: relative;

            
            .title{
                font-size: 40px;
                background: #00a0af;
                position: absolute;
                left: 250px;top:400px;
                color:#fff;
            }
            h1{
                font-size: 74px;
                position: absolute;
                left: 250px;top:470px;
                color:#fff;
            }
        
        .slideBtn{
                    width: 200px;height: 60px;
                    background: #fff;
                    font-size: 17px;
                    font-weight: 600;
                    border-radius: 50px;
                    position: absolute;
                    bottom: 350px;left: 250px;
                    box-shadow: 1px 1px 20px rgba(0,0,0,0.2);
                    a{
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        height: 100%;
                    }
                }
    }

</style>