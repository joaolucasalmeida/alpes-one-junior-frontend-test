<template>
  <div class="card-container">
    <img class="imagem-do-carro" :src="imagemDoCarro" alt="Imagem do carro">
    <div class="marcaDoCarro">{{ marcaDoCarro }}</div>
    <div class="container-button-card">
      <div v-if="!esconderBotaoCotacao" class="margin-right">
        <Button textoBotao="Cotação"/>
      </div>
      <div class="exibir-botao-ligar">
        <Button textoBotao="Ligar" color="#666666"/>
      </div>
    </div>
    <div class="compartilhe-container">
        <span class="compartilhe-texto">Compartilhe: </span> 
        <img class="compartilhe-icones" src="icons\svg\facebook.svg" alt="facebook">
        <img class="compartilhe-icones" src="icons\svg\whatsapp.svg" alt="whatsapp">
    </div>
  </div>
</template>

<script>
import Button from './Button.vue'
export default {
  name: 'Card',
  components: {
    Button,
  },
  props: {
    imagemDoCarro: String,
    marcaDoCarro: String,
    esconderBotaoCotacao: Boolean,
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .card-container {
        width: 315px;
        height: 363px;
        text-align: center;
        margin-right: 30px;
        margin-bottom: 30px;
    }
    .marcaDoCarro {
        margin-top: 16px;
        margin-bottom: 29px;
        text-align: left;
        font-family: BMWTypeNext-Light;
        font-size: 20px;
    }
    .compartilhe-texto {
        font-family: BMWTypeNext-Light;
        font-size: 12px;
    }
    .compartilhe-container {
        display: flex;
        height: 24px;
        margin-left: 2px;
        margin-top: 30px;
        align-items: center;
    }
    .compartilhe-icones {
        width: 24px;
        height: 24px;
        margin-left: 16px;
        filter: invert(42%) sepia(0%) saturate(531%) hue-rotate(245deg) brightness(88%) contrast(75%);
        cursor: pointer;
    }
    .compartilhe-icones:hover {
      filter: invert(45%) sepia(90%) saturate(4924%) hue-rotate(204deg) brightness(88%) contrast(89%);
    }
    .container-button-card {
      display: flex;
    }
    .exibir-botao-ligar {
      display: none;
    }
    .imagem-do-carro:hover {
      opacity: 0.5;
      cursor: pointer;
    }
    .margin-right {
      margin-right: 16px;
    }
    @media screen and (max-width: 600px) {
      .card-container {
        margin-right: 0px;
      }
      .exibir-botao-ligar {
        display: flex;
      }
    }
</style>
