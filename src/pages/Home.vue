<template>
  <div class="container">
    <img class="banner" src="images/ifood-banner.png" alt="banner-ifood" />
    <div class="categories-box">
      <categories></categories>
    </div>
  </div>
</template>

<script>
import Categories from "../components/Categories";
export default {
  name: "Home ",
  components: {
    categories: Categories
  }
};
</script>
<style scoped>
.categories-box {
  padding: 20px 0;
}
.banner {
  width: 100%;
  height: 245px;
  margin: 20px 0;
}
</style>
