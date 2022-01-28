<template>
  <span class="dot" style="background-color: #1c69d4"></span>
  <span class="dot" style="background-color: #e6e6e6"></span>
  <span class="dot" style="background-color: #e6e6e6"></span>
</template>
<script>
export default {
  name: "CarouselNavigations",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.dot {
  height: 14px;
  width: 14px;
  margin-right: 10px;
  border-radius: 50%;
  display: inline-block;
  cursor: pointer;
}
</style>
