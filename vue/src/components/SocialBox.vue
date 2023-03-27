<template>
  <section class="card">
    <img
      @click="target = `https://mikewhalen.tech/Resources`"
      src="https://cdn-icons-png.flaticon.com/512/1419/1419647.png"
      alt="Instagram"
    />
    <img
      @click="target = `https://mikewhalen.tech/Resources`"
      src="https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/discord-square-black-icon.png"
      alt="Discord"
    />
    <img
      @click="target = `https://mikewhalen.tech/Resources`"
      src="https://cdn-icons-png.flaticon.com/512/1384/1384044.png"
      alt="Twitter"
    />
    <img
      @click="target = `https://mikewhalen.tech/Resources`"
      src="https://cdn-icons-png.flaticon.com/512/60/60580.png"
      alt="Youtube"
    />
  </section>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style scoped>
.card {
  backdrop-filter: blur(16px) saturate(180%);
  -webkit-backdrop-filter: blur(16px) saturate(180%);
  background-color: rgba(17, 25, 40, 0.75);
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.125);
  width: 80vw;
  background-image: url("");
}
section {
  display: flex;
  justify-content: space-around;
}
html {
  background-image: url("https://images.unsplash.com/photo-1519681393784-d120267933ba?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1124&q=100");
  background-position: center;
}
img {
  padding: 1rem;
  width: 5vw;
}
</style>
