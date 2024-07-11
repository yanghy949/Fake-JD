<script setup>
import {ref, onMounted, onBeforeUnmount} from 'vue';

const slides = ref([]);
const currentSlide = ref(0);
let slideInterval = null;

const showSlide = (n) => {
  if (slides.value[currentSlide.value]) {
    slides.value[currentSlide.value].classList.remove('active');
  }
  currentSlide.value = (n + slides.value.length) % slides.value.length;
  slides.value[currentSlide.value].classList.add('active');
};

const nextSlide = () => {
  showSlide(currentSlide.value + 1);
};

onMounted(() => {
  slides.value = document.querySelectorAll('.slide');
  slideInterval = setInterval(nextSlide, 1500);
});

onBeforeUnmount(() => {
  clearInterval(slideInterval);
});
document.addEventListener('DOMContentLoaded', () => {
  const time = document.getElementById("time")
  time.innerText = (new Date()).getHours() + 1 + ":00"
})

</script>

<template>
  <div class="fl">
    <div style="width: 1200px">
      <div class="left">
        <ul>
          <li><a>家用电器</a></li>
          <li><a>手机</a><span>/</span><a>运营商</a><span>/</span><a>数码</a></li>
          <li><a>电脑</a><span>/</span><a>办公</a><span>/</span><a>文具用品</a></li>
          <li><a>家居</a><span>/</span><a>家具</a><span>/</span><a>家装</a><span>/</span><a>厨具</a></li>
          <li><a>男装</a><span>/</span><a>女装</a><span>/</span><a>童装</a><span>/</span><a>内衣</a></li>
          <li><a>美妆</a><span>/</span><a>个护清洁</a><span>/</span><a>宠物</a></li>
          <li><a>女鞋</a><span>/</span><a>箱包</a><span>/</span><a>钟表</a><span>/</span><a>珠宝</a></li>
          <li><a>男鞋</a><span>/</span><a>运动</a><span>/</span><a>户外</a></li>
          <li><a>房产</a><span>/</span><a>汽车</a><span>/</span><a>汽车用品</a></li>
          <li><a>母婴</a><span>/</span><a>玩具乐器</a></li>
          <li><a>食品</a><span>/</span><a>酒类</a><span>/</span><a>生鲜</a><span>/</span><a>特产</a></li>
          <li><a>艺术</a><span>/</span><a>礼品鲜花</a><span>/</span><a>农牧园艺</a></li>
          <li><a>京东买药</a><span>/</span><a>计生情趣</a></li>
          <li><a>图书</a><span>/</span><a>文娱</a><span>/</span><a>教育</a><span>/</span><a>电子书</a></li>
          <li><a>机票</a><span>/</span><a>酒店</a><span>/</span><a>旅游</a><span>/</span><a>生活</a></li>
          <li><a>支付</a><span>/</span><a>白条</a><span>/</span><a>保险</a><span>/</span><a>企业金融</a></li>
          <li><a>安装</a><span>/</span><a>维修</a><span>/</span><a>清洗</a><span>/</span><a>二手</a></li>
          <li><a>五金机电</a><span>/</span><a>元器件</a></li>
        </ul>

      </div>
      <div class="center">
        <img src="../assets/image/slide/(1).jpg" alt="1" class="slide active">
        <img src="../assets/image/slide/(2).jpg" alt="2" class="slide">
        <img src="../assets/image/slide/(3).jpg" alt="3" class="slide">
        <img src="../assets/image/slide/(4).jpg" alt="4" class="slide">
        <img src="../assets/image/slide/(5).jpg" alt="5" class="slide">
        <img src="../assets/image/slide/(6).jpg" alt="6" class="slide">
      </div>
      <div class="right" style="background-color: pink">
        <div id="user">
          <div>
            <img src="@/assets/image/logo2.png" alt="">
            <span style="margin: 3px 0;color: #666666">Hi~欢迎逛京东！</span>
            <span style="color: #333333;font-weight: 500"><a href="">登录</a>&nbsp;&nbsp;&nbsp;<a
                href="">注册</a></span>
          </div>
          <div>
            <div>
              <span>Plus会员</span>
              <span>专享立减</span>
              <span>立即开通&nbsp;></span>
            </div>
            <div>
              <span>企业会员</span>
              <span>新客补贴3000元</span>
              <span>立即开通&nbsp;></span>
            </div>
          </div>
        </div>
        <div class="secKill">
          <div class="ms">
            <div>
              <img src="../assets/image/京东秒杀.png" alt="" width="63px" height="12px">
              <img src="../assets/image/计时.png" alt="" width="24" height="24">
              <span><strong id="time">20:00</strong>场</span>
            </div>
            <div>
              <div><img src="../assets/image/ms/1.jpg" alt="" width="77px" height="77px"><span>￥100</span></div>
              <div><img src="../assets/image/ms/2.jpg" alt="" width="77px" height="77px"><span>￥100</span></div>
              <div><img src="../assets/image/ms/3.jpg" alt="" width="77px" height="77px"><span>￥100</span></div>
            </div>
          </div>
          <div class="ms">
            <div><img src="../assets/image/ms/ms.png" alt="" width="83"></div>
            <div>
              <div><img src="../assets/image/ms/4.jpg" alt="" width="77px" height="77px"><span>￥10</span></div>
              <div><img src="../assets/image/ms/5.jpg" alt="" width="77px" height="77px"><span>￥10</span></div>
              <div><img src="../assets/image/ms/6.jpg" alt="" width="77px" height="77px"><span>￥10</span></div>
            </div>
          </div>
          <div class="ms">
            <ul>
              <li>
                <div><img src="../assets/image/icon/礼品卡.png" alt=""><span>礼品卡</span></div>
              </li>
              <li>
                <div><img src="../assets/image/icon/加油卡.png" alt=""><span>加油卡</span></div>
              </li>
              <li>
                <div><img src="../assets/image/icon/话费.png" alt=""><span>话费</span></div>
              </li>
              <li>
                <div><img src="../assets/image/icon/游戏.png" alt=""><span>游戏</span></div>
              </li>
              <li>
                <div><img src="../assets/image/icon/酒店.png" alt=""><span>酒店</span></div>
              </li>
              <li>
                <div><img src="../assets/image/icon/云建站.png" alt=""><span>云建站</span></div>
              </li>
              <li>
                <div><img src="../assets/image/icon/五金城.png" alt=""><span>五金城</span></div>
              </li>
              <li>
                <div><img src="../assets/image/icon/PLUS会员.png" alt=""><span>PLUS会员</span></div>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.fl {
  display: flex;
  background-color: #e3e4e5;
  width: 100%;
  justify-content: center;
  padding: 10px 0;
}

