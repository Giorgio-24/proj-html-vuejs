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
    <div class="col-4">
      <div class="row">
        <InputPill
          :type="input.type"
          :placeholder="input.placeholder"
          :buttonColor="input.buttonColor"
          :buttonIcon="input.buttonIcon"
          :columnClass="input.columnClass"
        />
        <h5 class="col-12 text-white text-end mt-4">Search Categories</h5>
        <div class="col-12">
          <div class="row justify-content-end">
            <div
              v-for="(category, index) in footerCategories"
              :key="index"
              class="
                category
                my-2
                mx-1
                border
                rounded-pill
                text-uppercase
                d-flex
                text-center
                py-2
                px-2
              "
            >
              <a class="text-white mx-auto" href="#">{{ category.name }}</a>
            </div>
          </div>
        </div>
        <div class="mt-4 col-12 text-end color-yellow">
          ModelTheme. All rights reserved.
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import SocialLogo from "./SocialLogo.vue";
import List from "./List.vue";
import InputPill from "./InputPill.vue";
export default {
  name: "FooterContent",
  components: {
    SocialLogo,
    List,
    InputPill,
  },
  props: ["footerList", "footerCategories"],
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
      input: {
        type: "search",
        placeholder: "Search...",
        buttonColor: "bg-yellow",
        buttonIcon: "fas fa-search",
        columnClass: "col-12",
      },
    };
  },
};
</script>

<style lang="scss" scoped>
h5 {
  font-family: "Fredoka One", cursive;
}

.category {
  max-width: 98px;
}
</style>