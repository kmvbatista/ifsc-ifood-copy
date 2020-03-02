<template>
  <div class="options-list">
    <div v-for="categorie in categories" :key="categorie.name">
      <food-option
        :name="categorie.name"
        :photoUrl="categorie.photoUrl"
      ></food-option>
    </div>
  </div>
</template>

<script>
import FoodOption from './FoodOption';
import categoriesJson from '@/assets/categories.json';
export default {
  name: 'Categories',
  components: {
    'food-option': FoodOption,
  },
  data() {
    return {
      categories: categoriesJson,
    };
  },
  created() {
    console.log(categoriesJson);
  },
};
</script>

<style>
.options-list {
  display: flex;
  justify-content: space-around;
  text-align: center;
}
</style>
