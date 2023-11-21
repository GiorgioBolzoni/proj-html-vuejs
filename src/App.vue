<template>
  <div>
    <header class="d-flex p-3">
      <NavBar />
    </header>
    <main>
      <MainApp />
    </main>
  </div>
</template>

<script>
import { store } from './data/store'; 
import axios from 'axios';
import NavBar from './components/header/NavBar.vue'; 
import MainApp from './components/main/MainApp.vue'; 

export default {
  components:{
    NavBar,
    MainApp,
  },
  data () {
    

    return {}
  }
}
</script>

<style lang="scss" scoped>

</style>