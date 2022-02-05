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
        <MenuButton @click-menu="clickMenu" textoBotao="1" />
        <MenuButton @click-menu="clickMenu" textoBotao="2" />
        <MenuButton @click-menu="clickMenu" textoBotao="3" />
        <MenuButton @click-menu="clickMenu" textoBotao="4" />
        <MenuButton @click-menu="clickMenu" textoBotao="5" />
        <MenuButton @click-menu="clickMenu" textoBotao="6" />
        <MenuButton @click-menu="clickMenu" textoBotao="7" />
        <MenuButton @click-menu="clickMenu" textoBotao="8" />
        <MenuButton @click-menu="clickMenu" textoBotao="X" />
        <MenuButton @click-menu="clickMenu" textoBotao="Z" />
        <MenuButton @click-menu="clickMenu" textoBotao="M" />
        <MenuButton @click-menu="clickMenu" textoBotao="i" />
        <MenuButton @click-menu="clickMenu" textoBotao="Plug-in-Hybrid" />
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
    <div v-if="showForm" class="mobile-header-button">
      <Button
        @click-event="clickEvent"
        textoBotao="Minimizar"
        width="100%"
        color="#666666"
      />
    </div>
    <div v-else class="mobile-header-button">
      <Button
        @click-event="clickEvent"
        textoBotao="Solicitar Cotação"
        width="100%"
      />
    </div>
    <div v-if="showForm">
      <Form />
    </div>
    <div v-if="showDropdown" class="dropdown-container">
      <img
        class="dropdown-setas"
        src="icons/svg/seta-a-esquerda.svg"
        alt="icone"
      />
      <Card
        marcaDoCarro="BMW Serie 1"
        imagemDoCarro="imgs\veiculos\serie1.png"
        :esconderBotaoCotacao="true"
      />
      <Card
        marcaDoCarro="BMW Serie 1"
        imagemDoCarro="imgs\veiculos\serie1.png"
        :esconderBotaoCotacao="true"
      />
      <Card
        marcaDoCarro="BMW Serie 1"
        imagemDoCarro="imgs\veiculos\serie1.png"
        :esconderBotaoCotacao="true"
      />
      <div class="carousel-container">
        <CarouselNavigations />
      </div>
      <img
        class="dropdown-setas"
        src="icons/svg/seta-a-direita.svg"
        alt="icone"
      />
    </div>
  </header>
</template>

<script>
import HeaderButton from "../components/HeaderButton.vue";
import MenuButton from "../components/MenuButton.vue";
import Button from "../components/Button.vue";
import Form from "../components/Form.vue";
import Card from "../components/Card.vue";
import CarouselNavigations from "../components/CarouselNavigations.vue";

export default {
  name: "Header",
  components: {
    HeaderButton,
    MenuButton,
    Button,
    Form,
    Card,
    CarouselNavigations,
  },
  data() {
    return {
      showForm: false,
      showDropdown: false,
    };
  },
  methods: {
    //Exibe formulario apos captura do evento de click no botao solitar
    clickEvent() {
      this.showForm = !this.showForm;
    },

    //Exibe dropdown do menu apos click no botao do menu
    clickMenu() {
      this.showDropdown = !this.showDropdown;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header {
  display: flex;
  justify-content: space-evenly;
  min-width: 1280px;
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
.dropdown-container {
  width: 100%;
  min-width: 1280px;
  height: 383px;
  background-color: white;
  position: absolute;
  z-index: 1;
  top: 149px;
  display: flex;
  justify-content: center;
  border-style: outset;
  border-width: 1px;
}
.dropdown-setas {
  width: 24px;
  height: 24px;
  filter: invert(39%) sepia(15%) saturate(16%) hue-rotate(64deg) brightness(95%)
    contrast(81%);
  margin-top: 158px;
  margin-right: 35px;
  margin-left: 35px;
  cursor: pointer;
}
.mobile-header-button {
  display: none;
}
.mobile-telefone-header {
  display: none;
}
.carousel-container {
  position: absolute;
  top: 340px;
}
@media screen and (max-width: 600px) {
  .header {
    width: 100%;
    min-width: 0;
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
    filter: invert(39%) sepia(15%) saturate(16%) hue-rotate(64deg)
      brightness(95%) contrast(81%);
  }
  .mobile-header-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-right: 16px;
    margin-left: 16px;
  }
  .dropdown-container {
    display: none;
  }
}
</style>
