<script setup>

</script>

<template>
  <div class="foot">
    <div>
      <ul>
        <li>
          <div><img src="@/assets/image/多.png" alt=""><span>&nbsp;品类齐全，轻松购物</span></div>
        </li>
        <li>
          <div><img src="@/assets/image/快.png" alt=""><span>&nbsp;多仓直发，急速配送</span></div>
        </li>
        <li>
          <div><img src="@/assets/image/好.png" alt=""><span>&nbsp;正品行货，精致服务</span></div>
        </li>
        <li>
          <div><img src="@/assets/image/省.png" alt=""><span>&nbsp;天天低价，畅选无忧</span></div>
        </li>
      </ul>
    </div>
    <div>
      <div class="list">
        <h5>购物指南</h5>
        <ul>
          <li><a href="">购物流程</a></li>
          <li><a href="">会员介绍</a></li>
          <li><a href="">生活旅行</a></li>
          <li><a href="">常见问题</a></li>
          <li><a href="">大家电</a></li>
          <li><a href="">联系客服</a></li>
        </ul>
      </div>
      <div class="list">
        <h5>配送方式</h5>
        <ul>
          <li><a href="">上门自提</a></li>
          <li><a href="">211限时达</a></li>
          <li><a href="">配送服务查询</a></li>
          <li><a href="">配送费收取标准</a></li>
        </ul>
      </div>
      <div class="list">
        <h5>支付方式</h5>
        <ul>
          <li><a href="">货到付款</a></li>
          <li><a href="">在线支付</a></li>
          <li><a href="">分期付款</a></li>
          <li><a href="">公司转账</a></li>
        </ul>
      </div>
      <div class="list">
        <h5>售后服务</h5>
        <ul>
          <li><a href="">售后政策</a></li>
          <li><a href="">价格保护</a></li>
          <li><a href="">退款说明</a></li>
          <li><a href="">返修/退换货</a></li>
          <li><a href="">取消订单</a></li>
        </ul>
      </div>
      <div class="list">
        <h5>特色服务</h5>
        <ul>
          <li><a href="">夺宝岛</a></li>
          <li><a href="">DIY装机</a></li>
          <li><a href="">延保服务</a></li>
          <li><a href="">京东E卡</a></li>
          <li><a href="">京东通信</a></li>
          <li><a href="">京鱼座智能</a></li>
        </ul>
      </div>
      <div class="list">
        <h5>京东自营覆盖区县</h5>
        <p>京东已向全国2661个区县提供自营配送服务，支持货到付款、POS机刷卡和售后上门服务。</p>
        <a href="">查看详情</a>
      </div>
    </div>
    <div>
      <p><a href="">关于我们</a><span>|</span><a href="">联系我们</a><span>|</span><a href="">联系客服</a><span>|</span><a href="">合作招商</a><span>|</span><a href="">商家帮助</a><span>|</span><a href="">营销中心</a><span>|</span><a href="">手机京东</a><span>|</span><a href="">友情链接</a><span>|</span><a href="">销售联盟</a><span>|</span><a href="">京东社区</a><span>|</span><a href="">风险监测</a><span>|</span><a href="">质量公告</a><span>|</span><a href="">隐私政策</a><span>|</span><a href="">京东公益</a><span>|</span><a href="">Media &amp; IR</a></p>
    </div>
  </div>
</template>

<style scoped>
.foot {
  width: 100%;
  background-color: #e3e4e5;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 20px;
}
.foot>div:first-child{
  border-bottom: 1px solid ;
}
.foot>div:first-child ul {
  width: 1200px;
  list-style-type: none;
  display: flex;
  padding: 0;
}

.foot>div:first-child li {
  width: 300px;
  padding-left: 50px;
}

.foot>div:first-child li > div {
  width: 180px;
  height: 42px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.foot li img {
  width: 36px;
}

.foot li span {
  font-size: 18px;
  font-weight: 700;
  white-space: nowrap;
}
.foot>div:nth-child(2){
  display: flex;
  margin-top: 10px;
  padding-bottom: 10px;
  border-bottom: 1px solid ;
}
.list{
  width: 200px;
  font-size: 12px;
  font-weight: 400;
  color: #666666FF;
  display: grid;
}
.list h5{
  font-size: 14px;
  font-weight: 700;
  margin: 5px;
}
.list ul{
  list-style-type: none;
  padding: 0;
  margin: 0;
}
.list li{
  margin: 2px 0;
}
.list li :hover{
  color: red;
}
a{
  text-decoration: none;
  color: #666666FF;
}
.foot>div:nth-child(3){
  font-size: 12px;
}
.foot>div:nth-child(3) span{
  margin: 0 7px;
}
</style>