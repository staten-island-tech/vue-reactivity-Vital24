<template>
  <div>
    <h1 v-for="Food in Foods" :key="Food">{{ Food }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      Foods: [
        "Som Tam",
        "Laab",
        "Jok",
        "Pad Thai",
        "Pad See Ew",
        "Kuay Teow Neua",
        "Ba Mee Kiew",
        "Khao Niao",
        "Gai Yang",
        "Pla Plao",
        "Gai Hor Bai Toey",
        "Sai Oua",
        "Hor Mok Pla",
        "Hoi Tod",
        "Pad Kra Pao",
        "Khao Kha Moo",
        "Khao Kluk Kapi",
        "Khao Mok Gai",
        "Khao Pad",
        "Phrik Kaeng Phet",
        "Kaeng Kari",
        "Kaeng Khiao Wan",
        "Khao Soi",
        "Tom Yum",
        "Tom Kha Gai",
        "Kaeng Som",
        "Massaman Curry",
        "Panang Curry",
        "Khao Niao Mamuang",
        "Kluai Buat Chi",
      ],
    };
  },
};
</script>

<style scoped></style>
