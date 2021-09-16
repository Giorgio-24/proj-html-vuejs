<template>
  <div class="d-flex justify-content-center">
    <FacultyCard
      v-for="(faculty, index) in faculties"
      :key="index"
      :logo="faculty.logo"
      :name="faculty.name"
      :active="faculty.active"
      class="card col-2 p-4 border border-1 color-primary"
      :class="
        faculty.active === true
          ? 'bg-color-primary text-white'
          : 'color-primary'
      "
    />
  </div>
</template>

<script>
import FacultyCard from "./FacultyCard.vue";
export default {
  name: "FacultiesList",
  components: {
    FacultyCard,
  },
  data() {
    return {
      faculties: [
        {
          logo: require("../assets/img/Gavel-v2.png"),
          name: "Law Faculty",
          active: true,
        },
        {
          logo: require("../assets/img/Coins-tabs-v2.png"),
          name: "Economy",
          active: false,
        },
        {
          logo: require("../assets/img/Medicine-tabs-v2.png"),
          name: "Medicine",
          active: false,
        },
        {
          logo: require("../assets/img/Computer-tabs-v2.png"),
          name: "Computer Scienze",
          active: false,
        },
        {
          logo: require("../assets/img/Palette-tabs-v2.png"),
          name: "Graphic Design",
          active: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
div {
  box-shadow: 0 1px 10px rgb(0 0 0 / 0.2);
  .card {
    max-width: 240px;
    font-family: "Fredoka One", cursive;
  }
}
</style>