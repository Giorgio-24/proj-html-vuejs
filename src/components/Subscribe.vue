<template>
  <div class="row align-items-center justify-content-center">
    <h2 class="col-5 text-white text-end">Subscribe now to Our Newsletter!</h2>
    <div class="col-6 offset-1">
      <InputPill
        :type="input.type"
        :placeholder="input.placeholder"
        :buttonColor="input.buttonColor"
        :buttonIcon="input.buttonIcon"
        :columnClass="input.columnClass"
      />
    </div>
  </div>
</template>

<script>
import InputPill from "./InputPill.vue";
export default {
  name: "Subscribe",
  components: {
    InputPill,
  },
  data() {
    return {
      input: {
        type: "email",
        placeholder: "Email address...",
        buttonColor: "bg-yellow",
        buttonIcon: "fab fa-telegram-plane",
        columnClass: "col-7",
      },
    };
  },
};
</script>

<style lang="scss" scoped>
h2 {
  font-family: "Fredoka One", cursive;
}
</style>