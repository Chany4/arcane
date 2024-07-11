<template>
  <section>
    <Navigation/>
  </section>
  <router-view/>
</template>

<script>
import Navigation from '@/components/NavBar.vue'

export default{
components:{
  Navigation
}

}
</script>

<style src="../src/assets/css/style.css">
</style>
