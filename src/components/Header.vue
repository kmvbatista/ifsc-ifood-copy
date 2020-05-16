<template>
  <div class="box-with-border">
    <div class="container header">
      <div class="logo-box">
        <img class="logo" src="icons/ifood-logo.svg" alt="logo" />
      </div>
      <div class="search">
        <div class="search-icon-box">
          <img src="icons/search.svg" class="icon" alt="localização" />
        </div>
        <input type="text" placeholder="Busque por item ou loja" class="search-input" />
      </div>
      <div class="location">
        <p class="location-text">ENTREGAR EM</p>
        <div class="location-adress">
          <img src="icons/location.svg" class="icon" alt="localização" />
          <p>R. Orense, 584</p>
        </div>
      </div>
      <div class="options-box">
        <div class="header-option">
          <img src="icons/commerce.svg" class="icon" alt="promoções" />
          <p class="header-option-text">Promoções</p>
        </div>
        <div class="header-option">
          <img src="icons/door.svg" class="icon" alt="entrar" />
          <p class="header-option-text">Entrar</p>
        </div>
        <div class="header-option">
          <img src="icons/bag.svg" class="icon" alt="sacola" />
          <p class="header-option-text">Sacola</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
.box-with-border {
  border-bottom: 1px solid #dcdcdc;
}
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
.logo {
  width: 100px;
  height: 100px;
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
.search {
  background-color: #f7f7f7;
  border-radius: 4px;
  border: 1px solid #f2f2f2;
  display: flex;
  align-items: center;
}
.search-icon-box {
  padding: 8px;
}
.search-input {
  background-color: transparent;
  border: none;
  width: 350px;
  height: 45px;
  line-height: 1.25em;
  outline: none;
}
.search-input::placeholder {
  color: rgb(158, 158, 158);
}
.location-text {
  color: rgb(158, 158, 158);
  font-size: 13px;
  font-family: "OpenSans-Regular";
}
.location-adress {
  display: flex;
  font-family: "OpenSans-Regular";
}
</style>
