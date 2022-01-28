<template>
  <button
    @click="$emit('click-event')"
    class="botao-estilo-padrao"
    :style="{ width: width, backgroundColor: color }"
  >
    {{ textoBotao }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    textoBotao: String,
    width: String,
    color: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.botao-estilo-padrao {
  background-color: #1c69d4;
  width: 275px;
  height: 45px;
  color: white;
  border: none;
  cursor: pointer;
  font-family: BMWTypeNext-Bold;
  font-size: 14px;
}
.botao-estilo-padrao:hover {
  filter: brightness(80%);
}
@media screen and (max-width: 600px) {
  .botao-estilo-padrao {
    width: 156px;
    height: 35px;
  }
}
</style>
