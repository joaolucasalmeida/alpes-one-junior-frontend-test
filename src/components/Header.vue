<template>
  <header class="header">
    <div class="header-conteudo-container">
      <div>
        <HeaderButton
          icone="icons/svg/telefone.svg"
          textoBotao="(21) 2042-4442"
        />
        <HeaderButton icone="icons/svg/360.svg" textoBotao="TOUR VIRTUAL" />
        <HeaderButton
          icone="icons/svg/whatsapp.svg"
          textoBotao="WHATSAPP"
          color="#25D366"
          width="143"
        />
      </div>
      <div>
        <MenuButton textoBotao="1" />
        <MenuButton textoBotao="2" />
        <MenuButton textoBotao="3" />
        <MenuButton textoBotao="4" />
        <MenuButton textoBotao="5" />
        <MenuButton textoBotao="6" />
        <MenuButton textoBotao="7" />
        <MenuButton textoBotao="8" />
        <MenuButton textoBotao="X" />
        <MenuButton textoBotao="Z" />
        <MenuButton textoBotao="M" />
        <MenuButton textoBotao="i" />
        <MenuButton textoBotao="Plug-in-Hybrid" />
      </div>
    </div>
    <div class="mobile-header-container">
      <div class="mobile-telefone-header">
        <img
          class="mobile-icone-telefone"
          src="icons/svg/telefone.svg"
          alt="icone"
        />
        (21) 2042-4442
      </div>
      <img class="logo-bmw" src="imgs/logos/logo-bmw-rio.svg" alt="logo bmw" />
    </div>
    <div class="mobile-header-button">
      <Button textoBotao="Solicitar Cotação" width="100%" />
    </div>
  </header>
</template>

<script>
import HeaderButton from "../components/HeaderButton.vue";
import MenuButton from "../components/MenuButton.vue";
import Button from "../components/Button.vue";

export default {
  name: "Header",
  components: {
    HeaderButton,
    MenuButton,
    Button,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header {
  display: flex;
  justify-content: space-evenly;
  width: 1920px;
  height: 145px;
}
.header-conteudo-container {
  display: flex;
  flex-direction: column;
  padding-top: 30px;
}
.logo-bmw {
  width: 91.98px;
  height: 91.98px;
  padding-top: 30px;
}
.mobile-header-button {
  display: none;
}
.mobile-telefone-header {
  display: none;
}
@media screen and (max-width: 600px) {
  .header {
    width: 100%;
    height: 105px;
    justify-content: center;
    flex-direction: column;
  }
  .header-conteudo-container {
    display: none;
  }
  .logo-bmw {
    width: 34.5px;
    height: 34.5px;
    padding-top: 13px;
    padding-bottom: 12.5px;
  }
  .mobile-header-button {
    display: flex;
  }
  .mobile-telefone-header {
    display: flex;
    font-family: BMWTypeNext-Bold;
    font-size: 14px;
    color: #666666;
  }
  .mobile-icone-telefone {
    width: 19px;
    height: 19px;
    margin-right: 6px;
    filter: invert(39%) sepia(15%) saturate(16%) hue-rotate(64deg) brightness(95%) contrast(81%);
  }
  .mobile-header-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-right: 16px;
    margin-left: 16px;
  }
}
</style>
