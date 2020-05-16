<template>
  <div class="header">
    <div class="logo-box">
      <img class="logo" src="@/assets/images/ifood-logo.png" alt="logo" />
    </div>
    <div class="search">
      <img src="icons/search.svg" class="icon" alt="localização" >
    <input type="text" placeholder="Busque por item ou loja" class="search-input">
    </div>
    <div class="location">
      <p>ENTREGAR EM</p>
    <img src="icons/location.svg" class="icon" alt="localização" >
    </div>
    <div class="options-box">
      <div class="header-option">
        <img src="icons/commerce.svg" class="icon" alt="promoções" >
        <p class="header-option-text">Promoçoes</p>
      </div>
      <div class="header-option">
        <img src="icons/door.svg" class="icon" alt="entrar" >
        <p class="header-option-text">Entrar</p>
      </div>
      <div class="header-option">
        <img src="icons/bag.svg" class="icon" alt="sacola" >
        <p class="header-option-text">Sacola</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
};
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.header-option {
  display: flex;
}
.header-option > img {
  margin-right: 3px;
}
.options-box {
  display: flex;
  justify-content: space-around;
}
.options-box > :not(:last-child) {
  margin-right: 50px;
}

.logo-box {
  height: 100px;
  width: 100px;
  padding: 20px 0 20px 0;
}
.tt {
  display: block;
}
.icon {
  width: 20px;
  height: 20px;
}

.logo {
  max-width: 100%;
  max-height: 100%;
  top: 50%;
}
</style>
