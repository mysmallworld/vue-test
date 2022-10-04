<template>
<div class="home">
  <HomeVue/>
  </div>
</template>

<script>
import HomeVue from './views/home-vue.vue'

export default {
  name: 'App',
  components: {
    HomeVue
  }
}
</script>

<style>
#app {
  font-family: 'Roboto';
  color:#FFF;
  top: 83px;
  left: 0px;
  width: 1429px;
  height: 612px;
  background: var(--unnamed-color-242424) 0% 0% no-repeat padding-box;
  background: #242424 0% 0% no-repeat padding-box;
  opacity: 1;
}
</style>
