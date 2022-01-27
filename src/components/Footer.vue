<template>
  <footer class="footer">
    <p class="footer-text">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed a elementum
      orci, vitae commodo nibh. In vitae convallis nisl. Morbi rhoncus mattis
      purus sed commodo. Integer rhoncus ex risus. Proin efficitur elit nunc, ut
      pulvinar massa egestas in. Fusce quis quam viverra, pretium quam ac,
      consectetur lectus.
    </p>
    <div class="copyright-container">
      <img class="logo-bmw" src="imgs/logos/logo-bmw-rio.svg" alt="logo bmw" />
      <span>© Copyright © 2021 Lorem ipsum dolor sit amet.</span>
      <div class="logo-alpes-container">
        <span>Feito por:</span>
        <img
          class="logo-alpes"
          src="imgs/logos/logo-alpes.png"
          alt="logo alpes"
        />
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.footer {
  width: 1920px;
  height: 251px;
  background-color: #e6e6e6;
}
.footer-text {
  font-family: BMWTypeNext-Light;
  font-size: 14px;
  width: 1350px;
  text-align: center;
  margin-left: 285px;
  padding-top: 40px;
  padding-bottom: 40px;
}
.copyright-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-left: 285px;
  margin-right: 285px;
  font-family: BMWTypeNext-Light;
  font-size: 12px;
  border-top: 1px solid #bbbbbb;
  height: 110px;
}
.logo-bmw {
  width: 50px;
  height: 50px;
}
.logo-alpes {
  width: 124px;
  height: 24px;
  margin-left: 13px;
}
.logo-alpes-container {
  display: flex;
  align-items: center;
}

@media screen and (max-width: 600px) {
  .footer {
    width: 100%;
    height: 266px;
  }
  .footer-text {
    width: auto;
    margin: 0;
    padding-top: 30px;
    padding-bottom: 46px;
    font-size: 10px;
  }
  .logo-bmw {
      display: none;
  }
  .copyright-container { 
    margin-left: 0;
    margin-right: 0;
    flex-direction: column;
    justify-content: center;
    font-size: 10px;
  }
  .logo-alpes-container {
      padding-top: 30px;
  }
}
</style>
