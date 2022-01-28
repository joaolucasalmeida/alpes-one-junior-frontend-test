<template>
  <button
    class="botao-estilo-padrao"
    :style="{ backgroundColor: color, width: width + 'px' }"
  >
    <div class="container-conteudo-botao">
        <img class="icone-botao" :src="icone" alt="icone" />
        {{ textoBotao }}
    </div>
  </button>
</template>

<script>
export default {
  name: "HeaderButton",
  props: {
    textoBotao: String,
    width: String,
    color: String,
    icone: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.botao-estilo-padrao {
  background-color: black;
  width: 165px;
  height: 43px;
  color: white;
  border: none;
  cursor: pointer;
  font-family: BMWTypeNext-Bold;
  font-size: 14px;
  margin-right: 30px;
  margin-bottom: 30px;
}
.botao-estilo-padrao:hover {
  filter: brightness(90%);
}
.icone-botao {
    width: 19px;
    height: 19px;
    filter: invert(100%) sepia(0%) saturate(7483%) hue-rotate(96deg) brightness(111%) contrast(101%);
}
.container-conteudo-botao {
    display: flex;
    justify-content: space-evenly;
}

</style>
