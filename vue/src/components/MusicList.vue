<template>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"
  />
  <PlayList v-bind:Lists="Lists"></PlayList>
  <div>
    <div :class="[Music]" v-for="(Music, index) in Musics" :key="Music">
      <h1 class="{{ Music.name }}">
        {{ index + 1 }}. {{ Music.name }} by {{ Music.artist }}
        <i
          @click="Consoling"
          style="font-size: 24px,color:red"
          :class="[Music.name, Music.artist]"
          >&#xf067;</i
        >
      </h1>
    </div>
  </div>
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
      console.log(this.Lists);
      this.$emit("toParent", this.Lists);
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
