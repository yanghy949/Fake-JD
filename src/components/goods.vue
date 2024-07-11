<script setup>
let items = [
  {image: "1.jpg", txt: "凤（feng） 牌红茶 经典58 特级凤庆滇红茶老字号 袋装茶叶 200g", price: 59, float: 99},
  {image: "2.jpg", txt: "小米（MI）小米13 徕卡光学镜头 第二代骁龙8处理器 超窄边屏幕 120Hz高刷 67W快充 12+256GB 白色 5G手机",price:3099 ,float:0},
  {image: "3.jpg", txt: "索尼（SONY）A6400入门级微单相机4K高清学生美颜vlog 索尼a6400 港货银色A6400【18-135套机】 套餐三",price:17392 ,float:0},
  {image: "4.jpg", txt: "Holy STONE HS430 遥控飞机四轴飞行器 无人机玩具 1080P 26分钟续航飞行航拍 黑色",price:939 ,float:99 },
  {image: "5.jpg", txt: "米愿 头戴式蓝牙耳机无线带麦音乐游戏吃鸡运动通话降噪耳麦可插卡插线适用华为苹果安卓手机电脑通用 B39【炫酷黑/呼吸灯/超长续航】",price:41 ,float:32 },
]
rand(items)
function rand(array) {
  for (let i = array.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [array[i], array[j]] = [array[j], array[i]];
  }
}
</script>

<template>

  <div class="goods">
    <ul>
      <li v-for="item in items" :key="item">
        <div>
          <img :src="'img/goods/'+item.image">
          <p v-text="item.txt"></p>
          <br>
          <span>￥<span style="font-size: 20px">{{ item.price }}.</span>{{ item.float }}</span>
        </div>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.goods {
  width: 1200px;
}

.goods ul {
  list-style-type: none;
  display: flex;
  margin: 5px;
  padding: 0;
}

.goods li {
  width: 230px;
  height: 322px;
  background-color: white;
  margin-right: 10px;
}

.goods li > div {
  flex-direction: column;
  font-size: 14px;
}

.goods img {
  width: 230px;
  height: 230px;
}

.goods p {
  width: 190px;
  height: 48px;
  margin: 0;
  line-height: 1.6;
  overflow: hidden;
}

.goods span {
  color: red;
  font-size: 12px;
  font-weight: 700;
}
</style>