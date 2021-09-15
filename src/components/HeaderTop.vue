<template>
  <div>
    <div><img :src="logo" alt="EduPrime-logo" /></div>
    <nav></nav>
  </div>
</template>

<script>
export default {
  name: "HeaderTop",
  data() {
    return {
      logo: require("../assets/img/theme_eduprime_logo.png"),
    };
  },
};
</script>

<style lang="scss" scoped>
</style>