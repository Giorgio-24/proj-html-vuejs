<template>
  <div class="row">
    <h2 class="col-12 text-center font-35">Partners</h2>
    <div class="my-4 mx-auto col-5 text-center">
      Leverage agile frameworks to provide a robust synopsis for high level
      overviews. Iterative approaches to corporate strategy.
    </div>
    <div class="col-12 mt-2 mb-5">
      <div class="logos-row row align-items-center justify-content-center">
        <PartnersLogos
          v-for="(partner, index) in partners"
          :key="index"
          :column="partner.column"
          :image="partner.image"
          :imgClass="partner.imgClass"
        />
      </div>
    </div>
  </div>
</template>

<script>
import PartnersLogos from "./PartnersLogos.vue";
export default {
  name: "Partners",
  components: {
    PartnersLogos,
  },
  data() {
    return {
      partners: [
        {
          column: "col-2",
          imgClass: " image-grey",
          image: require("../assets/img/partner-2.png"),
        },
        {
          column: "col-1",
          imgClass: "max-dimentions image-grey",
          image: require("../assets/img/partner-3.png"),
        },
        {
          column: "col-1",
          imgClass: "max-dimentions image-grey",
          image: require("../assets/img/partner-4.png"),
        },
        {
          column: "col-2",
          imgClass: " image-grey",
          image: require("../assets/img/partner-5.png"),
        },
        {
          column: "col-1",
          imgClass: "max-dimentions image-grey",
          image: require("../assets/img/partner-6.png"),
        },
        {
          column: "col-1",
          imgClass: "max-dimentions image-grey",
          image: require("../assets/img/partner-8.png"),
        },
        {
          column: "col-1",
          imgClass: "max-dimentions image-grey",
          image: require("../assets/img/partner-1.png"),
        },
        {
          column: "col-2",
          imgClass: " image-grey",
          image: require("../assets/img/partner-7.png"),
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.logos-row {
  height: 43px;
}
</style>