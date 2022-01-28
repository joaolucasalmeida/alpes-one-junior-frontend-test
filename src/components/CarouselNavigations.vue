<template>
  <span class="dot" style="background-color: #1C69D4"></span>
  <span class="dot" style="background-color: #E6E6E6"></span>
  <span class="dot" style="background-color: #E6E6E6"></span>
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
