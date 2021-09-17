<template>
  <div class="">
    <div
      class="dim-45 d-flex justify-content-center align-items-center text-white"
      :class="borderStyle"
    >
      <i :class="icon"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: "SocialLogo",
  props: ["icon", "borderStyle"],
};
</script>

<style lang="scss" scoped>
.dim-45 {
  height: 45px;
  width: 45px;
}

.border-yellow-circle {
  border: 2px solid $both-yellow;
  border-radius: 50%;
}
</style>