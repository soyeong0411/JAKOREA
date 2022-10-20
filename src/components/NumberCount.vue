<template>
  <div class="numberCount">
    <div class="container numberWrap">
        <img src="../assets/main-number-1.jpg" alt="">
        <div class="graph">
            <div class="graphWrap">
                <div class="numGraph">
                    <div class="numLine"></div>
                    <P>+200</P>
                </div>
                <p class="graphTxt"><span>지역 네트워크</span>전국 17개 시도 200개이상의 지역에서 교육하고 있습니다.</p>
            </div>
            <div class="graphWrap">
                <div class="numGraph">
                    <div class="numLine"></div>
                    <P>+1,000</P>
                </div>
                <p class="graphTxt"><span>학교 및 기관</span>전국 1,000여개 학교 및 기관, 단체와 협업하여 교육을 진행합니다.</p>
            </div>
            <div class="graphWrap">
                <div class="numGraph">
                    <div class="numLine"></div>
                    <P>+3,000</P>
                </div>
                <p class="graphTxt"><span>교육 진행자</span>3,000여명의 전문 지식을 갖춘 봉사자와 교사, 강사가 함께 교육을 진행하고 있습니다.</p>
            </div>
            <div class="graphWrap">
                <div class="numGraph">
                    <div class="numLine"></div>
                    <P>+90,000</P>
                </div>
                <p class="graphTxt"><span>교육 수혜자</span>전국 90,000여명의 청소년들이 교육 프로그램에 참여합니다.</p>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.numberCount{
    background: rgb(40, 106, 148);
    height: 500px;
    display: flex;
    align-items: center;
    .numberWrap{
        display: flex;
        justify-content: center;
        align-items: center;
        justify-content: space-between;
        img{
        width: 400px;
        border-radius: 20px;
    }
    }
    .graphWrap{
        display: flex;
        flex-direction: column;
        margin-left: 30px;
        .numGraph{
        display: flex;
        align-items: center;

        p{
            font-size: 32px;
            color:#fff;
            font-weight: bold;
            margin-bottom: 0;
            margin-left: 15px;
        }
        .numLine{
        width: 700px;height: 10px;
        background: rgb(50, 164, 235);
        border-radius: 10px;
    }
    }
    .graphTxt{
        margin-top: -12px;
        color:#fff;
        font-size: 15px;
        span{
            font-weight: bold;
            font-size: 17px;
            margin-right: 15px;
        }
    }
    }
    
    
    
}

</style>