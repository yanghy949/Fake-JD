<script setup>
</script>

<template>
  <div class="search">
    <div><a href="" class="logo"></a></div>
    <div class="inputBox">
      <input type="text">
      <a href="" style="align-content: center;margin-right: 10px">
        <img src="../assets/image/photo.svg" alt="">
      </a>
      <button class="btn">
        <img src="../assets/image/search.svg" alt="">
      </button>
    </div>
    <div class="shop"><img src="../assets/image/购物车.svg" alt=""><i>0</i><span>我的购物车</span></div>
  </div>
</template>

<style scoped>
.search {
  background-color: white;
  width: 100%;
  height: 52px;
  display: flex;
  align-content: center;
  align-items: center;
  justify-content: center;
  border-bottom: 2px solid red;
  z-index: 9999;
}

.logo {
  background: url(../assets/image/Logo.png);
  background-position-y: -120px;
  background-size: 190px 160px;
  cursor: pointer;
  display: block;
  height: 40px;
  outline-style: none;
  width: 125px;
}

.inputBox {
  width: 30vw;
  display: flex;
  border: 2px solid red;
  margin: 0 30px;
}

.inputBox input {
  height: 31px;
  width: 90%;
  font-size: 12px;
  padding: 0 10px;
  border: none;
}

.inputBox input:focus {
  outline: none;
}

.btn {
  background-color: red;
  width: 58px;
  border: none;
}

.shop {
  border: 1px solid #EEEEEEFF;
  height: 31px;
  width: 130px;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}

.shop img {
  width: 25px;
}

.shop span {
  color: red;
  font-size: 12px;
}

.shop i {
  background-color: rgb(225, 37, 27);
  border-radius: 7px;
  color: rgb(255, 255, 255);
  font-size: 12px;
  font-style: normal;
  font-weight: 400;
  line-height: 12px;
  min-width: 12px;
  padding: 1px 3px;
  text-align: center;
  align-self: start;
}
</style>