.fl div {
  display: flex;
  justify-content: center;
}

.left {
  background-color: white;
  width: 190px;
  height: 470px;
  font-size: 14px;
  font-weight: 400;
  //margin-right: 10px;
}

.left > ul {
  list-style-type: none;
  padding: 0 10px;
  align-items: center;
}

.left li:first-child {
  padding-top: 10px;
}

.left li {
  padding: 3px 0;
}

.left span {
  padding: 0 2px;
}

.center {
  width: 590px;
  height: 470px;
  position: relative;
  overflow: hidden;
  margin: 0 15px;
}

.slide {
  width: 590px;
  height: 470px;
  position: absolute;
  opacity: 0;
  transition: opacity 1s ease-in-out;
}

.slide.active {
  opacity: 1;
}

.right {
  width: 390px;
  height: 470px;
  display: flex;
  flex-direction: column;
}

.right div {
  cursor: pointer;
}

#user {
  background-color: white;
  width: 390px;
  height: 96px;
  display: flex;
  justify-content: center;
}

#user div:first-child {
  width: 124px;
  height: 80px;
  font-size: 12px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

#user > div:first-child img {
  width: 28px;
}

#user > div:last-child {
  width: 264px;
  height: 96px;
  display: flex;
  align-items: center;
}

#user > div > div {
  width: 124px;
  height: 80px;
  border-radius: 4px;
  flex-direction: column;
  font-size: 12px;
  padding-left: 10px;
  margin-right: 10px;
}

#user > div > div:first-child {
  background-color: #ffe092;
  align-items: flex-start;
}

#user > div > div:last-child {
  background-color: #d0deff;
  //margin-left: 10px;
}

a {
  text-decoration: none;
}

.secKill {
  flex-direction: column;
}

.secKill > div {
  background-color: white;
  width: 390px;
  height: 110px;
  margin-top: 10px;
  align-items: center;
}

.ms > div:first-child {
  background-color: #fff2f2;
  width: 83px;
  height: 94px;
  border-radius: 4px;
  flex-direction: column;
  align-items: center;
}

.ms > div:last-child {
  width: 293px;
  height: 110px;
}

.ms > div:last-child > div {
  flex-direction: column;
  align-items: center;
  margin: 0 2px;
  font-size: 13px;
  color: red;
  font-weight: 700;
}

.ms:last-child {
  height: 124px;
}

.ms:last-child ul {
  list-style-type: none;
  display: flex;
  flex-wrap: wrap;
}

.ms:last-child li {
  width: 78px;
  height: 55px;
}

.ms:last-child li > div {
  flex-direction: column;
  align-items: center;
  font-size: 12px;
}

.ms:last-child li img {
  width: 28px;
}
</style>