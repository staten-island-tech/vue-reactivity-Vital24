<template>
  <h1>PlayList</h1>

  <h1 v-for="Music in Lists" :key="Music">{{ Music }}</h1>
</template>

<script>
import Music from "./Music.vue";
export default {
  name: "PlayList",
  components: {
    // Music,
  },
  data() {
    return {};
  },
  props: {
    Lists: {
      type: Array,
    },
  },
};
</script>

<style scoped></style>
