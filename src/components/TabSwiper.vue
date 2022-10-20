<template>
    <div class="container tabWrap">
        <div class="tabSwiper">
            <h1>기관소식</h1>
            <div class="tabMenu">
                <div class="tab" @click="tab=1">공지사항</div>
                <div class="tab" @click="tab=2">스토리</div>
                <div class="tab" @click="tab=3">언론보도</div>
            </div>
        </div>

        <TabSwiperItem 
        :notice="notice" 
        :story="story" 
        :news="news"
        :tab="tab"
        ></TabSwiperItem>

    </div>
</template>

<script>
import TabSwiperItem from './TabSwiperItem.vue';

export default {
    props: [
        "notice",
        "story",
        "news",
    ],
    components: { TabSwiperItem },
    data(){
        return {
            tab:1
        }
    }
}
</script>

<style lang="scss" scoped>
.tabWrap{
    padding: 70px 0; 
    .tabSwiper{
    display: flex;
    align-items: center;
    .tabMenu{
        width: 300px;
        display: flex;
        justify-content: space-between;
        font-size: 22px;
        margin-left: 50px;


    }
}
}



</style>