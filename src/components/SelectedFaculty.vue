<template>
  <Paragraph
    class="mt-5"
    :title="title"
    :paragraph="paragraph"
    :buttonText="buttonText"
    :buttonColor="buttonColor"
    :illustration="illustration"
    :invert="invert"
  />
</template>

<script>
import Paragraph from "./Paragraph.vue";
export default {
  name: "SelectedFaculty",
  components: {
    Paragraph,
  },
  data() {
    return {
      title: "Law Faculty",
      paragraph:
        "Learning from world-leading academics and practitioners, you'll not only receive an outstanding grounding in the theory of law, but you will be able to understand how those principles are applied in practice through a range of student-led activities and competitions.",
      buttonText: "Read More",
      buttonColor: "bg-color-primary",
      illustration: require("../assets/img/Gavel-Illustration-e1556884768193.png"),
      invert: true,
    };
  },
};
</script>

<style lang="scss" scoped>
</style>