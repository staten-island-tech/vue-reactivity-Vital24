<template>
  <section>
    <div
      :class="[Music]"
      id="Music"
      v-for="(Music, index) in Musics"
      :key="Music"
    >
      <h1 class="{{ Music.name }}">
        {{ index + 1 }}. {{ Music.name }} by {{ Music.artist }}
        <i
          @click="Consoling"
          style="font-size: 24px,color:red"
          :class="[Music.name, Music.artist]"
          >+</i
        >
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
    Musics: {
      type: Array,
    },
  },
  data() {
    return {
      Lists: [],
    };
  },

  methods: {
    Consoling: function () {
      if (this.Lists.includes(event.target.className)) {
        console.log(event.target.className);
      } else {
        this.Lists.push(event.target.className);
      }

      this.$emit("toParent", this.Lists);
    },
  },
};
</script>

<style scoped>
#Music {
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
