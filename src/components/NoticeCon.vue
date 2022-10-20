<template>
  <div class="noticeCon">
    <h1>모집공고</h1>
    <div class="notice" v-for="(item,i) in 4" :key="i">
        <h4><a href="#">{{notice[i].title}}</a></h4>
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

<style>

</style>