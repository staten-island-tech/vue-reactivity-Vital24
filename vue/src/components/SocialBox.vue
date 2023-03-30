<template>
  <section class="card">
    <a target="_blank" href="https://instagram.com/p/Chv0g4tMMqe">
      <img
        src="https://cdn-icons-png.flaticon.com/512/1419/1419647.png"
        alt="Instagram"
      />
    </a>

    <a target="_blank" href="https://discord.gg/V37aPXJNKY">
      <img
        src="https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/discord-square-black-icon.png"
        alt="Discord"
    /></a>

    <a target="_blank" href="https://youtu.be/uJGZ7YAwFaY">
      <img
        src="https://cdn-icons-png.flaticon.com/512/1384/1384044.png"
        alt="Youtube"
    /></a>
    <a target="_blank" href="https://twitter.com/whalensiths?lang=en">
      <img
        src="https://cdn-icons-png.flaticon.com/512/60/60580.png"
        alt="Twitter"
    /></a>
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
