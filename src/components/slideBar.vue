<script setup>
document.addEventListener('DOMContentLoaded', () => {
  const top = document.getElementById('top');

  top.addEventListener('click', () => {
    window.scrollTo({
      top: 0,
      behavior: 'smooth'
    });
  });

  window.addEventListener('scroll', () => {
    if (window.scrollY > 600) {
      top.style.display = 'grid';
    } else {
      top.style.display = 'none';
    }
  });

});
</script>

<template>
  <div class="slide">
    <ul>
      <li>
        <div>
          <span>为你推荐</span>
        </div>
      </li>
      <li>
        <div>
          <img src="@/assets/image/客服.svg" alt="">
          <span>客服</span>
        </div>
      </li>
      <li>
        <div>
          <img src="@/assets/image/反馈.svg" alt="">
          <span>反馈</span>
        </div>
      </li>
      <li id="top" style="display: none">
        <div>
          <img src="@/assets/image/顶部.svg" alt="">
          <span style="color: red">顶部</span>
        </div>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.slide {
  width: 1400px;
  height: 0;
  display: flex;
  justify-content: end;
  position: sticky;
  top: 100px;
  z-index: 999999;
}

.slide ul {
  list-style-type: none;
  padding:0;
}
.slide li{
  width: 58px;
  height: 58px;
  background-color: white;
  cursor: pointer;
}
.slide li :hover{
  color: red;
}
.slide li div{
  padding: 10px;
  font-size: 14px;
  font-weight: 400;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}
.slide li div img{
  width: 16px;
  margin: 0;
}
</style>