<template>
    <div class="header">
        <div class="recognize"><i class="fas fa-microphone"></i></div>
        <div class="input">
            <a href="/" class="search-icon"><i class="fas fa-search"></i></a>
            <input type="text" class="search-txt" placeholder="あいみょん" >
        </div>
        <div class="playing">
            <div class="one"></div>
            <div class="two"></div>
            <div class="three"></div>
            <div class="four"></div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Head"
    }
</script>

<style scoped>
    .header {
        width: 40%;
        display: flex;
        justify-content: space-between;
    }
    .recognize{
        display: flex;
        justify-content: center;
        align-content: center;
        color: rgba(0,0,0,0.8);
        margin: auto 10px;
    }
    .fa-microphone{
        font-size: 30px;
    }

    .input{
        background-color: rgba(228, 237, 226, 0.6);
        opacity: 0.7;
        width:300px;
        height: 40px;
        border: none;
        border-radius: 20px;
        display: flex;
        justify-content: center;
        align-content: center;

    }
    .search-icon{
        color: #b0b8ae;
        position: relative;
        height: 30px;
        left: -5%;
        top: 15%;

    }
    .search-txt{
        border: none;
        background-color: rgba(228, 237, 226, 0.6);
        opacity: 0.7;
        width: 230px;
        height: 40px;
    }
    input:focus{
        outline: none;
    }
    .playing{
        display: flex;
        justify-content: center;
        align-items: flex-end;

    }
    .one,.three{
        width: 2px;
        height: 30px;
        background-color: black;
        margin-left:5px;
        animation: move1 1s infinite ease;
    }
    .two,.four{
        width: 2px;
        height: 30px;
        background-color: black;
        margin-left: 5px;
        animation: move2 1s infinite ease;
    }
    @keyframes move1 {
        0%{height: 30px;}
        50%{height: 15px;}
        100%{height: 30px}
    }
    @keyframes move2 {
        0%{height: 15px;}
        50%{height: 30px;}
        100%{height: 15px;}

    }

</style>