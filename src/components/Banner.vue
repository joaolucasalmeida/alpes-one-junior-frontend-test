<template>
  <img class="banner-imagem" src="imgs/banners/desktop-.jpg" alt="banner" />
  <img
    class="banner-imagem-mobile"
    src="imgs/banners/mobile-banner.png"
    alt="banner-mobile"
  />
  <div class="carousel-container">
    <CarouselNavigations />
  </div>
</template>

<script>
import CarouselNavigations from "../components/CarouselNavigations.vue";

export default {
  name: "Banner",
  components: {
    CarouselNavigations,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.banner-imagem {
  width: 1920px;
  min-width: 1400px;
}
.banner-imagem-mobile {
  display: none;
}
.carousel-container {
  position: absolute;
  bottom: 43px;
  left: 929px;
  min-width: 80px;
}
@media screen and (max-width: 600px) {
  .banner-imagem {
    display: none;
  }
  .banner-imagem-mobile {
    display: flex;
    width: 100%;
  }
  .carousel-container {
    display: none;
  }
}
</style>
