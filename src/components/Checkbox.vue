<template>
  <div class="checkbox-container">
    <input type="checkbox" class="input-checkbox" />
    <label class="label-checkbox">
      Aceito a
      <span class="label-checkbox-bold">Política de Privacidade.</span></label
    >
  </div>
</template>
<script>
export default {
  name: "Checkbox",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.checkbox-container {
  display: flex;
  width: 203px;
  align-items: center;
  margin-top: 16px;
  margin-bottom: 16px;
}
.label-checkbox {
  font-family: BMWTypeNext-Light;
  font-size: 12px;
  color: #bbbbbb;
}
.label-checkbox-bold {
  font-family: BMWTypeNext-Bold;
  font-size: 12px;
  color: #666666;
}
.input-checkbox {
  cursor: pointer;
}
</style>
