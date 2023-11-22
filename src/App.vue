<template>
  <div>
    <header class="d-flex p-3">
      <NavBar />
    </header>
    <main>
      <MainApp />
    </main>
    <footer>
      <FooterApp />
    </footer>
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
</style>