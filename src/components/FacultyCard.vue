<template>
  <div>
    <div class="img-box m-auto mb-3">
      <img class="img-fluid" :src="logo" :alt="`${name}-logo`" />
    </div>
    <div class="text-center">{{ name }}</div>
  </div>
</template>

<script>
export default {
  name: "FacultyCard",
  props: ["logo", "name"],
};
</script>

<style lang="scss" scoped>
.img-box {
  max-width: 100px;
}
</style>