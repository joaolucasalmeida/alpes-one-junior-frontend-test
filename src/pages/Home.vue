<template>
  <div class="home-container">
    <Header />
    <div class="hideFormOnMobile">
      <Form />
    </div>
    <Banner />
    <h1 class="titulo-lista-carros">ESCOLHA SEU BMW</h1>
    <div class="cards-container">
      <Card
        marcaDoCarro="BMW Serie 1"
        imagemDoCarro="imgs\veiculos\serie1.png"
      />
      <Card
        marcaDoCarro="BMW M3 Competition"
        imagemDoCarro="imgs\veiculos\m3.png"
      />
      <Card marcaDoCarro="BMW M5" imagemDoCarro="imgs\veiculos\m5.png" />
      <Card marcaDoCarro="BMW X2" imagemDoCarro="imgs\veiculos\x2.png" />
      <Card
        marcaDoCarro="BMW Serie 4"
        imagemDoCarro="imgs\veiculos\serie-4.png"
      />
      <Card
        marcaDoCarro="BMW Serie 3"
        imagemDoCarro="imgs\veiculos\serie-3.png"
      />
      <Card marcaDoCarro="BMW Z4" imagemDoCarro="imgs\veiculos\z4.png" />
      <Card
        marcaDoCarro="BMW Serie 2"
        imagemDoCarro="imgs\veiculos\serie2.png"
      />
    </div>
    <Footer />
    <button class="whatsapp-button">
      <img class="whatsapp-icone" src="icons\svg\whatsapp.svg" alt="whatsapp" />
    </button>
  </div>
</template>

<script>
import Header from "../components/Header.vue";
import Card from "../components/Card.vue";
import Banner from "../components/Banner.vue";
import Form from "../components/Form.vue";
import Footer from "../components/Footer.vue";

export default {
  name: "Home",
  components: {
    Header,
    Banner,
    Card,
    Form,
    Footer,
  },
};
</script>

<style>
.home-container {
  min-width: 380px;
}
.titulo-lista-carros {
  font-family: BMWTypeNext-Light;
  font-size: 40px;
  font-weight: 100;
  margin-top: 80px;
  margin-bottom: 61px;
  margin-left: 788px;
  width: 397px;
}
.cards-container {
  display: flex;
  flex-flow: row wrap;
  width: 1400px;
  margin-left: 285px;
}

.whatsapp-button {
  display: none;
}

/* On screens that are 600px wide or less, make the cards stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .cards-container {
    width: 100%;
    margin-left: 0;
    justify-content: center;
  }
  .titulo-lista-carros {
    margin-left: 0;
    font-size: 20px;
    display: flex;
    justify-content: center;
    width: 100%;
  }
  .hideFormOnMobile {
    display: none;
  }
  .whatsapp-icone {
    width: 36px;
    height: 36px;
    filter: invert(100%) sepia(0%) saturate(7470%) hue-rotate(116deg)
      brightness(109%) contrast(109%);
  }

  .whatsapp-button {
    display: block;
    background-color: #25d366;
    width: 63px;
    height: 63px;
    border: none;
    border-radius: 50%;
    box-shadow: 0px 10px 20px #00000029;
    position: fixed;
    bottom: 16px;
    left: 16px;
  }
}
</style>
