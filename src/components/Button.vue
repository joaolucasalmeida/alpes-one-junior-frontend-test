<template>
    <button class="blue-button"> {{ textoBotao }} </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    textoBotao: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .blue-button {
        background-color: #1c69d4;
        width: 275px;
        height: 45px;
        color: white;
        border: none;
    }
</style>
