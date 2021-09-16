<template>
  <div>
    <div class="col-12 mt-5 py-5">
      <Paragraph
        v-for="(paragraph, index) in paragraphs"
        :key="index"
        class="mb-5"
        :icon="paragraph.icon"
        :title="paragraph.title"
        :paragraph="paragraph.paragraph"
        :buttonText="paragraph.buttonText"
        :buttonColor="paragraph.buttonColor"
        :illustration="paragraph.illustration"
        :invert="paragraph.invert"
      />
    </div>
  </div>
</template>

<script>
import Paragraph from "./Paragraph.vue";
export default {
  name: "CoursesDetails",
  components: {
    Paragraph,
  },
  data() {
    return {
      paragraphs: [
        {
          icon: require("../assets/img/Exam-icon.png"),
          title: "The most efficient examination method",
          paragraph:
            "EduPrime has gathered teahcers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teacher from our university has an influence on how students are evaluated at his/her Subject.",
          buttonText: "Discover the Method",
          buttonColor: "bg-color-primary",
          illustration: require("../assets/img/Exam-Illustration.png"),
          invert: false,
        },
        {
          icon: require("../assets/img/Exam-icon-1.png"),
          title: "Variable fees for international students",
          paragraph:
            "EduPrime has gathered teahcers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teacher from our university has an influence on how students are evaluated at his/her Subject.",
          buttonText: "List of Fees",
          buttonColor: "bg-color-primary",
          illustration: require("../assets/img/Girl-Illustration.png"),
          invert: true,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
</style>