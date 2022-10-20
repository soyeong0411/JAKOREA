<template>
  <div class="resultCon">
    <h1>결과발표</h1>
    <div class="result" v-for="(item,i) in 4" :key="i">
        <h4><a href="#">{{result[i].title}}</a></h4>
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

<style>

</style>