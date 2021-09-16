<template>
  <div id="app">
    <header class="pt-5">
      <div class="container">
        <HeaderTop :navElements="navElements" />
        <HeaderBottom />
      </div>
    </header>
    <main class="pt-5">
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
      <section class="bg-color-primary py-5">
        <div class="container">
          <UniYear />
          <Events />
        </div>
      </section>
    </main>
    <footer class="pt-5">
      <div class="container"></div>
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
    };
  },
};
</script>

<style lang="scss">
@import "assets/scss/_style.scss";
</style>
