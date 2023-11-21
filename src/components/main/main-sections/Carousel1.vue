<template>
    <div class="carousel">
      <button @click="slidePrecedente" class="button-prev">&lt;</button>
      <img :src="images[currentIndex].img" alt="immagine" class="active" @click="resetAutoSlide">
      <button @click="slideSuccessiva" class="button-next">&gt;</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Carousel1',
    data() {
      return {
        images: [
          { img: '/images/event1.jpg' },
          { img: '/images/event2.jpg' },
          { img: '/images/event3.jpg' },
          { img: '/images/event4.jpg' },
          { img: '/images/event5.jpg' },
          { img: '/images/event6.jpg' },
          { img: '/images/event7.jpg' },
          { img: '/images/event8.jpg' },
          { img: '/images/event9.jpg' },
          { img: '/images/event10.jpg' },
        ],
        currentIndex: 0,
        autoSlideInterval: null,
      };
    },
    methods: {
      slidePrecedente() {
        this.currentIndex = (this.currentIndex - 1 + this.images.length) % this.images.length;
        this.resetAutoSlide();
      },
      slideSuccessiva() {
        this.currentIndex = (this.currentIndex + 1) % this.images.length;
        this.resetAutoSlide();
      },
      startAutoSlide() {
        this.autoSlideInterval = setInterval(() => {
          this.slideSuccessiva();
        }, 5000);
      },
      stopAutoSlide() {
        clearInterval(this.autoSlideInterval);
      },
      resetAutoSlide() {
        this.stopAutoSlide();
        this.startAutoSlide();
      },
    },
    mounted() {
      this.startAutoSlide();
    },
    beforeDestroy() {
      this.stopAutoSlide();
    },
  };
  </script>
  
  <style lang="scss" scoped>
  .carousel {
    overflow: hidden;
    position: relative;
  }
  
  img {
    width: 100%;
    transition: transform 0.4s ease-in-out;
  }
  
  .active {
    transform: translateX(0);
  }
  
  .button-prev,
  .button-next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: transparent;
    border: none;
    color: white;
    font-size: 16px;
    cursor: pointer;
    z-index: 1;
  }
  
  .button-prev {
    left: 10px;
  }
  
  .button-next {
    right: 10px;
  }
  </style>
  