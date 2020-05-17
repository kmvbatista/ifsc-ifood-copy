<template>
  <div class="container">
    <img class="banner" src="images/ifood-banner.png" alt="banner-ifood" />
    <div class="box">
      <categories></categories>
    </div>
    <div class="box">
      <restaurants-list></restaurants-list>
    </div>
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
.box {
  margin: 50px 0;
}
.banner {
  width: 100%;
  height: 245px;
}
</style>
