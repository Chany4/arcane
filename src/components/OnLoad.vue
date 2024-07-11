<template>
    <div class="fullscreen-overlay" v-show="show">
      <img id="animatedImage" src="@/assets/logo.png" alt="Animated Image" @animationend="hideImage">
    </div>
  </template>
  
  <script>
  export default {
    name: 'FullscreenImage',
    data() {
      return {
        show: true,
      };
    },
    mounted() {
      const image = document.getElementById('animatedImage');
      image.style.animationPlayState = 'running';
    },
    methods: {
      hideImage() {
        this.show = false;
      }
    }
  }
  </script>
  
  <style scoped>
  .fullscreen-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgba(0, 0, 0, 0.8); /* Dark background */
    z-index: 9999; /* High z-index to ensure it takes priority */
  }
  
  #animatedImage {
    opacity: 0;
    transform: scale(1);
    animation: popInZoomOut 3s forwards;
  }
  
  @keyframes popInZoomOut {
    0% {
      opacity: 0;
      transform: scale(1);
    }
    10% {
      opacity: 1;
      transform: scale(1);
    }
    50% {
      transform: scale(1.1);
    }
    100% {
      opacity: 0;
      transform: scale(1.1);
    }
  }
  </style>
  