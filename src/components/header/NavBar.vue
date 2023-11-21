<template>
    <div class="container d-flex justify-content-between">
      <section class="border col-lg-3 col-md-4 card">
        <img src="/images/logo-gobike.png" alt="">
      </section>

      <section class="border col-lg-6 d-flex align-items-center justify-content-between">
        <ul class="d-flex ">
                <li class="d-flex align-items-center py-4 mx-3 " v-for="(content, index) in NavListContent" :key="index">
                    <a href="#">{{ content.text }}</a>
                </li>
            </ul>
      </section>

      <section class="border col-lg-3 col-md-4 d-flex align-items-center justify-content-between">
        <div>
          <i class="fa-solid fa-bars" style="color: #000000;"></i>
        </div>
        <button type="button" class="d-flex px-5 py-3">
          <img src="images/h" alt="">
          <span>Upcoming events <i class="fa-solid fa-arrow-right" style="color: #000000;"></i></span>
        </button>
      </section>
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
  li{
    list-style: none;
    a{
      color: black;
    }
  }

</style>