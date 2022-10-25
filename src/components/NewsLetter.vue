<template>
  <div class="container NewsWrap" data-aos="fade-up" data-aos-duration="1500">
    <h3>JA Korea 뉴스레터 구독하기</h3>
    <div class="insert">
        <div class="name">
            <img src="../assets/user_w.png" alt="">
            <input type="text" name="name" placeholder="이름" class="inp_name">
        </div>
        <div class="email">
            <img src="../assets/mail.png" alt="">
            <input type="text" name="email" placeholder="이메일 주소" class="inp_mail">
        </div>
        <div class="ins_btn">
            <a href="#">신청하기</a>
        </div>
    </div>
    <div class="check">
        <p>뉴스레터 구독을 위한 이름 및 이메일 주소 수집에 동의합니다.</p>
    </div>
    <img src="../assets/subscribe-img.png" alt="" class="r_img">
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.NewsWrap{
    background: #00a0af;
    padding: 50px;
    border-radius: 20px;
    position: relative;
    h3{
        color: #fff;
        font-weight: bold;
        margin-bottom: 30px;
    }
    .insert{
        display: flex;
        position: relative;
        gap:15px;
        .inp_name,.inp_mail{
            width: 330px;height: 50px;
            border-radius: 10px;
            background: #46ccd8;
            border: none;
            text-indent: 40px;
            &:focus{
                outline:none;
            }
            &::placeholder {
                    font-weight: 400;
                    color: white;
                }
        }
        img{
            width: 24px;
            position: absolute;
            left: 10px;
            top: 10px;
            z-index: 1;
        }
        .email{
            .inp_mail{
                text-indent: 50px;
            }
            img{
                left: 360px;
                top: 15px;
            }
        }
        .ins_btn{
            border: 1px solid rgb(255, 255, 255);
            border-radius: 10px;
            a{
                display: flex;
                justify-content: center;
                align-items: center;
                padding: 10px 50px;
                color:#fff;
            }
        }
    }
    .check{
        p{
            color:#fff;
            margin-top: 30px;
            font-weight: bold;
        }
    }
    .r_img{
        width: 350px;height: 287px;  
        position: absolute;right: 20px;
        top: -50px;
    }
}

</style>