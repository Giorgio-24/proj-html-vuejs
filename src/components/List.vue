<template>
  <div>
    <h4 class="mb-4">{{ listTitle }}</h4>
    <ul class="p-0">
      <li class="py-2" v-for="(item, index) in listItems" :key="index">
        <a class="text-white" href="#">{{ item }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "List",
  props: ["listTitle", "listItems"],
};
</script>

<style>
h4 {
  font-family: "Fredoka One", cursive;
}
</style>