<template>
<div class="slide">
    <div class="my-slide">
        <transition-group name="fade">
            <div class="img" v-show="ShowIndex===index" v-for="(img,index) in imgs" :key="img">
                <img  :src="img.src" width="100%">
            </div>
        </transition-group>
    </div>
    <div class="nav">
        <div v-for="n in 3" :key="n" :class="['point',{active:n-1===ShowIndex}]" @click="Active(n-1)"></div>

    </div>
    <div class="pre">

    </div>
    <div class="next" @click="next"> > </div>

</div>
    
</template>

<script>
    export default {
        name: "Slide",
        data:function() {
                 return {
                     ShowIndex:0,
                     imgs:[
                         {src:require('../../static/kakki1.jpg')},
                         {src:require('../../static/kakki2.jpg')},
                         {src:require('../../static/kakki4.jpg')},
                     ]
                 };
             },
        methods:{
            Active(i){
                this.ShowIndex=i;
            },
            next(){
                this.ShowIndex++;
                if(this.ShowIndex>2){
                    this.ShowIndex=0;
                }
                this.Active(this.ShowIndex);
            }
        },
        mounted() {
            setInterval(this.next,5000)
        }
    }
</script>

<style scoped>
    .slide{
        width: 40%;
        display: flex;
        justify-content: center;
        margin-top: 10px;
        position: relative;
    }
    .img{
        display: flex;
        justify-content: center;

    }

    img{
        border-radius: 5%;
    }
    .nav{
        position: absolute;
        display: flex;
        justify-content: center;
        bottom: 0;
    }
    .pre,.next{
        position: absolute;
        font-weight: 900;
        font-size: 300%;
        top:50%;
        color: rgba(228, 237, 226, 0.6);
    }
    .point{
        width: 8px;
        height: 8px;
        border-radius: 50%;
        margin: 3px;
        background-color: rgba(166, 177, 177, 0.8);
        cursor: pointer;
    }
    .active{
        background-color: #ec292d;
    }
    .next{
        position: absolute;
        right: 5%;
        cursor: pointer;
    }
    .pre{
        position: absolute;
        left: 5%;
    }
    .fade-enter-active, .fade-leave-active {
        transition: opacity .8s;
    }
    .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
        opacity: 0;
        position: absolute;
        top:5%;
    }



</style>