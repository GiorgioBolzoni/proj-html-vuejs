<template>
  
  <div>
    <header class="d-flex p-3">
      <NavBar />
    </header>
    <main>
      <MainApp />
    </main>
    <footer class="mt-5">
      <FooterApp />
    </footer>
    <div id="top">
      <button type="button"><a href="#"><i class="fa-solid fa-chevron-up fa-2xl" style="color: #ffffff;"></i></a></button>
    </div>
  </div>
</template>

<script>
import { store } from './data/store'; 
import axios from 'axios';
import NavBar from './components/header/NavBar.vue'; 
import MainApp from './components/main/MainApp.vue'; 
import FooterApp from './components/footer/FooterApp.vue'; 

export default {
  components:{
    NavBar,
    MainApp,
    FooterApp,
  },
  data () {
    

    return {}
  }
}
</script>

<style lang="scss" scoped>
  main{
    margin-top: 50px;
  }
  #top{
    background: black;
    display: block;
    position: fixed;
    bottom: 10px;
    right: 10px;
    z-index: 100;
    width: 60px;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>