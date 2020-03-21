<template>
  <div class="__frosted-glass-wrap-box__">
    <div class="window-glass">
      <span></span>
    </div>
    <div class="content">
      <h1>{{ msg }}</h1>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "HelloWorld",
  props: {
    msg: String,
    display: {
      type: String,
      default: "inline-block"
    },
    blur: {
      type: String,
      default: "36px"
    },
    image: {
      type: String,
      default: "./assets/bg-1.png"
    }
  },
  computed: {
    style_wrap_box_() {}
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
.__frosted-glass-wrap-box__ {
  overflow: hidden;
  position: relative;

  .window-glass {
    filter: blur(36px);
    position: absolute;
    background: url('./assets/bg-1.png');
    background-position: center;
    background-size: cover;
    z-index: -1;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
  }

  .content, .window-glass {
    height: 100%;
    width: 100%;
  }

  .content {
  }
}
</style>
