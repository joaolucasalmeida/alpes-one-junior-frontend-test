<template>
    <button @click="$emit('click-menu')" class="botao-estilo-padrao"> {{ textoBotao }} </button>
</template>

<script>
export default {
  name: 'MenuButton',
  props: {
    textoBotao: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .botao-estilo-padrao {
        background-color: white;
        width: fit-content;
        height: fit-content;
        color: #666666;
        border: none;
        cursor: pointer;
        font-family: BMWTypeNext-Bold;
        font-size: 14px;
        margin-right: 58px;
    }
</style>
