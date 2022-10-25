<template>
  <div class="footWrap">
    <div class="container">
        <div class="footTop">
            <ul>
                <li><a href="#">이용약관</a></li>
                <li><a href="#">개인정보처리방침</a></li>
                <li><a href="#">이메일수집거부</a></li>
                <li><a href="#">오시는길</a></li>
            </ul>
            <select name="site" class="site">
                <option value="0">관련 사이트보기</option>
                <option value="1">JA Worldwide</option>
                <option value="2">JA Africa</option>
                <option value="3">JA Worldwide</option>
            </select>
        </div>
        
    </div>
  </div>
  <div class="footBottom container">
        <div class="foot_menu">
            <ul>
                <li><a href="#">후원하기</a></li>
                <li><a href="#">온라인 학습관리</a></li>
                <li><a href="#">기부금영수증</a></li>
                <li><a href="#">국세청 공시 및 공개 내역</a></li>
                <li><a href="#">1:1 문의</a></li>
            </ul>
            <div class="footIcon">
                <p>Follow SNS</p>
                <div class="icon">
                    <img src="../assets/facebook_g.png" alt="">
                    <img src="../assets/instagram_g.png" alt="">
                    <img src="../assets/youtube_g.png" alt="">
                </div>
            </div>
        </div>
        <div class="foot_info">
            <h1><a href="#"><img src="../assets/footer-logo.svg" alt=""></a></h1>
            <p>서울특별시 강서구 양천로 583, B동 1408호(염창동, 우림블루나인비즈니스센터) 사단법인 제이에이코리아    우편번호 : 07547    대표 : 이은형    사업자번호 : 107-82-10367<br>
                대표전화 : 02-783-2367    팩스 : 070-4275-5115    이메일 : jakorea@jakorea.org<br><br>
                ⓒJA Korea,2022</p>
        </div>
    </div>
    
</template>

<script>
export default {

}
</script>

<style lang="scss">
    .footWrap{
        background: rgb(233, 233, 233);
        margin-top: 100px;
        .footTop{
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 30px 0;
            ul{
                display: flex;
                align-items: center;
                padding-left: 0;
                margin-bottom: 0;
                a{
                display: flex;
                justify-content: center;
                align-items: center;
                padding: 0 20px;
                height: 100%;
                font-size: 18px;
            }

                
            }
            .site{
                width: 230px;height: 40px;
                border: 0 none;
                border-radius: 10px;
                text-indent: 15px;
                &:focus{
                outline:none;
            }
            }
        }
        
    }
    .footBottom{

        .foot_menu{
            display: flex;
            justify-content: space-between;
            padding: 15px 0;
            ul{
                display: flex;
                align-items: center;
                padding-left: 0;
                margin-bottom: 0;
                a{
                display: flex;
                justify-content: center;
                align-items: center;
                padding: 0 20px;
                height: 100%;
            }
            }
            .footIcon{
                color:#aaa;
                .icon{
                    display: flex;
                    gap:20px;
                    img{
                    width: 22px;
                }
                }
                
            }
            
        }
        .foot_info{
            padding: 20px 0;
            h1{
                img{
                width: 230px;  
                };
                }
            }
    }
    
    
</style>