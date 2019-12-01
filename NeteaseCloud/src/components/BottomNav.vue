<template>
    <div class="BottomNav">
        <div class="item">
            <p>发现</p>
        </div>
        <div class="item">
            <p>视频</p>
        </div>
        <div class="item">
            <p>我的</p>
        </div>
        <div class="item">
            <p>云村</p>
        </div>
        <div class="item">
            <p>账号</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: "BottomNav"
    }
</script>

<style scoped>
    .BottomNav{
        position:fixed;
        bottom: 0;
        width: 40%;
        display: flex;
        justify-content: center;
        background-color: #c9d1c8;

    }
    .item{
        text-align: center;
        width:20%;
        cursor: pointer;
    }
    .item:visited{
        color: #ec292d;
    }

</style>