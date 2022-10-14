<template>
  <div class="iconBanner">
    <div class="container">
        <div class="row">
            <ul>
                <li v-for="item in iconData" :key="item">
                    <img :src="`./images/${item.src}`" alt="">
                </li>
            </ul>
        </div>
    </div>
  </div>
</template>

<script>
import iconData from "@/data/02iconBanner.js"

export default {
    data(){
        return {
            iconData:iconData,
        }
    },
}
</script>

<style>

</style>