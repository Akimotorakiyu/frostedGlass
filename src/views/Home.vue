<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <h3>默认</h3>
    <FrostedGlass image="/assets/bg-1.png" />
    <h3>使用插槽</h3>
    <FrostedGlass image="/assets/bg-1.png">你好世界</FrostedGlass>
    <h3>inline-block</h3>
    <FrostedGlass image="/assets/bg-1.png" class="block">你好世界</FrostedGlass>
  </div>
</template>

<script>
// @ is an alias to /src
import FrostedGlass from "@/components/FrostedGlass.vue";

export default {
  name: "Home",
  components: {
    FrostedGlass
  }
};
</script>

<style lang="stylus" scoped>
.block {
  display: inline-block;
  width: 200px;
  height: 200px;
  border-radius: 1em;
}
</style>