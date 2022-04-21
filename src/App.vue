<template>
  <div id="app">
    
    <MainComp/>
  </div>
</template>

<script>
import "bootstrap"

import MainComp from './components/MainComp.vue'
export default {
  
  name: 'App',
  components: {

  MainComp
  }
}
</script>

<style lang="scss">
@import "bootstrap/dist/css/bootstrap.min.css";

#app{
  background: #1e2d3b;
  height: 100vh;
}
</style>
