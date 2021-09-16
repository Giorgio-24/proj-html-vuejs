<template>
  <div class="row">
    <div class="col-1 mx-auto text-center">
      <img
        class="img-fluid"
        src="../assets/img/Clock-and-Bell.png"
        alt="clock-and-bell"
      />
    </div>
    <h2 class="mt-3 col-12 text-center font-35 text-white">
      <span>University Year</span>
    </h2>
    <Timeline />
  </div>
</template>

<script>
import Timeline from "./Timeline.vue";
export default {
  name: "UniYear",
  components: {
    Timeline,
  },
};
</script>

<style lang="scss" scoped>
h2 {
  span {
    background-color: $bg-dark-green;
  }
}
</style>