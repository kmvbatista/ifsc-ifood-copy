<template>
  <div class="container column home">
    <img class="banner" src="images/ifood-banner.png" alt="banner-ifood" />
    <categories></categories>
    <restaurants-list></restaurants-list>
  </div>
</template>

<script>
import Categories from "../components/Categories";
import RestaurantsList from "../components/RestaurantsList";
export default {
  name: "Home ",
  components: {
    Categories,
    RestaurantsList
  }
};
</script>
<style scoped>
.banner {
  width: 100%;
  height: 200px;
}
.home > * {
  margin-bottom: 50px;
}
</style>
