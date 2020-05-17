<template>
  <div @click="handleCardClick">
    <default-card>
      <div class="photo" :style="`background-image: url(${restaurant.photo})`"></div>
      <div class="spacer"></div>
      <div class="card-infos column">
        <strong>{{restaurant.name}}</strong>
        <div class="row">
          <img src="@/assets/icons/star.svg" alt="avaliação" class="rating-icon" />
          <p class="rating">{{restaurant.rating}}</p>
          <p>• {{restaurant.category}} • {{restaurant.distance}}km</p>
        </div>
        <div class="row">
          <p>{{restaurant.deliveryTime}} •</p>
          <p v-if="restaurant.deliveryPrice">{{'R$ ' + restaurant.deliveryPrice}}</p>
          <p v-else class="free-delivery">Entrega grátis</p>
        </div>
      </div>
    </default-card>
  </div>
</template>

<script>
import DefaultCard from "./DefaultCard";
export default {
  props: ["restaurant"],
  components: {
    DefaultCard
  },
  methods: {
    handleCardClick() {
      this.$router.push({
        name: "details",
        params: {
          restaurant: this.restaurant.name,
          restaurantData: this.restaurant
        }
      });
    }
  }
};
</script>

<style scoped>
.rating {
  color: var(--color-yellow);
}
.rating-icon {
  height: 13px;
  width: 13px;
  margin: auto 3px;
}
.free-delivery {
  color: var(--color-green);
}
</style>