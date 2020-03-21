<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <h1>Default</h1>
    <FrostedGlass image="/assets/bg-1.png" />
    <h1>Slot</h1>
    <FrostedGlass image="/assets/bg-1.png">
      <h2>Hello world</h2>
    </FrostedGlass>
    <h1>Inline-block</h1>
    <FrostedGlass image="/assets/bg-1.png" class="block">
      <h2>Hello world</h2>
    </FrostedGlass>
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