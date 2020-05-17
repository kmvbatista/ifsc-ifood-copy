<template>
  <div class="card row">
    <div class="restaurant-photo" :style="`background-image: url(${restaurant.photo})`"></div>
    <div class="spacer"></div>
    <div class="card-infos column">
      <strong>{{restaurant.name}}</strong>
      <div class="row">
        <img src="icons/star.svg" alt="avaliação" class="rating-icon" />
        <p class="rating">{{restaurant.rating}}</p>
        <p>• {{restaurant.category}} • {{restaurant.distance}}km</p>
      </div>
      <div class="row">
        <p>{{restaurant.deliveryTime}} •</p>
        <p v-if="restaurant.deliveryPrice">{{'R$ ' + restaurant.deliveryPrice}}</p>
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
* {
  --card-height: 120px;
}
.restaurant-photo {
  background-size: cover;
  width: calc(var(--card-height) * 0.8);
  height: calc(var(--card-height) * 0.8);
}
.card {
  width: 100%;
  max-width: 500px;
  height: var(--card-height);
  padding: calc(var(--card-height) * 0.15);
  border: 1px solid #dcdcdc;
  border-radius: 4px;
}
p {
  margin-right: 5px;
  font-size: 0.95em;
}
.spacer {
  width: 1px;
  height: 100%;
  margin: 0 20px;
  background-color: #f2f2f2;
}

.card-infos {
  height: 100%;
  justify-content: space-between;
}
.rating {
  color: #e7a74e;
}
.rating-icon {
  height: 13px;
  width: 13px;
  margin: auto 3px;
}
.free-delivery {
  color: #50a773;
}
</style>