<template>
  <div>
    <div class="column details-container container">
      <div class="row">
        <img src="@/../public/icons/star.svg" alt="avaliação" class="rating-icon" />
        <p class="rating">{{restaurant.rating}}</p>
        <p>(80 avalições)</p>
      </div>
      <h3>{{restaurant.name}}</h3>
      <p class="top-information">{{restaurant.description}}</p>

      <div class="row">
        <p
          class="top-information"
        >{{restaurant.category}} • {{restaurant.deliveryTime}} • {{restaurant.distance}} km •</p>
        <p v-if="restaurant.deliveryPrice">{{'R$ ' + restaurant.deliveryPrice}}</p>
        <div v-else class="free-delivery">ENTREGA GRÁTIS</div>
      </div>
      <aside class="empty-bag column">
        <img
          class="empty-bag-image"
          src="@/../public/icons/empty-bag.svg"
          alt="sua sacola está vazia"
        />
        <strong>Sua sacola está vazia</strong>
        <p>Adicione items</p>
      </aside>
      <h4>Pratos</h4>
      <div class="plates"></div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      restaurant: this.$route.params.restaurantData
    };
  }
};
</script>
<style scoped>
.free-delivery {
  border-radius: 2px;
  font-weight: bold;
  font-size: 0.9em;
}
.rating {
  color: var(--color-yellow);
}
.rating-icon {
  height: 13px;
  width: 13px;
  margin: auto 3px;
}
h3 {
  font-size: 2.8em;
  font-weight: 500;
}
.details-container {
  position: relative;
}
.details-container > * {
  margin-top: 10px;
}

.top-information {
  font-size: 1.1em;
  color: var(--color-gray-2);
}
.empty-bag {
  margin-top: 0;
  height: 100vh;
  position: fixed;
  right: 0;
  border-left: 1px solid var(--color-gray-lighter);
  box-shadow: 3px 8px 13px 1px #0000005c;
  align-items: center;
  justify-content: center;
}
.empty-bag > :not(:last-child) {
  margin-bottom: 20px;
}
.empty-bag-image {
  height: 200px;
  width: 200px;
  margin: 0 50px;
}
h4 {
  font-size: 1.6em;
  font-weight: 600;
  color: var(--color-gray-dark);
}
</style>