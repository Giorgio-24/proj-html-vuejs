<template>
  <div id="header-top" class="row">
    <div class="img-box h-100 col-3 clickable">
      <img class="h-100" :src="logo" alt="EduPrime-logo" />
    </div>
    <nav class="text-white d-flex col-9 justify-content-end">
      <ul class="d-flex align-items-center my-0 mx-2">
        <li
          class="fw-bold"
          v-for="(element, index) in navElements"
          :key="index"
        >
          <a
            class="px-3"
            :class="element.active === true ? 'color-yellow' : 'text-white'"
            href="#"
            >{{ element.name
            }}<i
              v-if="element.hasList === true"
              class="ps-1 fas fa-caret-down"
            ></i
          ></a>
        </li>
      </ul>
      <a
        href="#"
        class="
          big-button
          d-flex
          align-items-center
          bg-yellow
          text-white text-uppercase
        "
        >View courses</a
      >
    </nav>
  </div>
</template>

<script>
export default {
  name: "HeaderTop",
  props: ["navElements"],
  data() {
    return {
      logo: require("../assets/img/theme_eduprime_logo.png"),
    };
  },
};
</script>

<style lang="scss" scoped>
#header-top {
  height: 65px;
}
</style>