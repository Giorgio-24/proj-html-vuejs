<template>
  <section class="row">
    <div class="col-4">
      <div class="row">
        <div class="col-10 logo-box clickable">
          <img class="img-fluid" :src="logo" alt="EduPrime-logo" />
        </div>
        <div class="col-12 text-white my-4">
          EduPrime is the most versatile WordPress theme for educational
          purposes, showcasing universities, courses, secondary schools etc.
        </div>
        <div class="col-6">
          <div class="row">
            <SocialLogo
              v-for="(socialIcon, index) in socialIcons"
              :key="index"
              :icon="socialIcon.icon"
              :borderStyle="socialIcon.borderStyle"
              class="col-3 clickable"
            />
          </div>
        </div>
      </div>
    </div>
    <div class="col-4">
      <div class="row text-white">
        <div v-for="(list, index) in footerList" :key="index" class="col-6">
          <List :listTitle="list.listTitle" :listItems="list.listItems" />
        </div>
      </div>
    </div>
    <div class="col-4"></div>
  </section>
</template>

<script>
import SocialLogo from "./SocialLogo.vue";
import List from "./List.vue";
export default {
  name: "FooterContent",
  components: {
    SocialLogo,
    List,
  },
  props: ["footerList"],
  data() {
    return {
      logo: require("../assets/img/theme_eduprime_logo.png"),
      socialIcons: [
        {
          icon: "fab fa-facebook-f",
          borderStyle: "border-yellow-circle",
        },
        {
          icon: "fab fa-twitter",
          borderStyle: "border-yellow-circle",
        },
        {
          icon: "fab fa-instagram",
          borderStyle: "border-yellow-circle",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
</style>