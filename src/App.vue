<template>
  <div class="app">
    <AboutMe/>
  </div>
</template>

<script>
import AboutMe from './components/about-me.vue'
import '@/icons/style.css'

export default {
  name: 'App',
  components: {
    AboutMe
  }
}
</script>

<style lang="scss">
$background: #191919;

.app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: $background;
  height: 100%;
  width: 100%;
}
</style>
