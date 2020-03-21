<template>
  <div class="__frosted-glass-wrap-box__">
    <div class="window-glass" :style="style_window_glass">
      <span></span>
    </div>
    <slot>
      <h2>{{ msg }}</h2>
    </slot>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  name: "FrostedGlass",
  props: {
    msg: {
      type: String,
      default: "frosted-glass"
    },
    blur: {
      type: String,
      default: "36px"
    },
    image: {
      type: String,
      required: true
    }
  },
  computed: {
    style_window_glass() {
      return {
        filter: `blur(${this.blur})`,
        background: `url(${this.image})`
      };
    }
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
.__frosted-glass-wrap-box__ {
  overflow: hidden;
  position: relative;
  border-radius: 1em;

  .window-glass {
    // filter: blur(36px);
    // background: url('./assets/bg-1.png');
    position: absolute;
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
