<template>
  <div class="noticeCon">
    <h1>모집공고</h1>
    <div class="notice" v-for="(item,i) in 4" :key="i">
        <h5><a href="#">{{notice[i].title}}</a></h5>
        <p>{{notice[i].operate}}</p>
    </div>
  </div>
</template>

<script>
export default {
    props:[
        "notice"
    ],
}
</script>

<style lang="scss">
 .noticeCon{
    h1{
      &::after{
        content: "";display: block;
        border-bottom: 2px solid #000;
        margin: 20px 0;
      }
    }
    .notice{
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
</style>