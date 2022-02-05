<template>
  <footer class="footer">
    <div class="footer-text-container">
      <p class="footer-text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed a elementum
        orci, vitae commodo nibh. In vitae convallis nisl. Morbi rhoncus mattis
        purus sed commodo. Integer rhoncus ex risus. Proin efficitur elit nunc, ut
        pulvinar massa egestas in. Fusce quis quam viverra, pretium quam ac,
        consectetur lectus.
      </p>
    </div>
    <div class="copyright-container">
      <img class="logo-bmw" src="imgs/logos/logo-bmw-rio.svg" alt="logo bmw" />
      <span>© Copyright © 2021 Lorem ipsum dolor sit amet.</span>
      <div class="logo-alpes-container">
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
  height: 251px;
  min-width: 1280px;
  background-color: #e6e6e6;
}
.footer-text-container {
  display: flex;
  justify-content: center;
}
.footer-text {
  font-family: BMWTypeNext-Light;
  font-size: 14px;
  text-align: center;
  padding-top: 40px;
  padding-bottom: 40px;
  width: 1082px;
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
    min-width: 0;
    height: 266px;
  }
  .footer-text {
    width: auto;
    margin: 0;
    padding-top: 30px;
    padding-bottom: 46px;
    padding-right: 15px;
    padding-left: 15px;
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
