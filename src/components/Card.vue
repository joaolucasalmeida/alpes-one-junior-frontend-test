<template>
  <div class="card-container">
    <img :src="imagemDoCarro" alt="Imagem do carro">
    <div class="marcaDoCarro">{{ marcaDoCarro }}</div>
    <div v-if="!esconderBotaoCotacao">
      <Button textoBotao="Cotação"/>
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
    esconderBotaoCotacao: Boolean
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
        margin-left: 20px;
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
        margin-left: 20px;
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
    @media screen and (max-width: 600px) {
      .card-container {
        margin-right: 0px;
      }
    }
</style>
