<template>
  <div class="carousel">
    <div class="card-container row">
      <div v-for="(image, index) in visibleImages" :key="index" class="card-carousel col-3" @click="resetAutoSlide">
        <img :src="image.img" alt="immagine" class="active">
        <div class="image-text d-flex flex-column justify-content-between">
          <div class="image-title" v-html="image.text"></div>
          <button type="button" class="px-3 py-2 d-none btn-view">View</button>
        </div>
      </div>
    </div>
    <div class="d-flex justify-content-center">
      <button @click="slidePrecedente" class="button-prev my-5 mx-2">&lt;</button>
      <button @click="slideSuccessiva" class="button-next my-5 mx-2">&gt;</button>
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
          img: '/images/training-box-1.jpg',
          text: `<div>Riding Lesson</div>`,
        },
        { 
          img: '/images/training-box-2.jpg',
          text: `<div>Safe Driving</div>`,
        },
        { 
          img: '/images/training-box-3.jpg',
          text: `<div>Mountain Bike</div>`
        },
        { 
          img: '/images/training-box-4.jpg',
          text: `<div>Tail Drive</div>`,
        },
        { 
          img: '/images/training-box-5.jpg',
          text: `<div>Pedaling</div>`,
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
.carousel {
  overflow: hidden;
  position: relative;
  height: 800px;
}

.card-container {
  display: flex;
  transition: all 1s ease-in-out;
}

.card-carousel {
  position: relative;
  overflow: hidden;
  cursor: pointer;

}

img {
  width: 100%;
  display: block;
  border: 10px solid black;
  position: relative;
  filter: brightness(60%);
}

.card-carousel:hover img {
  filter: brightness(80%);  
}
.card-carousel:hover .btn-view {
  display: block;  //non compare!
}

.active {
  transform: translateX(0);
}

.image-text {
  position: absolute;
  top: 3%;
  left: 8%;
  color: white;
  text-align: start;
  font-weight: 600;
  height: 90%;
}

.image-title {
  font-size: 2em;
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
