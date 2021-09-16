<template>
  <div class="course-card text-center mx-3 py-5 position-relative">
    <div class="icon-box mx-auto mb-4">
      <img class="img-fluid image-primary" :src="icon" alt="course-icon" />
    </div>
    <h5>{{ title }}</h5>
    <div class="my-3">
      <i class="far fa-user"></i>Teacher: <strong>{{ teacher }}</strong>
    </div>
    <div class="mb-1">
      <i class="far fa-money-bill-alt"></i>Price: <strong>{{ price }}</strong>
    </div>
    <a
      class="small-button text-white position-absolute"
      :class="buttonColor"
      href="#"
      ><i class="far fa-eye"></i>{{ buttonText }}</a
    >
  </div>
</template>

<script>
export default {
  name: "CoursesCard",
  props: ["icon", "title", "teacher", "price", "buttonText", "buttonColor"],
};
</script>

<style lang="scss" scoped>
.course-card {
  box-shadow: 0px 0px 75px -30px #d3d3d3;
  max-width: 22%;
  .icon-box {
    max-width: 70px;
  }
  h5 {
    font-family: "Fredoka One", cursive;
  }
  a {
    left: 50%;
    bottom: 0;
    transform: translate(-50%, 50%);
    min-width: 56%;
  }
}
</style>