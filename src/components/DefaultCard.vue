<template>
  <div class="card row default-border">
    <slot></slot>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
* {
  --card-height: 120px;
}
.photo {
  background-size: cover;
  width: calc(var(--card-height) * 0.8);
  height: calc(var(--card-height) * 0.8);
}
.card {
  width: 100%;
  max-width: 500px;
  height: var(--card-height);
  padding: calc(var(--card-height) * 0.15);
  cursor: pointer;
  border: 1px solid #dcdcdc;
  border-radius: 4px;
  align-items: center;
}
.spacer {
  width: 1px;
  height: 100%;
  margin: 0 20px;
  background-color: var(--color-gray-lighter);
}

.card-infos {
  height: 100%;
  justify-content: space-between;
  max-width: calc(100% - 10px - var(--card-height) * 0.8);
}
</style>