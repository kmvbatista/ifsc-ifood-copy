<template>
  <div>
    <strong>Restaurantes</strong>
    <div class="restaurants-grid">
      <restaurant-card
        v-for="restaurant in restaurants"
        :key="restaurant.name"
        :restaurant="restaurant"
      ></restaurant-card>
    </div>
  </div>
</template>
<script>
import RestaurantCard from "../components/RestaurantCard";
export default {
  components: {
    RestaurantCard
  },
  props: ["restaurants"]
};
</script>
<style scoped>
.restaurants-grid {
  margin-top: 20px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}
</style>