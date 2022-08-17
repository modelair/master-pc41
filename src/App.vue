<template>
  <link rel="prefetch stylesheet"
        href="https://use.typekit.net/uso4aoz.css?family=Lato:300,400,500&display=swap"
        crossorigin="anonymous"
  />
  <FenixMain/>
</template>

<script>
import FenixMain from './components/FenixMain.vue'

export default {
  name: 'App',
  components: {
    FenixMain
  }
}
</script>

<style>
html {
  background-color: var(--background-color);
   --primary-color: #2E8BE8;
  --background-color: #2a343a;
  font-family: Lato, sans-serif;
}
#app {

  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  background-color: var(--background-color);
  color: var(--primary-color);
  margin-top: 60px;
  font-size: 24px;

}


</style>
