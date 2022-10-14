<template>
  <Header></Header>
  <main-visual></main-visual>
</template>

<script>
import Header from "./components/Header.vue"
import MainVisual from './components/MainVisual.vue'


export default {
  components:{
    Header,
    MainVisual,

  }
}
</script>

<style>

@import url(./assets/style.css);

</style>
