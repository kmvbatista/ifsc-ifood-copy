<template>
  <default-card>
    <div class="card-infos column">
      <strong>{{plate.name}}</strong>
      <p class="plate-description">{{description}}</p>
      <p class="price">R$ {{plate.price}}</p>
    </div>
    <div class="photo" :style="`background-image: url(${plate.photo})`"></div>
  </default-card>
</template>

<script>
import DefaultCard from "./DefaultCard";
export default {
  props: ["plate"],
  components: {
    DefaultCard
  },
  computed: {
    description() {
      if (this.plate.description.length > 0) {
        return this.plate.description.slice(0, 80) + "...";
      }
      return this.plate.description;
    }
  }
};
</script>

<style scoped>
.photo {
  margin-left: 10px;
}
.plate-name {
  margin-bottom: 10px;
  font-size: 1.2em;
}
.plate-description {
  color: var(--color-gray-2);
}
.price {
  color: var(--color-green);
}
</style>
