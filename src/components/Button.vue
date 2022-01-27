<template>
    <button class="botao-estilo-padrao" :style="{ width: width + 'px' }"> {{ textoBotao }} </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    textoBotao: String,
    width: String
  }
}
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
    }
</style>
