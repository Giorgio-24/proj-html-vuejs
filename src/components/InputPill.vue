<template>
  <div class="d-flex">
    <input
      class="border-0 p-4 rounded-pill"
      :class="columnClass"
      :type="type"
      :placeholder="placeholder"
    />
    <div
      class="icon-button rounded-circle text-white position-relative"
      :class="buttonColor"
    >
      <i class="fa-2x p-4 rounded-circle" :class="buttonIcon"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: "InputPill",
  props: ["type", "placeholder", "buttonColor", "buttonIcon", "columnClass"],
};
</script>

<style lang="scss" scoped>
input {
  outline: none;
}
.icon-button {
  right: 75px;
}
</style>