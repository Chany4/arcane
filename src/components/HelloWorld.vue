<template>
  <div class="image-container">
    <img id="animatedImage" src="../assets/logo.png" alt="Animated Image">
  </div>
</template>

<script>
export default {
  name: 'AnimatedImage',
  mounted() {
    const image = document.getElementById('animatedImage');
    image.style.animationPlayState = 'running';
  }
}
</script>

<style scoped>
.image-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f0f0f0;
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
