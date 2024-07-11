<script setup>

</script>

<template>
  <div style="width: 100%;background-color: #e3e4e5">
    <div class="top">
      <div class="location">
        <img src="../assets/image/location.svg" alt="">
        <span>天津</span>
        <span>切换至企业版</span>
      </div>
      <ul class="fr">
        <li><a><span>你好，</span><span style="color: red">请登录</span></a></li>
        <b>|</b>
        <li><a>免费注册</a></li>
        <b>|</b>
        <li><a>我的订单</a></li>
        <b>|</b>
        <li><a>我的京东</a></li>
        <b>|</b>
        <li><a>企业采购</a></li>
        <b>|</b>
        <li><a>商家服务</a></li>
        <b>|</b>
        <li><a>网站导航</a></li>
        <b>|</b>
        <li><a>手机京东</a></li>
        <b>|</b>
        <li><a>网站无障碍</a></li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.top {
  color: rgb(153, 153, 153);
  display: flex;
  font-size: 12px;
  font-weight: 400;
  height: 21px;
  line-height: 30px;
  margin: 0px 250px 0px 250px;
  width: 1190px;
  justify-content: center;
  align-items: center;
}

.location span {
  margin: 0 10px;
}

.fr {
  margin-left: 100px;
  color: rgb(153, 153, 153);
  display: flex;
  font-size: 12px;
  font-weight: 400;
  height: 30px;
  line-height: 30px;
  list-style-type: disc;
  unicode-bidi: isolate;
  width: 727px;
  //overflow: hidden;
}

.fr > li {
  color: rgb(153, 153, 153);
  float: left;
  font-size: 12px;
  font-weight: 400;
  height: 30px;
  line-height: 30px;
  list-style: none outside none;
  text-align: left;
  justify-self: end;
  margin: 0 10px;
}
.fr>li :hover{
  color: red;
}
</style>