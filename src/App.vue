<template>
  <Form />
  <Banner />
  <Card marcaDoCarro="BMW Serie 1" imagemDoCarro="imgs\veiculos\serie1.png"/>
</template>

<script>
import Card from './components/Card.vue'
import Banner from './components/Banner.vue'
import Form from './components/Form.vue'

export default {
  name: 'App',
  components: {
    Banner,
    Card, 
    Form
  }
}
</script>

<style>
/*
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
*/
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
