<template>
    <div class="container noticeWrap">
        <NoticeCon :notice="notice"></NoticeCon>
        <Announce :result="result"></Announce>
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
}
</style>