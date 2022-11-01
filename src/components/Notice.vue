<template>
    <div class="container noticeWrap">
        <NoticeCon :notice="notice"  data-aos="fade-up" data-aos-duration="1500"></NoticeCon>
        <Announce :result="result"  data-aos="fade-up" data-aos-duration="2000"></Announce>
    </div>

</template>

<script>
import NoticeCon from './NoticeCon.vue';
import Announce from './Announce.vue';



export default {
    components: { NoticeCon, Announce },
    props:[
        "notice",
        "result",
    ]
}
</script>

<style>
.noticeWrap{
    display: flex;
    gap: 80px;
    padding: 50px 0;
}

@media (max-width: 991px){
    .noticeWrap{
    display: block;

}
}

</style>