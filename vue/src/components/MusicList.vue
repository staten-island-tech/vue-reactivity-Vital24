<template>
  <section>
    <div
      :class="[Music]"
      id="Music"
      v-for="(Music, index) in Musics"
      :key="Music"
    >
      <h1>
        {{ index + 1 }}. {{ Music.name }} by {{ Music.artist }}
        <button
          @click="Consoling"
          style="font-size: 24px, color:red"
          :class="[Music.name, By, Music.artist]"
        >
          Add to Playlist
        </button>
      </h1>
    </div>
  </section>
</template>

<script>
import PlayList from "./PlayList.vue";

export default {
  Name: "MusicList",
  components: {
    PlayList,
  },
  props: {
    Lists: {
      type: Array,
    },
    Musics: {
      type: Array,
    },
  },
  data() {
    return {
      By: "by",
    };
  },

  methods: {
    Consoling: function () {
      if (this.Lists.includes(event.target.className)) {
      } else {
        this.Lists.push(event.target.className);
      }

      this.$emit("toParent", this.Lists);
    },
  },
};
</script>

<style scoped>
/* #Music {
  text-shadow: 1rem 1rem 2rem black;

  color: white;
  text-decoration: solid;
}

hr {
  color: white;
} */
</style>
