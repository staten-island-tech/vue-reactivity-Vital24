<template>
  <h1 class="Header">Music</h1>
  <div class="Hidden">
    <div
      :class="[Music]"
      id="Music"
      v-for="(Music, index) in Musics"
      :key="Music"
    >
      <h2>
        {{ index + 1 }}. {{ Music.name }} by {{ Music.artist }}
        <button
          @click="Consoling"
          style="font-size: 24px, color:red"
          :class="[Music.name, By, Music.artist]"
        >
          Add to Playlist
        </button>
      </h2>
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
html {
  display: flex;
  flex-direction: column;
}

.Header {
  position: relative;
}
.Hidden {
  margin: 2rem 2rem 0 0;

  height: 45rem;
  overflow: hidden;
  overflow-y: scroll;
}
/* CSS */
button {
  background-color: #3dd1e7;
  border: 0 solid #e5e7eb;
  box-sizing: border-box;
  color: #000000;

  font-family: ui-sans-serif, system-ui, -apple-system, system-ui, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif,
    "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
  font-size: 0.25rem;
  font-weight: 700;
  justify-content: center;
  line-height: 0.75rem;
  padding: 0.75rem 1.65rem;
  position: relative;
  text-align: center;
  text-decoration: none #000000 solid;
  text-decoration-thickness: auto;

  position: relative;
  cursor: pointer;
  transform: rotate(-2deg);
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}

button:focus {
  outline: 0;
}

button:after {
  content: "";
  position: absolute;
  border: 1px solid #000000;
  bottom: 4px;
  left: 4px;
  width: calc(100% - 1px);
  height: calc(100% - 1px);
}

button:hover:after {
  bottom: 2px;
  left: 2px;
}

@media (min-width: 768px) {
  button {
    padding: 0.75rem 3rem;
    font-size: 1.25rem;
  }
}
</style>
