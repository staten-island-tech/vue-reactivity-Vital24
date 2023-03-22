<template>
  <section>
    <div class="Music">
      <h1>Personal Playlist</h1>
      <h1 v-for="(Music, index) in AddedMusic" :key="Music">
        {{ index + 1 }} {{ Music }}
        <button :class="[Music]" @click="RemoveMusic">
          Remove from Playlist
        </button>
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
    AddedMusic: {
      type: Array,
    },
  },
  methods: {
    value:



    NewList = AddedMusic.filter(item => item !== )

    console.log(arr)
    RemoveMusic(event) {
      event.target.parentElement.remove();

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
