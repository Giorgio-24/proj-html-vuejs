<template>
  <section class="row py-5">
    <div
      v-for="(theme, index) in themes"
      :key="index"
      class="position-absolute themes py-2 px-3 rounded clickable"
    >
      <img v-if="theme.icon" :src="theme.icon" alt="theme-icon" />{{
        theme.text
      }}
    </div>
    <div class="col-4">
      <div class="row">
        <div class="col-9 logo-box clickable">
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
        <h5 class="col-12 text-white text-end mt-5 mb-4">Search Categories</h5>
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
    <a
      class="
        go-up
        text-white
        bg-yellow
        rounded-circle
        d-flex
        align-items-center
        justify-content-center
        position-absolute
      "
      href="#"
      ><i class="fas fa-angle-up"></i
    ></a>
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
      themes: [
        { icon: "", text: "Purachase Theme" },
        { icon: "", text: "Related Themes" },
      ],
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
.themes {
  background-color: $both-dark-grey;
  box-shadow: 0 13px 13px -8px #000;
  color: $border-grey;
  max-width: 160px;
  font-size: 14px;

  left: 30px;
  bottom: 30px;

  &:nth-of-type(1) {
    left: 30px;
    bottom: 85px;
  }
}

h5 {
  font-family: "Fredoka One", cursive;
}

.category {
  max-width: 98px;
  font-size: 14px;
}

.go-up {
  max-width: 40px;
  height: 40px;

  bottom: 40px;
  right: 30px;
  i {
    font-size: 24px;
  }
}
</style>