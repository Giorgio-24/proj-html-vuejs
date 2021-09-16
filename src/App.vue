<template>
  <div id="app">
    <header class="pt-5">
      <div class="container">
        <HeaderTop />
        <HeaderBottom />
      </div>
    </header>
    <main class="pt-5">
      <div class="container">
        <MainHeader class="row" />
      </div>
    </main>
    <footer class="pt-5">
      <div class="container"></div>
    </footer>
  </div>
</template>

<script>
import HeaderTop from "./components/HeaderTop.vue";
import HeaderBottom from "./components/HeaderBottom.vue";
import MainHeader from "./components/MainHeader.vue";

export default {
  name: "App",
  components: {
    HeaderTop,
    HeaderBottom,
    MainHeader,
  },
};
</script>

<style lang="scss">
@import "assets/scss/_style.scss";
</style>
