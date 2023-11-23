<template>
    <div class="container">
        <div class="text-center py-3">
            <h3>Resent New & Articles</h3>
            <h6>Important information about bike</h6>
        </div>
        <div class="carousel">
            <div class="card-container d-flex justify-content-between">
                <div v-for="(image, index) in visibleImages" :key="index" class="card p-4" @click="resetAutoSlide">
                    <img :src="image.img" alt="immagine" class="active">
                    <div class="image-text d-flex flex-column justify-content-between align-items-center text-center">
                        <div class="image-data" v-html="image.date"></div>
                        <div class="image-title" v-html="image.title"></div>
                        <div class="image-info" v-html="image.info"></div>
                        <button type="button" class="px-3 py-2 w-50">More</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Carousel2',
    data() {
      return {
        images: [
          { 
            img: '/images/news-bike5-373x223.jpg',
            date: `
                <div>22.06.2022 - Bike</div>
            `,
            title: `<h4><strong>Road bike or mountain bike?</strong></h4>`,
            info: `<p>Compared to similar road bikes with a solid frame structure, […]</p>`,
          },
          { 
            img: '/images/news-bike6-373x223.jpg',
            date: `
                <div>22.06.2022 - Bike</div>
            `,
            title: `<h4><strong>What is mountain biking called?</strong></h4>`,
            info: `<p>Mountain biking is one of the most popular outdoor sports, […]</p>`,
          },
          { 
            img: '/images/news-bike3-373x223.jpg',
            date: `
                <div>22.06.2022 - Bike</div>
            `,
            title: `<h4><strong>How much should you cycle a day?</strong></h4>`,
            info: `<p>In order to get the right benefit from the exercise […]</p>`,
          },
          { 
            img: '/images/news-bike4-373x223.jpg',
            date: `
                <div>22.06.2022 - Bike</div>
            `,
            title: `<h4><strong>How long does it take 5 km by bike?</strong></h4>`,
            info: `<p>It takes 5 km and 10 minutes, sir. But at […]</p>`,
          },
        ],
        currentIndex: 0,
        autoSlideInterval: null,
        cardsPerView: 4,
      };
    },
    computed: {
      visibleImages() {
        const startIndex = this.currentIndex;
        let endIndex = startIndex + this.cardsPerView;
  
        if (endIndex > this.images.length) {
          endIndex = endIndex - this.images.length;
          return [...this.images.slice(startIndex), ...this.images.slice(0, endIndex)];
        }
  
        return this.images.slice(startIndex, endIndex);
      },
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
        }, 10000);
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
  .card-container {
    display: flex;
    transition: all 1s ease-in-out;
    padding: 20px;
  }
  
  .card {
    position: relative;
    overflow: hidden;
    cursor: pointer;
    width: calc((100% / 4) - 40px);
    border: none;
    box-shadow: 1px 1px 10px 10px #f5f5f5;
  }
  
  img {
    width: 100%;
    display: block;
    position: relative;
  }  
  .active {
    transform: translateX(0);
  }
  
  .image-title {
    color: black;
    font-weight: 600;
    font-size: 1.2em;
  }
  
  
  .description {
    margin-top: 20px;
  }
  
  .button-prev,
  .button-next {
    background-color: white;
    width: 60px;
    height: 60px;
    border: 2px solid black;
    border-radius: 0;
    color: black;
    font-size: 16px;
    cursor: pointer;
    z-index: 1;
    font-size: 3em;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  </style>
  