<template>
  <div class="event-card col-3 py-4 px-5 bg-white mx-3 position-relative">
    <h4 class="mt-2">{{ title }}</h4>
    <div class="color-grey"><i class="far fa-calendar-alt"></i> {{ date }}</div>
    <div class="color-grey mb-4">{{ text }}</div>
    <a
      class="text-white position-absolute small-button"
      :class="buttonColor"
      href="#"
      >{{ buttonText }}</a
    >
  </div>
</template>

<script>
export default {
  name: "EventsCard",
  props: ["key", "title", "date", "text", "buttonText", "buttonColor"],
};
</script>

<style lang="scss" scoped>
.event-card {
  border-radius: 15px;
  a {
    left: 50%;
    transform: translateX(-50%);

    box-shadow: 0px 3px 8px -5px black;
  }
  .color-grey {
    color: $grey-blue;
  }
}
</style>