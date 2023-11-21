<template>
    <div class="carousel">
      <button @click="slidePrecedente" class="button-prev">&lt;</button>
      <div class="image-container">
        <img :src="images[currentIndex].img" alt="immagine" class="active" @click="resetAutoSlide">
        <div class="image-text">
            <div class="image-title" v-html="images[currentIndex].text">
            </div>
            <div>
                <div class="py-2">Learn cycling from the pros.</div>
                <button type="button" class="px-5 py-3">Learn More</button>
            </div>
        </div>
      </div>
      <button @click="slideSuccessiva" class="button-next">&gt;</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Carousel1',
    data() {
      return {
        images: [
          { 
            img: '/images/event1.jpg',
            text: `<div>Learn Mountain Bike <br> From The Expert</div>`
          },
          { 
            img: '/images/event2.jpg',
            text: `<div>Professional <br> Cycling Club</div>`,
          },
          { 
            img: '/images/event3.jpg',
            text: `<div>Unforgettable <br> Cycling Experience</div>`,
          },
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
    height: 800px;
  }
  
  .image-container {
    position: relative;
  }
  
  img {
    width: 100%;
    transition: transform 1s ease-in-out;

  }
  
  .active {
    transform: translateX(0);
  }
  
  .image-text{
    position: absolute;
    top: 300px;
    left: 140px;
    right: 0;
    bottom: 0;
    display: flex;
    align-items: start;
    color: white;
    text-align: start;
    font-weight: 600;
    flex-direction: column;
  }
  .image-title {
    
    font-size: 3em;
  }
  .button-prev,
  .button-next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: black;
    width: 60px;
    height: 60px;
    border: none;
    color: white;
    font-size: 16px;
    cursor: pointer;
    z-index: 1;
    font-size: 3em;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .button-prev {
    left: 10px;
  }
  
  .button-next {
    right: 10px;
  }
  </style>
  