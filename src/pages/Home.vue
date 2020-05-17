<template>
  <div class="container column home">
    <img class="banner" src="images/ifood-banner.png" alt="banner-ifood" />
    <categories @chosecategory="filterRestaurants"></categories>
    <restaurants-list :restaurants="restaurants"></restaurants-list>
  </div>
</template>

<script>
import Categories from "../components/Categories";
import RestaurantsList from "../components/RestaurantsList";
import restaurantsJson from "@/assets/restaurants.json";

export default {
  components: {
    Categories,
    RestaurantsList
  },
  data() {
    return {
      restaurants: restaurantsJson
    };
  },
  methods: {
    filterRestaurants(choseCategory) {
      this.restaurants = restaurantsJson.filter(
        x => x.category === choseCategory
      );
    }
  }
};
</script>
<style scoped>
.banner {
  width: 100%;
  height: 250px;
}
.home > * {
  margin-bottom: 50px;
}
</style>
