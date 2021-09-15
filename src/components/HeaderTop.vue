<template>
  <div id="header-top" class="row">
    <div class="img-box h-100 col-5 clickable">
      <img class="h-100" :src="logo" alt="EduPrime-logo" />
    </div>
    <nav class="text-white d-flex col-7">
      <ul class="d-flex align-items-center m-0">
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
    </nav>
  </div>
</template>

<script>
export default {
  name: "HeaderTop",
  data() {
    return {
      logo: require("../assets/img/theme_eduprime_logo.png"),
      navElements: [
        { name: "Home", hasList: true, active: true },
        { name: "Courses", hasList: true, active: false },
        { name: "About Us", hasList: false, active: false },
        { name: "News", hasList: true, active: false },
        { name: "Pages", hasList: true, active: false },
        { name: "Contact", hasList: false, active: false },
        { name: "Purchase", hasList: false, active: false },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
#header-top {
  height: 65px;
}
.color-yellow {
  color: $both-yellow;
}
</style>