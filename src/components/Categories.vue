<template>
  <div>
    <strong>Categorias</strong>
    <div class="options-list">
      <div v-for="categorie in categories" :key="categorie.name">
        <food-option :name="categorie.name" :photoUrl="categorie.photoUrl"></food-option>
      </div>
    </div>
  </div>
</template>
<script>
import FoodOption from "./FoodOption";
import categoriesJson from "@/assets/categories.json";
export default {
  name: "Categories",
  components: {
    "food-option": FoodOption
  },
  data() {
    return {
      categories: categoriesJson
    };
  },
  created() {
    console.log(categoriesJson);
  }
};
</script>

<style scoped>
.options-list {
  display: flex;
  justify-content: space-between;
  text-align: center;
  margin-top: 15px;
}
strong {
  font-size: 17px;
}
</style>
