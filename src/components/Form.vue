<template>
  <div class="form-container">
    <div class="titulo-form-container">
      <img
        class="carro-icone-form"
        src="icons/svg/carro.svg"
        alt="icone formulario"
      />
      <div class="titulo-form">Solicitar cotação</div>
    </div>
    <Input labelInput="Nome" />
    <Input labelInput="E-mail" />
    <Input labelInput="Telefone" />
    <Input labelInput="Modelo" />
    <Input labelInput="Mensagem" />
    <Checkbox />
    <Button width="215px" textoBotao="Enviar" />
  </div>
</template>
<script>
import Input from "../components/Input.vue";
import Button from "../components/Button.vue";
import Checkbox from "../components/Checkbox.vue";

export default {
  name: "Form",
  components: {
    Input,
    Button,
    Checkbox,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .form-container {
    position: absolute;
    margin-left: 1370px;
    margin-top: 30px;
    display: flex;
    justify-content: center;
    flex-direction: column;
    width: 255px;
    height: 478px;
    align-items: center;
    background-color: white;
    border-style: outset;
    border-width: 1px;
  }
  .titulo-form {
    font-family: BMWTypeNext-Light;
    font-size: 20px;
  }
  .carro-icone-form {
    width: 23px;
    height: 23px;
    filter: invert(26%) sepia(37%) saturate(5993%) hue-rotate(209deg)
      brightness(93%) contrast(78%);
    margin-top: 3px;
    margin-right: 10px;
  }
  .titulo-form-container {
    display: flex;
  }
  @media screen and (max-width: 600px) {
    .form-container {
      margin: 0;
      width: 100%;
      min-width: 380px;
    }
  }
</style>
