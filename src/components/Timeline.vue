<template>
  <div class="col-12 my-5">
    <div class="row text-white">
      <div class="col-4 offset-3 text-center">
        <h5>Demo Classes</h5>
        <span
          >In the first week, students try to accomodate with the teaching style
          and choose their optional courses.</span
        >
      </div>
      <div class="col-4 text-center">
        <h5>Graduation Day</h5>
        <span
          >On the day of graduation, all students gather for the ceremony and
          then network and party among others.</span
        >
      </div>
      <div class="col-10 mx-auto">
        <img
          class="img-fluid"
          src="../assets/img/Timeline-Item.png"
          alt="timeline-image"
        />
      </div>
      <div class="col-4 offset-1 text-center">
        <h5>Orientation</h5>
        <span
          >First day of the university year, all students gather for the
          ceremony and then network and party among others.</span
        >
      </div>
      <div class="col-4 text-center">
        <h5>Evaluation</h5>
        <span
          >At the end of a semester, students take a general evaluation test for
          every subject they're learning.</span
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Timeline",
};
</script>

<style lang="scss" scoped>
.row {
  h5 {
    font-family: "Fredoka One", cursive;
  }
}
</style>