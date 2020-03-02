<template>
  <div class="main">
    <p>Categorias</p>
    <categories></categories>
  </div>
</template>

<script>
import Categories from '../components/Categories';
export default {
  name: 'Home ',
  components: {
    categories: Categories,
  },
};
</script>

<style></style>
