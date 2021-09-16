<template>
  <div class="d-flex justify-content-center">
    <FacultyCard
      v-for="(faculty, index) in faculties"
      :key="index"
      :logo="faculty.logo"
      :name="faculty.name"
      class="card col-2 p-4 border border-1 color-red"
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
        { logo: require("../assets/img/Gavel-v2.png"), name: "Law Faculty" },
        { logo: require("../assets/img/Coins-tabs-v2.png"), name: "Economy" },
        {
          logo: require("../assets/img/Medicine-tabs-v2.png"),
          name: "Medicine",
        },
        {
          logo: require("../assets/img/Computer-tabs-v2.png"),
          name: "Computer Scienze",
        },
        {
          logo: require("../assets/img/Palette-tabs-v2.png"),
          name: "Graphic Design",
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