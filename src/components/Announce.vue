<template>
  <div class="resultCon">
    <h1>결과발표</h1>
    <div class="result" v-for="(item,i) in 4" :key="i">
        <h5><a href="#">{{result[i].title}}</a></h5>
        <p>{{result[i].date}}</p>
    </div>
  </div>
</template>

<script>
export default {
    props:[
        "result"
    ],
}
</script>

<style lang="scss">
.resultCon{
  padding: 0 30px;
    h1{

      &::after{
        content: "";display: block;
        border-bottom: 2px solid #000;
        margin: 20px 0;
      }
    }
    .result{
      width: 550px;
      overflow: hidden;
      white-space: nowrap;
      text-overflow: ellipsis;
      padding: 20px 0;
      h5{
      font-weight: bold;
      }
      p{
        font-size: 14px;
        color:rgb(197, 197, 197);
        margin-top: 25px;
      }
    }
    
 }

 @media (max-width: 991px){
    .result{
      h5{
        font-size: 18px;
      }
    }
}
</style>