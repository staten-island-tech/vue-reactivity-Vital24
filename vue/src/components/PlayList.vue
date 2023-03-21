<template>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"
  />
  <section>
    <div class="Music">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
        <path
          d="M240 80c0-17.7-14.3-32-32-32s-32 14.3-32 32V224H32c-17.7 0-32 14.3-32 32s14.3 32 32 32H176V432c0 17.7 14.3 32 32 32s32-14.3 32-32V288H384c17.7 0 32-14.3 32-32s-14.3-32-32-32H240V80z"
        />
      </svg>
      <h1>Personal Playlist</h1>
      <h1 v-bind:Lists="Lists" v-for="(Music, index) in Pants" :key="Music">
        {{ index + 1 }} {{ Music }}
      </h1>
    </div>
  </section>
</template>

<script>
export default {
  name: "PlayList",

  data() {
    return {};
  },
  props: {
    Pants: {
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
svg {
  width: 25px;
}
</style>
