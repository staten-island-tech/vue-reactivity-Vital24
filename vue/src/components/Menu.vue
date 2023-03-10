<template>
  <div>
    <h1 v-for="Food in ThaiFood" :key="Food">
      {{ Food.dish }} Price: {{ Food.price }}
    </h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      ThaiFood: [
        { dish: "Pad Thai", price: 2.0 },
        { dish: "Tom Yum Goong", price: 3.0 },
        { dish: "Green Curry", price: 4.0 },
        { dish: "Massaman Curry", price: 5.0 },
        { dish: "Som Tum", price: 2.5 },
        { dish: "Papaya Salad", price: 2.5 },
        { dish: "Pad Kra Pao", price: 3.5 },
        { dish: "Khao Pad", price: 3.0 },
        { dish: "Tom Kha Gai", price: 3.5 },
        { dish: "Gaeng Daeng", price: 4.5 },
        { dish: "Gaeng Keow Wan Kai", price: 4.0 },
        { dish: "Pla Rad Prik", price: 7.0 },
        { dish: "Pad See Ew", price: 3.5 },
        { dish: "Mango Sticky Rice", price: 2.5 },
        { dish: "Kai Med Ma Muang", price: 4.0 },
        { dish: "Tom Yam Kung", price: 3.0 },
        { dish: "Laab Moo", price: 3.5 },
        { dish: "Pad Krapow Moo Saap", price: 3.5 },
        { dish: "Khao Man Gai", price: 2.5 },
        { dish: "Khao Niew Mamuang", price: 2.5 },
        { dish: "Gai Yang", price: 3.0 },
        { dish: "Pla Pao", price: 8.0 },
        { dish: "Gaeng Som", price: 4.0 },
        { dish: "Pad Prik King", price: 3.5 },
        { dish: "Pad Pak Boong", price: 3.0 },
        { dish: "Rad Na", price: 3.5 },
        { dish: "Kao Soi", price: 4.0 },
        { dish: "Pad Siew", price: 3.5 },
        { dish: "Kai Jeow", price: 2.0 },
        { dish: "Khao Kha Moo", price: 2.5 },
        { dish: "Kai Pad Med Mamuang", price: 4.0 },
      ],
    };
  },
};
</script>

<style scoped></style>
