<template>
  <div class="header">
    <div class="logo-box">
      <img src="../assets/ifood-logo.png" alt="logo" />
    </div>
    <p>busque o que você quer</p>
    <p>entregar em</p>
    <div class="options-box">
      <div class="tt">
        <p>promoçoes</p>
      </div>
      <div class="tt">
        <p>perfil</p>
      </div>
      <div class="tt">
        <p>sacola</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
};
</script>

<style lang="css" scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-around;
}
.options-box {
  display: flex;
  justify-content: space-around;
}
.logo-box {
  height: 100px;
  width: 100px;
  padding: 20px 0 20px 0;
}
.tt {
  display: block;
}

img {
  max-width: 100%;
  max-height: 100%;
  top: 50%;
}
</style>
