<template>
  <div>
    <div class="img-box m-auto mb-3">
      <img
        class="img-fluid"
        :class="active === true ? 'img-white' : 'image-primary'"
        :src="logo"
        :alt="`${name}-logo`"
      />
    </div>
    <div class="text-center">{{ name }}</div>
  </div>
</template>

<script>
export default {
  name: "FacultyCard",
  props: ["logo", "name", "active"],
};
</script>

<style lang="scss" scoped>
.img-box {
  max-width: 100px;
}
.img-white {
  filter: brightness(0) invert(1);
}
</style>