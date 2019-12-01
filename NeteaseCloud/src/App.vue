<template>
  <div id="app">
    <Head></Head>
    <Slide></Slide>
    <TopNav></TopNav>
    <div class="line"></div>
    <song-list></song-list>
  </div>
</template>

<script>

import TopNav from "./components/TopNav";
import SongList from "./components/SongList";
import Head from "./components/Head";
import Slide from "./components/Slide";



export default {
  name: 'app',
  components: {
    TopNav,
    SongList,
    Head,
    Slide,
  }
}
</script>

<style>
  .line{
    width:40%;
    height: 1px;
    margin: 30px 0px;
    background-color: rgba(203, 203, 203, 0.9);
  }
  #app{
    margin: 20px;
  }

</style>
