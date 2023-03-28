<template>
  <div>
    <div class="Music">
      <h1>Personal Playlist</h1>
      <h1 v-for="(Music, index) in AddedMusic" :key="Music">
        {{ index + 1 }} {{ Music }}
        <button :class="[Music]" @click="RemoveMusic">
          Remove from Playlist
        </button>
      </h1>
    </div>
  </div>
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
    RemoveMusic(event) {
      console.log(event.target.className);
      let Removed = event.target.className;
      event.target.parentElement.remove();
      this.$emit("removes", Removed);
    },
  },
};
</script>

<style scoped>
button {
  background-color: #e05c7b;
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
/* .Music {
  text-shadow: 1rem 1rem 2rem black;

  color: white;
  text-decoration: solid;
}

hr {
  color: white;
}
svg {
  width: 25px;
} */
/* section {
  display: flex;
  flex-direction: column;
} */
</style>
