<template>
    <div class="nav">
        <div class="item">
            <div class="icon"><i class="fas fa-calendar-day"></i></div>
            <div class="text"><p>每日推荐</p></div>
        </div>
        <div class="item">
            <div class="icon"><i class="fas fa-stream"></i></div>
            <div class="text"><p>歌单</p></div>
        </div>
        <div class="item">
            <div class="icon"></div>
            <div class="text"><p>排行榜</p></div>
        </div>
        <div class="item">
            <div class="icon"><i class="fas fa-broadcast-tower"></i></div>
            <div class="text"><p>电台</p></div>
        </div>
        <div class="item">
            <div class="icon"></div>
            <div class="text"><p>直播</p></div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "TopNav"
    }
</script>

<style scoped>
    .nav{
        width: 40%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .icon{
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background-color: #ff3526;
        cursor: pointer;
        margin: 10px;
        display: flex;
        justify-content: center;
        align-content: center;
    }
    .fas{
        color: rgba(240,240,240,1);
        font-size: 130%;
        position: relative;
        top:25%;
    }
    .text{
        text-align: center;
    }

</style>