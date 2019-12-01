<template>
    <div class="SongList">
        <div class="header">
            <div class="title">推荐歌单</div>
            <div class="market">歌单广场</div>
        </div>
        <div class="covers" :style="{display:MinDisplay}">
            <div class="cover" v-for="(img,index) in imgs" :key='img'><img :src="img.src" width="90%" class="min" @click="ZoomIn(index)" alt=""></div>

        </div>
        <div class="max" :style="{display:display}">
            <div @click="ZoomOut"  v-for="(img,index) in imgs" :key='img' :class="[index===ShowIndex?'active':'None']" ><img :src="img.src" width="100%"></div>
            <div class="small">
                <div :class="[{'smallActive':index===ShowIndex},'cover-small']" v-for="(img,index) in imgs" :key='img' @click="select(index)" ><img :src="img.src" width="90%"></div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "SongList",
        data:function() {
            return {
                ShowIndex:0,
                display: 'none',
                MinDisplay:'flex',
                imgs:[
                    {"src":require('../../static/cover1.jpg')},
                    {"src":require('../../static/cover2.jpg')},
                    {"src":require('../../static/cover3.jpg')},
                    {"src":require('../../static/cover4.jpg')},
                    {"src":require('../../static/cover5.jpg')},
                    {"src":require('../../static/cover6.jpg')},
                    {"src":require('../../static/cover7.jpg')},
                    {"src":require('../../static/cover8.jpg')},
                    {"src":require('../../static/cover9.jpg')},
                ]

            };
        },
        methods:{
            ZoomIn(i){
               this.display='block';
                this.MinDisplay='none';
                this.ShowIndex=i;
            },
            ZoomOut(){
                this.display='none';
                this.MinDisplay='flex';
            },
            select(i){
                this.ShowIndex=i;


            }
        }
    }
</script>

<style scoped>
    .SongList{
        width: 40%;
    }
    .header{
        display: flex;
        justify-content: space-between;
    }
    .title{
        font-weight: bold;
    }
    .market{
        font-size: 90%;
        text-align: center;
        width: 70px;
        border-radius: 10px;
        height: 20px;
        border: 1px solid rgba(200,200,200,0.9);
        cursor: pointer;
    }
    .covers{
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }
    .cover{
        display: flex;
        justify-content: center;
        width: 33%;
        margin: 10px 0;
    }
    .min{
        border-radius: 10px;
        cursor: zoom-in;
    }
    .max{
        cursor: zoom-out;
        width: 100%;

    }
    .small{
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }
    .cover-small{
        display: flex;
        justify-content: center;
        width: 10%;
        margin: 10px 0;
        opacity: 0.6;
        cursor: pointer;
    }
    .cover-small:hover{
        opacity: 1;
    }
    .active{
        display: flex;
    }
    .None{
        display: none;
    }
    .smallActive{
        opacity: 1;
    }




</style>