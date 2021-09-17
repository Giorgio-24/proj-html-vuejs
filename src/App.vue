<template>
  <div id="app">
    <header class="pt-5">
      <div class="container">
        <HeaderTop :navElements="navElements" />
        <HeaderBottom />
      </div>
    </header>
    <main class="pt-5">
      <section>
        <div class="container">
          <MainHeader class="row mb-5" />
          <Faculties class="row my-5" />
        </div>
        <div class="container-fluid">
          <FacultiesList class="row" />
        </div>
        <div class="container py-4">
          <SelectedFaculty />
        </div>
      </section>
      <section class="bg-color-primary py-5">
        <div class="container">
          <UniYear />
          <Events />
        </div>
      </section>
      <section class="container py-5">
        <Courses class="row" />
        <CoursesDetails class="row mt-5" />
      </section>
      <div class="container-fluid bg-color-primary py-5">
        <Subscribe />
      </div>
      <section class="container py-5">
        <Partners />
      </section>
    </main>
    <footer class="py-5 bg-color-primary position-relative">
      <div class="container">
        <FooterContent
          :footerList="footerList"
          :footerCategories="footerCategories"
        />
      </div>
    </footer>
  </div>
</template>

<script>
import HeaderTop from "./components/HeaderTop.vue";
import HeaderBottom from "./components/HeaderBottom.vue";
import MainHeader from "./components/MainHeader.vue";
import Faculties from "./components/Faculties.vue";
import FacultiesList from "./components/FacultiesList.vue";
import SelectedFaculty from "./components/SelectedFaculty.vue";
import UniYear from "./components/UniYear.vue";
import Events from "./components/Events.vue";
import Courses from "./components/Courses.vue";
import CoursesDetails from "./components/CoursesDetails.vue";
import Subscribe from "./components/Subscribe.vue";
import Partners from "./components/Partners.vue";
import FooterContent from "./components/FooterContent.vue";

export default {
  name: "App",
  components: {
    HeaderTop,
    HeaderBottom,
    MainHeader,
    Faculties,
    FacultiesList,
    SelectedFaculty,
    UniYear,
    Events,
    Courses,
    CoursesDetails,
    Subscribe,
    Partners,
    FooterContent,
  },
  data() {
    return {
      navElements: [
        { name: "Home", hasList: true, active: true },
        { name: "Courses", hasList: true, active: false },
        { name: "About Us", hasList: false, active: false },
        { name: "News", hasList: true, active: false },
        { name: "Pages", hasList: true, active: false },
        { name: "Contact", hasList: false, active: false },
        { name: "Purchase", hasList: false, active: false },
      ],
      footerList: [
        {
          listTitle: "Get Eduprime",
          listItems: [
            "Request a website",
            "Browse Themes",
            "Payment options",
            "Support System",
            "Checkout",
            "Purchase Theme",
          ],
        },
        {
          listTitle: "Networking",
          listItems: [
            "Purchase Theme",
            "Our Benefits",
            "Our team",
            "Our services",
            "Other Products",
            "My account",
          ],
        },
      ],
      footerCategories: [
        { name: "economy" },
        { name: "design" },
        { name: "coaching" },
        { name: "business" },
        { name: "medicine" },
        { name: "law" },
        { name: "fitness" },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "assets/scss/_style.scss";
</style>
