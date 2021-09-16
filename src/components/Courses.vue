<template>
  <div>
    <h2 class="col-12 font-35 my-5">Latest Courses</h2>
    <div class="col-12">
      <div class="row">
        <CoursesCard
          class="col-3"
          v-for="(course, index) in courses"
          :key="index"
          :icon="course.icon"
          :title="course.title"
          :teacher="course.teacher"
          :price="course.price"
          :buttonText="course.buttonText"
          :buttonColor="course.buttonColor"
        />
      </div>
    </div>
  </div>
</template>

<script>
import CoursesCard from "./CoursesCard";
export default {
  name: "Courses",
  components: {
    CoursesCard,
  },
  data() {
    return {
      courses: [
        {
          icon: require("../assets/img/Decisions-icon.png"),
          title: "Make Better decision",
          teacher: "James Colins",
          price: "$21.00",
          buttonText: "View Course",
          buttonColor: "bg-color-primary",
        },
        {
          icon: require("../assets/img/Speaker-icon.png"),
          title: "How to be a speaker",
          teacher: "James Colins",
          price: "Free",
          buttonText: "View Course",
          buttonColor: "bg-color-primary",
        },
        {
          icon: require("../assets/img/Network-icon.png"),
          title: "Network introductions",
          teacher: "James Colins",
          price: "Free",
          buttonText: "View Course",
          buttonColor: "bg-color-primary",
        },
        {
          icon: require("../assets/img/Brand-icon.png"),
          title: "Brand management",
          teacher: "James Colins",
          price: "Free",
          buttonText: "View Course",
          buttonColor: "bg-color-primary",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
</style>