<template>
    <div class="row d-flex justify-content-between">
      <div class="col-6 card-image d-flex justify-content-center align-items-center">
        <div class="bike-circle-container">
          <img src="/images/bike-circle.png" alt="bike-circle" class="bike-circle">
          <img src="/images/bike-player.png" alt="bike-player" class="bike-player">
        </div>
      </div>
      <div class="col-5">
        <h3 class="py-1">Do you want to be a professional cyclist?</h3>
        <div class="py-3">
          We offer 6 courses of varying difficulty and beautiful scenery that cyclists of all levels can enjoy. You will
          learn cycling from professionals with our competent and experienced staff. You will have a lot of fun with our
          amazing space.
        </div>
        <img class="divider" width="120" height="15" title="divider" alt="divider"
          src="https://garantiwebtasarim.com/wordpress/gobike/wp-content/uploads/2022/05/divider.jpg">
        <div class="py-3">
            <h4>Professional Team</h4>
            <div>We make you professional by adding your sincerity as well as professionalism.</div>
            <h4>Professional Trainings</h4>
            <div>We always ride with the best equipment, respecting nature and fun.</div>
        </div>
        <button type="button" class="p-3">Get to know us</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Section2',
    data() {
      return {};
    },
  };
  </script>
  
  <style lang="scss" scoped>
  .card-image {
    position: relative;
  }
  
  .bike-circle-container {
    position: relative;
    width: 100%;
    height: 0;
    padding-top: 100%; 
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .bike-circle {
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    width: 100%;
    height: 100%;
    position: absolute;
    animation: rotateCircle 10s linear infinite; 
  }
  
  @keyframes rotateCircle {
    from {
      transform: rotate(0deg);
    }
    to {
      transform: rotate(360deg);
    }
  }
  h3, h4, button{
    font-weight: 600;
  }
  .bike-player {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    width: 100%;
  }
  </style>
  