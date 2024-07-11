<template>
  <FullscreenImage/>
 <HelloWorld/>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'
import FullscreenImage from '../components/OnLoad.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    FullscreenImage
  }
}
</script>
