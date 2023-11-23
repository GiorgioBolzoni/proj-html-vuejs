<template>
    <div class="navbar">
      <div class="container d-flex justify-content-between align-items-center">
        <section class="col-lg-3 col-md-4 logo">
          <img src="/images/logo-gobike.png" alt="">
        </section>

        <section class="col-lg-6 d-flex align-items-center justify-content-between">
          <ul class="d-flex align-items-center">
                  <li class="d-flex align-items-center py-4 mx-3 " v-for="(content, index) in NavListContent" :key="index">
                      <a href="#">{{ content.text }}</a>
                  </li>
              </ul>
        </section>

        <section class="col-lg-3 col-md-4 d-flex align-items-center justify-content-between">
          <div>
            <!-- <i class="fa-solid fa-bars" style="color: #000000;"></i> -->
            <div class="hamburger-menu"> 
              <span></span> 
              <span></span> 
              <span></span> 
            </div>
          </div>
          <button type="button" class="d-flex px-5 py-3 ms-3 align-items-center justify-content-between">
            <img src="/images/Screenshot 2023-11-23 122012.png" alt="img">
            <span class="d-flex justify-content-center align-content-center">Upcoming events 
              <!-- <i class="fa-solid fa-arrow-right" style="color: #ffffff;"></i>  -->
            </span>
          </button>
        </section>
      </div>
    </div>
</template>

<script>
export default {
    name: 'NavBar',
    data() {
        return {
          NavListContent: [
                {
                    text: 'Home'
                },
                {
                    text: 'About Us'
                },
                {
                    text: 'Trainings'
                },
                {
                    text: 'Packages'
                },
                {
                    text: 'Blog'
                },
                {
                    text: 'Contact'
                },
              ]
    }
  },
  methods: {
    
  },
}
</script>

<style lang="scss" scoped>

  *{
    font-weight:500;
  }

  .navbar{
    position: fixed;
    z-index: 1000;
    height: 150px;
    top: 0;
    left: 0;
    right: 0;
    background-color: white;
  }
  .logo{
    
      max-width: min-content;
    
  }
  li{
    list-style: none;
    a{
      color: black;
    }
  }
.hamburger-menu {
    width: 30px;
    height: 20px;
    position: relative;
    cursor: pointer;
}
.hamburger-menu span {
    position: absolute;
    height: 2px;
    width: 100%;
    background: black;
}
.hamburger-menu span:nth-child(1) {
    top: 0px;
    width: 100%;
}
.hamburger-menu span:nth-child(2) {
    top: 9px;
    width: 22px;
}
.hamburger-menu span:nth-child(3) {
    top: 18px;
    width: 100%;
}
button{
  img{
    max-width: 30%;
    margin-left: -20px;
  }
}
</style>