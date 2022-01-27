<template>
  <div class="form-container">
    <Input labelInput="Nome" />
    <Input labelInput="E-mail" />
    <Input labelInput="Telefone" />
    <Input labelInput="Modelo" />
    <Input labelInput="Mensagem" />
    <input type="checkbox">
    <label> Aceito a política de privacidade</label><br>
    <Button textoBotao="Enviar" />
  </div>
</template>
<script>
import Input from "../components/Input.vue";
import Button from "../components/Button.vue";

export default {
  name: "Form",
  components: {
    Input,
    Button,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .form-container {
        display: flex;
        flex-direction: column;
    }
</style>
