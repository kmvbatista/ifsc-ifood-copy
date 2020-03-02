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
  name: 'FoodOption',
  props: ['photoUrl', 'name'],
};
</script>

<style>
.main {
  padding: 0 3px 0 3px;
}
.photo {
  border-radius: 50%;
}

.category-text {
  text-align: center;
}

.photo {
  width: 120px;
  height: 120px;
  object-fit: cover;
}
</style>
