# frosted-glass

![usage](usage.png)

## Usage

```sh
npm install vue-frosted-glass
```

**notice**
|属性|描述|值类型|默认|
|---|---|---|---|
|image|磨砂背景的源图|图片路径|-|
|blur|高斯模糊的值|px、em...|36px|

```vue
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
    <FrostedGlass image="/assets/bg-1.png" class="inline-block">
      <h2>Hello world</h2>
    </FrostedGlass>
  </div>
</template>

<script>
import FrostedGlass from "vue-frosted-glass";
import "vue-frosted-glass/dist/VueFrostedGlass.css";

export default {
  name: "Home",
  components: {
    FrostedGlass
  }
};
</script>

<style lang="stylus" scoped>
.inline-block {
  display: inline-block;
  width: 400px;
  height: 400px;
  border-radius: 1em;
}
</style>
```

## LICENSE

MIT
