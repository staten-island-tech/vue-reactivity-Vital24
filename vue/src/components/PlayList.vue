<template>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"
  />
  <h1>PlayList</h1>
  <div class="Music">
    <h1 v-bind:Lists="Lists" v-for="(Music, index) in Lists" :key="Music">
      {{ index + 1 }} {{ Music }}
    </h1>
  </div>
</template>

<script>
export default {
  name: "PlayList",

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

<style scoped>
.Music {
  text-shadow: 1rem 1rem 2rem black;

  color: white;
  text-decoration: solid;
}

hr {
  color: white;
}
</style>
