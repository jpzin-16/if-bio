<template>
    <div class="slider-container">
      <transition name="fade" mode="out-in">
        <div :key="currentIndex" class="slider-image-container">
          <img :src="currentImg.src" class="slider-image" />
        </div>
      </transition>
      <a href="#" class="prev" @click="prev">&#10094; Previous</a>
      <a href="#" class="next" @click="next">&#10095; Next</a>
    </div>
  </template>
  
  <script>
  export default {
    name: 'TheSlider',
    data() {
      return {
        images: [
          { src: require("@/assets/FotoNaChuva.jpg") },
          { src: require("@/assets/MicroscopioAmarelo.jpg") },
          { src: require("@/assets/MicroscopioAzul.jpg") },
          { src: require("@/assets/MinaOlhandoMicroscopio.jpg") },
          { src: require("@/assets/MuitaGenteNumEspaco.jpg") },
        ],
        timer: null,
        currentIndex: 0
      };
    },
    mounted: function () {
      this.startSlide();
    },
    beforeUnmount: function () {
      clearInterval(this.timer);
    },
    methods: {
      startSlide: function () {
        this.timer = setInterval(this.next, 4000);
      },
      next: function () {
        this.currentIndex = (this.currentIndex + 1) % this.images.length;
      },
      prev: function () {
        this.currentIndex = (this.currentIndex - 1 + this.images.length) % this.images.length;
      }
    },
    computed: {
      currentImg: function () {
        return this.images[this.currentIndex];
      }
    }
  }
  </script>
  
  <style>
  .slider-container {
    position: relative;
    overflow: hidden;
  }
  
  .fade-enter-active,
  .fade-leave-active {
    transition: opacity 0.95s;
  }
  
  .fade-enter, .fade-leave-to {
    opacity: 0;
  }
  
  .slider-image-container {
    position: relative;
  }
  
  .slider-image {
    width: 650px;
    height: 450px;
  }
  
  .prev, .next {
    position: absolute;
    top: 50%;   
    font-size: 18px;
    color: white;
    background-color: rgba(0, 0, 0, 0.7);
    border: none;
    padding: 10px;
    cursor: pointer;
    user-select: none;
    visibility: hidden
  }
  
  .prev {
    left: 0;
  }
  
  .next {
    right: 0;
  }
  
  .prev:hover, .next:hover {
    background-color: rgba(0, 0, 0, 0.9);
  }
  </style>
  