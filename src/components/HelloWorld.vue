<template>
  <div class="__frosted-glass-wrap-box__">
    <div class="window-glass">
      <h1>{{ msg }}</h1>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "HelloWorld",
  props: {
    msg: String
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
.__frosted-glass-wrap-box__ {
  margin: 100px;
  color: green;
  display: inline-block;
  overflow: hidden;
  position: relative;

  .window-glass {
    &, &::before {
      display: inline-block;
      height: 400px;
      width: 400px;
    }

    &::before {
      content: '';
      position: absolute;
      filter: blur(36px);
      background: url('./assets/bg-1.png');
      background-position: center;
      background-size: cover;
      z-index: -1;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
    }
  }
}
</style>
