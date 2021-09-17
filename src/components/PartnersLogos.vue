<template>
  <div class="h-100 d-flex justify-content-center" :class="column">
    <img class="img-fluid" :class="imgClass" :src="image" alt="partner-logo" />
  </div>
</template>

<script>
export default {
  name: "PartnersLogos",
  props: ["column", "image", "imgClass"],
};
</script>

<style lang="scss" scoped>
.max-dimentions {
  max-width: 58px;
  max-height: 43px;
}
</style>