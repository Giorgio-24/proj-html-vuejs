<template>
  <div class="col-6">
    <div class="row">
      <div class="col-1 icon-box">
        <img class="img-fluid" :src="icon" alt="icon" />
      </div>
      <h2 class="col-11 fw-bold font-35 mt-3 mb-5">{{ title }}</h2>
      <p class="col-11 mb-5">{{ paragraph }}</p>
      <div class="col-11 mt-4">
        <a href="#" :class="buttonColor" class="big-button text-white">{{
          buttonText
        }}</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Paragraph",
  props: ["icon", "title", "paragraph", "buttonText", "buttonColor"],
};
</script>

<style lang="scss" scoped>
.icon-box {
  width: 72px;
}
</style>