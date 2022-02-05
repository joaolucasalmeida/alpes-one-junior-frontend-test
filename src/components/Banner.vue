<template>
  <img class="banner-imagem" src="imgs/banners/desktop-.jpg" alt="banner" />
  <img
    class="banner-imagem-mobile"
    src="imgs/banners/mobile-banner.png"
    alt="banner-mobile"
  />
</template>

<script>

export default {
  name: "Banner",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.banner-imagem {
  width: 100%;
  min-width: 1280px;
}
.banner-imagem-mobile {
  display: none;
}

@media screen and (max-width: 600px) {
  .banner-imagem {
    display: none;
  }
  .banner-imagem-mobile {
    display: flex;
    width: 100%;
  }

}
</style>
