<template>
  <div>
    <strong>Categorias</strong>
    <div class="options-list">
      <div v-for="categorie in categories" :key="categorie.name">
        <category :name="categorie.name" :photoUrl="categorie.photoUrl"></category>
      </div>
    </div>
  </div>
</template>
<script>
import Category from "./Category";
import categoriesJson from "@/assets/categories.json";
export default {
  name: "Categories",
  components: {
    category: Category
  },
  data() {
    return {
      categories: categoriesJson
    };
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
