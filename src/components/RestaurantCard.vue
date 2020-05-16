<template>
  <div class="card">
    <div class="restaurant-photo" :style="`background-image: url(${restaurant.photo})`"></div>
    <div class="spacer"></div>
    <div class="card-infos column">
      <strong>{{restaurant.name}}</strong>
      <div class="row">
        <img src="icons/star.svt" alt="avaliação" class="rating-icon" />
        <p class="rating">{{restaurant.rating}}</p>
        <p>* {{restaurant.category}} * {{restaurant.distance}}km</p>
      </div>
      <div class="row">
        <p>{{restaurant.deliveryTime}} * ''</p>
        <p v-if="restaurant.deliveryPrice">{{restaurant.deliveryPrice}}</p>
        <p v-else class="free-delivery">Entrega grátis</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["restaurant"]
};
</script>

<style scoped>
:root {
  --card-height: 70px;
}
.restaurant-photo {
  background-size: cover;
  width: calc(var(--card-heigth) * 80%);
  height: calc(var(--card-heigth) * 80%);
}
.card {
  display: flex;
  padding: calc(var(--card-height) * 10%);
}

.spacer {
  width: 1px;
  height: 100%;
  margin: 0 10px;
}

.card-infos {
  height: 100%;
  justify-content: space-between;
}
.rating {
  color: #e7a74e;
}
.rating-icon {
  width: 7px;
  height: 7px;
  margin-right: 2px;
}
.free-delivery {
  color: #50a773;
}
</style>