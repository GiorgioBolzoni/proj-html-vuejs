<template>
  <div>
    <header class="d-flex p-3">
      <NavBar @search-media="functionSearchMedia" />
    </header>
  </div>
</template>

<script>
import { store } from './data/store'; 
import axios from 'axios';
import NavBar from './components/header/NavBar.vue'; 

export default {
  components:{
    NavBar,
  },
  setup () {
    

    return {}
  }
}
</script>

<style lang="scss" scoped>

</style>