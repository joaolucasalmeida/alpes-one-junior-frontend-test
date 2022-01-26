<template>
  <div class="card-container">
    <img :src="imagemDoCarro" alt="Imagem do carro">
    <div class="marcaDoCarro">{{ marcaDoCarro }}</div>
    <Button textoBotao="Cotação"/>
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
    marcaDoCarro: String
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .card-container {
        width: 315px;
        height: 363px;
        text-align: center;
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
        color: #666666;
    }
</style>
