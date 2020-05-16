<template>
  <div class="main">
    <div class="food-photo">
      <img class="photo" :src="photoUrl" :alt="name" />
    </div>
    <p class="category-text">{{ name }}</p>
  </div>
</template>

<script>
export default {
  name: "FoodOption",
  props: ["photoUrl", "name"]
};
</script>

<style scoped>
.main {
  cursor: pointer;
}
.photo {
  border-radius: 50%;
}

.category-text {
  text-align: center;
}

.photo {
  width: 100px;
  height: 100px;
  object-fit: cover;
}
</style>
