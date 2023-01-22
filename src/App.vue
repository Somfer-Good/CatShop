<template>
  <div class="app">
    <Home/>
  </div>
</template>

<script>
import Home from './component/Home.vue';

export default {
    name: "App",
    components: { Home }
}
</script>
<style>
html {
  background-image: url(./assets/Background.png);
  background-repeat: no-repeat;
  background-position: center center;
  background-attachment: fixed;
  background-size: cover;
}
@font-face {
	font-family: 'Exo2.0'; 
	src: url(./fonts/Exo2.0-Thin.otf); 
}
</style>
