<template>
  <Home />
</template>

<script>
import Home from "./pages/Home.vue";

export default {
  name: "App",
  components: {
    Home,
  },
};
</script>

<style>
@font-face {
  font-family: "BMWTypeNext-Bold";
  src: local("BMWTypeNext-Bold"),
    url(fonts/BMWTypeNext-Bold.20210426144302.ttf) format("truetype");
}
@font-face {
  font-family: "BMWTypeNext-Light";
  src: local("BMWTypeNext-Light"),
    url(fonts/BMWTypeNext-Light.20210426144302.ttf) format("truetype");
}
</style>
