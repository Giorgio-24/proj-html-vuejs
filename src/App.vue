<template>
  <div id="app">
    <header class="pt-5">
      <div class="container">
        <HeaderTop />
        <HeaderBottom />
      </div>
    </header>
    <main></main>
    <footer></footer>
  </div>
</template>

<script>
import HeaderTop from "./components/HeaderTop.vue";
import HeaderBottom from "./components/HeaderBottom.vue";

export default {
  name: "App",
  components: {
    HeaderTop,
    HeaderBottom,
  },
};
</script>

<style lang="scss">
@import "assets/scss/_style.scss";
</style>
